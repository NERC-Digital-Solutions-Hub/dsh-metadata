# Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017.

## Overview
- Datasets describe fish abundance, habitat quality, water quality, flow, and climate factors across English rivers from 1975 to 2017.
- Variables evolve over time and are organized by survey date, including fish densities, HABSCORE habitat scores, climate indices, and water temperature data.
- Geographic focus: England; data linked to specific fish sites and surveys.

## Authors and Funding
- First author: Rachel Ainsworth (University of Hull); coauthors include Andy Nunn and others.
- Data collection dates: approx. 2019-04-03 to 2022-07-26.
- Funding: NERC CHEMPoP grant NE/S000100/2.
- Citation: Ainsworth et al. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. DOI: 10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e.

## Data Content and Structure
- File: CP_Fish_DataTable_Region.csv (NFPD fish abundance and covariates; includes densities, GSI, HABSCORE, cumulative degree days, NAOI; site and survey data).
- Data are provided as separate regional files (Anglian, Midlands, North East, North West, Thames, Southern, South West).
- Key columns in DataTable:
  - Fish_SiteID, Fish_SurveyID, Fish_Easting, Fish_Northing
  - Fish_SurveyDate, Fish_SpeciesCode
  - Fish_Densities (density per 100 m2)
  - Habitat covariates: HQS_Bt_Small, HQS_Bt_Med, HQS_Bt_Large, HQS_Sal_Small, HQS_Sal_Large
  - Climate covariates: GSI (Gulf Stream Index), NAOI (North Atlantic Oscillation Index), Degree_Days
- Relationship data:
  - FishSite_ID links to SiteVariables and DataTables
  - CP_Fish_SpeciesTable.csv contains mapping for Fish_SpeciesCode
- Derived and related data:
  - Run1_densities calculated from Run1_abundance and FISHED_AREA
  - Degree_Days computed from water temperature data and modelled using R
- Related files updated over time (see Version history). Regions contain 19 variables per region file.

## Data Processing and Methodology
- NFPD fish data: downloaded 2019-03-05, filtered to sites surveyed at least 10 times.
- Density calculation:
  - Convert raw counts to densities (numbers per 100 m2) to standardize sampling effort.
  - Use RUN1 from semi-quantitative surveys and the first catch from quantitative surveys.
  - Handling of missing or categorical abundance data via EU FAME/EFI+ conventions (mid-points for ranges, assumptions for “Present”, “Best Run”, etc.).
  - When FISHED_AREA is missing, those surveys are removed.
  - Densities summed across multiple EA codes when needed (e.g., multiple strains/variants).
- Habitat and climate covariates:
  - HABSCORE values sourced from EA and UoH datasets.
  - GSI and NAOI pulled from external sources; Degree_Days derived from modelled water temperature data.
- Processing and modelling tools:
  - Air temperature derived with Python (Pandas, NetCDF4, XArray) for CHESS-MET data.
  - Water temperature modeled via GAMMs in R (packages: mgcv, etc.) with validation against EA data.
  - Degree_Days computed in R; model selection based on predictive performance.
- Quality assurance:
  - Data checked; GAMM predictive performance evaluated using RMSE, NRMSE, and Scatter Index.

## Data Structure and Relationships
- Data are organized by region files and "CP_Fish_DataTable_Region" with 19 variables per region.
- Linkages:
  - Fish_SiteID links site-level data to site variables and hydrology/chemical data.
  - Fish_SurveyDate ties surveys to time series.
  - Fish_SpeciesCode referenced in CP_Fish_SpeciesTable.csv.
- Data caveats:
  - Some sites labeled as NFPD may also contain HIFI data in metadata.
  - Occasional discrepancies between Fish_Easting/Fish_Northing in SiteTable vs DataTable (survey-level locations may differ across years).
  - Survey IDs starting with -9999 indicate UoH data for corresponding NFPD sites.

## Licensing, Access, and Citations
- Licensing:
  - NFPD and EA surface water temperature data: Open Government Licence v3.0 (Crown copyright and database rights, EMOU206.2).
  - CHESS-MET air temperature data: copyright licensed by UKCEH.
  - HABSCORE data (UoH): copyright licensed by University of Hull.
- Public access:
  - NFPD data portal; CHESS-MET portal; data and licensing information available via listed links.
- Data can be cited using the provided dataset citation.

## File Versions and Updates
- Multiple versions produced:
  - 2021-11-16: 20211116_HIFI_Fish_JuvenileFish_England_SiteTable.csv and related juvenile data updates.
  - 2022-06-13: 20220505_NFPD_Fish_England_PrioritySitesOnly_DataTable_JuvenileRemoved_Yorkshire
  - Updates included corrections to juvenile site start/end dates, addition/removal of covariates, relocation of covariates to site tables, addition of Degree_Days, and regional file splits.

## Known Caveats and Notes
- Some sites may combine NFPD and HIFI data in metadata.
- Location coordinates may differ slightly between site-level and survey-level data.
- -9999 survey IDs indicate UoH-derived data for NFPD sites.
- Data are best used with attention to regional segmentation and the 10-survey threshold used for NFPD site inclusion.

## How to Use
- Suitable for analyses seeking correlations between fish densities and habitat quality, flow indicators, and climate indices over multi-decade timescales in English rivers.
- Capable of supporting predictive modeling of fish densities using covariates such as HABSCORE, GSI, NAOI, and Degree_Days, with region-specific considerations.