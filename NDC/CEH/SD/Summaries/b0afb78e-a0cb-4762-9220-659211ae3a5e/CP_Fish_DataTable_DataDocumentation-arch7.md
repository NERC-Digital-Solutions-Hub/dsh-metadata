# Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017

## Overview
- A dataset combining fish abundance, habitat quality (HABSCORE), water quality, flow, and climate covariates across English rivers, with data organized by survey date (1975–2017 for fish data; later processing spliced in 2019–2022 for metadata).
- Primary sources: Environment Agency National Fisheries Population Datasets (NFPD), HABSCORE data from University of Hull, and CHEMPOP CHESS-MET data.
- Data designed for GIS applications and map-based analyses, enabling spatial exploration of fish communities alongside habitat and climate covariates.

## Geographic and temporal coverage
- Geographic scope: England, United Kingdom.
- Spatial granularity: site-level data with easting/northing coordinates; regionally partitioned datasets.
- Temporal scope: fish surveys spanning 1975–2017; covariates (e.g., Degree Days, Gulf Stream Index, NAOI) tied to survey years; data processing and metadata constructed up to 2022.

## Data structure and files
- Data are stored as regionally split files:
  - CP_Fish_DataTable_Region.csv: NFPD fish abundance and covariate data, including densities, GSI, HABSCORE, cumulative degree days, NAOI, site and survey identifiers.
- Relationships:
  - DataTable files (per region) are linked to a SiteTable (SiteVariables) by Fish_SiteID and Fish_SurveyDate.
  - Fish_SpeciesCode in DataTable files is specified in CP_Fish_SpeciesTable.csv.
- Regional organization:
  - Regions: Anglian, Midlands, North East, North West, Thames, Southern, South West.
- File versions and updates:
  - Multiple versions exist; notable updates on 16/11/2021, 13/06/2022, and 12/08/2022 (e.g., juvenile data adjustments, removal of juvenile data from NFPD datasets, covariate adjustments, and regional file splits).

## Spatial details and linkage
- Coordinates:
  - Fish_Easting and Fish_Northing are provided for survey sites; note occasional differences between SiteTable coordinates and DataTable coordinates for survey-specific locations.
- Linking keys:
  - Fish_SiteID uniquely identifies fish sites and links to site-level variables.
  - Fish_SurveyDate provides temporal context for each observation.
- Data join paths:
  - SiteVariables (SiteTable) <-> DataTables via FishSiteID and Fish_SurveyDate.
  - Species mapping via CP_Fish_SpeciesTable.csv to interpret Fish_SpeciesCode.

## Key variables and GIS relevance
- Spatial/identifying keys:
  - Fish_SiteID, Fish_SurveyID, Fish_Easting, Fish_Northing, Fish_SurveyDate.
- Biological and abundance data:
  - Fish_Densities: density of each species per 100 m2 (calculated from Run1 abundance and FISHED_AREA).
  - Run1_densities: densities derived from Run1 abundance; Run1_abundance and FISHED_AREA used in calculation.
- Covariates (habitat and climate):
  - HQS_Bt_Small, HQS_Bt_Med, HQS_Bt_Large: Habitat Quality Scores for trout at different size classes.
  - HQS_Sal_Small, HQS_Sal_Large: Habitat Quality Scores for salmon.
  - GSI: Gulf Stream Index (summer climate).
  - NAOI: North Atlantic Oscillation Index (winter climate).
  - Degree_Days: cumulative degree days above 12°C for 12 months prior to survey (derived from modeled water temperature and air temperature data).
- Additional attributes:
  - FISHED_AREA: area used to compute densities.
  - Missing data code: -9999.
- Data quality notes:
  - Some sites named in NFPD data may also contain HIFI data; survey IDs starting with -9999 indicate UoH data for corresponding NFPD sites.

## Provenance, licensing, and access
- Data provenance:
  - Derived from EA NFPD fish counts, HABSCORE data (UoH), and CHEMPOP data; climate covariates sourced from Gulf Stream and NAOI datasets; degree days from modeled water temperature and air temperature data.
- Licensing:
  - NFPD and Environmental Agency surface water temperature archive data: Open Government Licence v3.0.
  - CHESS-MET air temperature data: copyright and licensed by UKCEH.
  - HABSCORE data (University of Hull): copyright and license of University of Hull.
- Publications and citations:
  - Dataset citation: Ainsworth et al. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. DOI provided in metadata.
- Accessibility:
  - Data are linked to publicly accessible datasets and documentation (e.g., NFPD dataset pages and CHESS-MET documentation).

## Data processing and quality assurance
- NFPD data processing:
  - Raw data filtered to sites surveyed at least 10 times.
  - Counts converted to densities (per 100 m2) to account for sampling area differences; surveys without FISHED_AREA removed from density calculations.
  - Densities for species with multiple EA codes summed where appropriate.
  - Taxa with no Chempop species code removed; fry surveys removed (juvenile data merged with UoH juvenile data); juvenile data adjustments reflected in updated regional files.
- Covariates and climate:
  - GSI, NAOI added by year; Degree_Days computed from water temperature modeling.
- Temperature modeling and QA:
  - Water temperature modeled via GAMM in R; model validation used RMSE, NRMSE, and Scatter Index (SI).
- Software:
  - Air temperature processing: Python 3 (Jupyter) with pandas, netCDF4, xarray, numpy, etc.
  - Degree days and GAMMs: R with packages including MASS, mgcv, dplyr, tidyverse, etc.
- Data validation:
  - Data were checked by the project team (notably by key authors) as of 2022.

## Usage notes for GIS analysts
- Join strategy:
  - Use Fish_SiteID and Fish_SurveyDate to join the DataTable with SiteTable (SiteVariables) for spatial and covariate context.
  - Reference CP_Fish_SpeciesTable.csv to interpret Fish_SpeciesCode.
- Consider coordinate caveats:
  - Be aware of potential discrepancies between coordinates in the SiteTable and DataTable for the same surveys.
- Temporal alignment:
  - Primary fish data span 1975–2017; climate covariates (GSI, NAOI, Degree_Days) are year-referenced to survey periods.
- Data scope and resolution:
  - Data are provided regionally (Anglian, Midlands, North East, North West, Thames, Southern, South West) as separate files; multiple versions exist reflecting updates and juvenile data handling.
- Caveats:
  - Some NFPD sites may also include HIFI data in metadata.
  - -9999 indicates missing data.
  - Some SurveyID values starting with -9999 denote UoH data for corresponding NFPD sites.

## Summary of how the document supports GIS-centric work
- Provides a regionally segmented, linkable fish abundance and covariate dataset with explicit spatial (easting/northing) and temporal (survey date) fields.
- Includes habitat quality and climate covariates essential for spatial analysis of fish-habitat-climate relationships.
- Clearly documents data provenance, licensing, data processing steps, QA procedures, and version history, enabling traceable GIS workflows and reproducible mapping analyses.