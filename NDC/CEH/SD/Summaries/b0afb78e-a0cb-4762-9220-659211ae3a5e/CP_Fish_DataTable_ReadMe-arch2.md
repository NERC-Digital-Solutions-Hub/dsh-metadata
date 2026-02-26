# CP_Fish_DataTable_readme.txt

## General information
- WP/task: Fish abundance, chemical, river flow and environmental variables for English rivers (1975–2017).
- Dataset description: Annual time series of fish abundance and densities, with covariates (habitat quality indicators, climatic variables, water temperature indicators).
- Authors: Dr Rachel Ainsworth (r.ainsworth@hull.ac.uk), Dr Andy Nunn (A.D.Nunn@hull.ac.uk).

## Data & file overview
- Site table and Data table are regional files (Anglian, Midlands, North East, North West, Thames, Southern, South West); Species table is a single file mapping species codes.
- File List: CP_Fish_DataTable_Region.csv containing NFPD fish abundance, densities by species, NAOI, GSI, HABSCORE, cumulative degree days (≥12°C) per site/date.
- Relationship: Fish_SiteID links across Fish data tables, Hydrology, and chemical determinands.
- Versions: Yes; e.g., 20220505_NFPD_Fish_England_PrioritySitesOnly_DataTable_JuvenileRemoved_Yorkshire HABSCORE (update due to juvenile site date corrections, added covariates, and site removals); updated 13/06/2022.

## Provenance information
- Data source: Environment Agency’s National Fisheries Population Datasets (NFPD) and related HABSCORE datasets; Gulf Stream Index (GSI) and North Atlantic Oscillation Index (NAOI); Degree Days derived from water temperature data and air temperature (via CEH CHESS-MET and EA archives).
- Specific sources include: Freshwater Fish Counts (EA), multiple HABSCORE files from EA/UoH, GSI data, NAOI data, and degree-day calculations (R) using water temperature and air temperature datasets.
- Degree Days method: Cumulative degree days above 12°C for the year prior to surveys; water temperature modeled via GAMM in R; validation with EA-provided data.

## Methodological information
- Data collection: NFPD data downloaded 05/03/2019; sites required to have ≥10 surveys; densities calculated from raw counts (Run1) to standardize sampling effort across surveys and sites.
  - Conversion details: Densities = Run1_abundance / FISHED_AREA × 100 (units: # per 100 m²); handling of abundance categories and survey specifics described (e.g., RUN1, [Best Run], [Survey], etc.).
- Data processing: Remove taxa without Chempop codes; aggregate densities for multiple EA codes; retain surveys with zero catches; adjust fry data (combined with UoH juvenile data).
- Covariates: HABSCORE, GSI, NAOI, Degree_Days (climate/temperature covariates).
- Software/tools:
  - Air temperature and Degree Days: Python 3 (Jupyter) with pandas, netCDF4, xarray, etc.
  - Water temperature modeling and validation: R (MASS, mgcv, dplyr, etc.) with GAMMs; RMSE, NRMSE, Scatter Index for model QA.
- QA procedures: Data checked by Dr. Andy Nunn (14/07/2022); model performance validated using RMSE, NRMSE, SI.

## Data-specific information
- File structure: Site table, Data table regionally; Species table is a single file.
- Core variables (example list from CP_Fish_DataTable_Region):
  - Fish_SiteID, Fish_SurveyID, Fish_Easting, Fish_Northing, Fish_SurveyDate
  - Fish_SpeciesCode, Fish_Densities
  - HQS_Bt_Small, HQS_Bt_Med, HQS_Bt_Large (habitat quality scores for trout)
  - HQS_Sal_Small, HQS_Sal_Large (habitat quality for salmon)
  - GSI, NAOI, Degree_Days
- Data caveats:
  - Some NFPD sites may also include HIFI data in metadata.
  - Locations (Fish_Easting/Northing) can differ slightly between SiteTable and DataTable across years.
  - Some SurveyID values start with -9999 (UoH data for corresponding NFPD sites).

## Data caveats
- Variation in site coordinates between metadata and data tables across years.
- Some surveys include special identifiers (e.g., -9999) indicating specific data origins.
- Hybrids or non-standard taxa may be excluded due to Chempop coding.