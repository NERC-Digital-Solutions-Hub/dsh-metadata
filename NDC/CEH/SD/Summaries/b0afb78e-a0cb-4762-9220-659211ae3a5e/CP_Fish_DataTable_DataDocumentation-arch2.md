# Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017.

## Overview
- A combined dataset of fish abundance, habitat quality, water quality, flow, and climate variables from English rivers, covering surveys from 1975 to 2017.
- Data include fish densities by species, habitat quality scores (HABSCORE) by size class, and climate covariates (Gulf Stream Index, North Atlantic Oscillation Index) plus environmental covariates (Degree Days, modeled water temperature, etc.).
- Regions are organized as separate regional files (Anglian, Midlands, North East, North West, Thames, Southern, South West) with links across tables via site and survey identifiers.
- Intended to support monitoring environmental health and policy performance over time with standardized outputs.

## Data provenance and access
- Principal authors: Rachel Ainsworth; Andy Nunn; with additional contributors from the University of Hull.
- Funding: NERC CHEMPop grant NE/S000100/2.
- Geographic scope: England.
- Timeframe: Data collection approximately 2019/04/03 – 2022/07/26 for the dataset release; historical data span 1975–2017.
- Data sources:
  - Environment Agency National Fisheries Population Datasets (NFPD) for fish counts/densities.
  - HABSCORE habitat quality data (EA and UoH sources).
  - CHEMPOP and CHESS-MET air temperature data; Gulf Stream Index (GSI); NAOI.
  - Degree Days derived from water temperatures and air temperatures; baseflow from CEH National River Flow Archive.
- Access/licensing:
  - NFPD and EA surface water temperature data under Open Government Licence v3.0.
  - CHESS-MET air temperature data licensed to UKCEH.
  - HABSCORE data copyright/licensed by University of Hull.
  - Public links to data portals provided for NFPD and CHESS-MET.
- Citation: Ainsworth et al. 2024, Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017. DOI: https://doi.org/10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e.

## Data structure and files
- DataTables are regionally partitioned: CP_Fish_DataTable_Region.csv contains fish abundance and covariates (density, GSI, HABSCORE, degree days, NAOI) linked to site and survey data.
- Relationships:
  - Fish_SiteID and Fish_SurveyDate link DataTable to SiteVariables and hydrology/chemical datasets.
  - Fish_SpeciesCode is defined in CP_Fish_SpeciesTable.csv.
- File list:
  - CP_Fish_DataTable_Region.csv
- Data organization:
  - DataTables are region-specific (Anglian, Midlands, North East, North West, Thames, Southern, South West).
- Multiple versions:
  - Updated files include 20211116_HIFI_Fish_JuvenileFish_England_SiteTable.csv (juvenile data updates) and 20220505_NFPD_Fish_England_PrioritySitesOnly_DataTable_JuvenileRemoved_Yorkshire (juvenile removals and covariate adjustments). Updates date: 16/11/2021; 13/06/2022; 12/08/2022.

## Methodology
- Data sources and processing:
  - NFPD fish data downloaded 05/03/2019; filtered to sites surveyed at least 10 times.
  - Densities converted from raw counts to densities (numbers per 100 m2) to standardize sampling effort across space and time.
  - Surveys with missing FISHED_AREA removed; densities for single or multiple EA codes aggregated appropriately; fry data combined with juvenile data from UoH.
  - HYDROGRAPHY: HABSCORE added for relevant sites/surveys. GSI and NAOI added by year.
  - Degree Days: calculated as cumulative degree days above 12°C for the 12 months prior to the survey; water temperature modeled from air temperature using GAMMs.
  - Water temperature modeling used GAMMs in R; model selection based on predictive performance.
- Processing steps:
  - Taxa without Chempop codes removed; hybrids or broad taxa excluded.
  - Densities computed as Run1_abundance / FISHED_AREA × 100.
  - Some species with multiple EA codes summed where applicable.
- Tools:
  - Python 3 (Jupyter) for air temperature, GSI, NAOI, and degree days data integration.
  - R (R Studio) with packages including MASS, scales, xts, lubridate, dplyr, ggplot2, mgcv for GAMM water temperature modeling and validation.
- Quality assurance:
  - Data checked by Andy Nunn; GAMM predictive performance evaluated using RMSE, normalized RMSE, and Scatter Index.

## Data quality and limitations
- Missing data coded as -9999.
- Caveats:
  - Some NFPD sites also contain HIFI data in metadata.
  - Occasional differences between coordinates in Fish_Easting/Fish_Northing across SiteTable vs DataTable (survey locations not identical year-to-year).
  - Survey IDs beginning with -9999 indicate UoH data for corresponding NFPD sites.
  - Fry data excluded/combined with juvenile data in certain updates; juvenile sites removed from some NFPD datasets in later versions.

## Versions and updates (summary)
- 2021-11-16: Update to HIFI juvenile data and site information; correction of start/end dates for juvenile sites; covariates added to data tables; juvenile data removed from some NFPD datasets; degree days added; data split into regional files.
- 2022-06-13 and 2022-08-12: Further updates including removal of juvenile sites from NFPD data, refinement of covariates, and reorganization into regional data tables.

## Data dictionary and key variables
- DataTable variables (region-specific; 19 variables per region):
  - Fish_SiteID: unique site code (Chempop project)
  - Fish_SurveyID: survey code (Chempop)
  - Fish_Easting / Fish_Northing: site coordinates
  - Fish_SurveyDate: survey date (dd/mm/yyyy)
  - Fish_SpeciesCode: species code (linked to CP_Fish_SpeciesTable.csv)
  - Fish_Densities: density of each species per survey (per 100 m2)
  - HQS_Bt_Small / HQS_Bt_Med / HQS_Bt_Large: habitat quality scores for brown trout by size class
  - HQS_Sal_Small / HQS_Sal_Large: habitat quality scores for salmon by size
  - GSI: Gulf Stream Index (annual, climate covariate)
  - NAOI: North Atlantic Oscillation Index (annual, climate covariate)
  - Degree_Days: cumulative degree days above 12°C for the 12 months prior to the survey

## Licensing and access
- NFPD and EA surface water temperature data: Open Government Licence v3.0 (Crown copyright and database rights).
- CHESS-MET air temperature data: licensed by UKCEH.
- HABSCORE data: copyright/licensed by University of Hull.
- Public data portals linked for access.
- Data intended for lawful, monitoring, and policy-assessment use.

## Citation and acknowledgement
- Full dataset citation: Ainsworth, R.F.; Keller, V.; Bachiller- Jareno, N.; Jürgens, M. D.; Eastman, M.; Sadykova, D; Rizzo, C.; Scarlett, P.; Peirson, G. ; Eley, F.; Antoniou, V.; Cowx, I.G.; Johnson, A.C.; Nunn, A. D. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e

## People involved
- Rachel Ainsworth; Andy Nunn; Virginie Keller; Nuria Bachiller Janero; Monika Jurgens; Dina Sadykova; Pete Scarlett; Michael Eastman; Ian Cowx; and others listed in the dataset documentation.