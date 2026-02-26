# CP_Fish_DataTable_readme.txt

## Overview
- Time period: 1975-2017
- Geographic scope: English rivers
- Content: Annual time series of fish abundance, fish densities and covariate data for fish sites from Environment Agencies NFPD dataset
- Covariates: Habitat quality indicators, climatic variables, and water temperature indicators
- Data organization: Site-level data and regionally split files (Anglian, Midlands, North East, North West, Thames, Southern, South West) plus a single Species table

## Data structure and files
- File List:
  - CP_Fish_DataTable_Region.csv: NFPD fish abundance and covariate data including species-specific densities, NAOI, GSI, HABSCORE, and water temperature-derived Degree Days
- Relationship between files: Fish_SiteID in Region/DataTable files matches across Hydrology and chemical determinands
- Versioning: Multiple versions exist; notable update:
  - 20220505_NFPD_Fish_England_PrioritySitesOnly_DataTable_JuvenileRemoved_Yorkshire_HABSCORE
  - Reason for update: Correct start/end dates for some juvenile sites, added covariates to data tables, removed juvenile sites from NFPD data and site tables, and removed some covariates from the sitetable

## Provenance
- Primary data source: Environment Agency's National Fisheries Population Datasets (NFPD) and Freshwater Fish Counts file
- HABSCORE data: From EA and University of Hull
- Climate covariates: Gulf Stream Index (GSI) and North Atlantic Oscillation Index (NAOI)
- Degree Days: Based on water temperature, using CEH CHESS-MET air temperature data and EA Water Temperature Archive
- Validation/QA: Data checked by Dr. Andy Nunn (14/07/2022); GAMM model predictions evaluated with RMSE, NRMSE, and Scatter Index

## Methodology and processing
- Data selection: NFPD sites with at least 10 surveys included
- Densities: Converted from raw fish counts to densities (numbers per 100 m2)
- Handling survey types: Used RUN1 from quantitative surveys and semi-quantitative data; applied rules to estimate abundance when counts were missing or labeled in various ways
- Taxa handling: Excluded taxa without Chempop codes; fry data merged with UoH juvenile data
- Covariates integration:
  - HABSCORE: Habitat quality for specified size classes
  - GSI and NAOI: Annual climate covariates
  - Degree_Days: Cumulative degree days above 12°C for the year prior to each survey
- Software/tools:
  - Python (Jupyter) for air temperature-related calculations
  - R (GAMM modeling) with packages such as MASS, mgcv, dplyr, etc., for temperature modelling and model validation

## Data attributes and structure
- Regional data organization: Separate region files (Anglian, Midlands, North East, North West, Thames, Southern, South West)
- Species table: Single file indicating species referenced in Fish_SpeciesCode
- Main variables (per region file):
  - Fish_SiteID, Fish_SurveyID
  - Fish_Easting, Fish_Northing
  - Fish_SurveyDate
  - Fish_SpeciesCode
  - Fish_Densities (density per 100 m2)
  - HQS_Bt_Small, HQS_Bt_Med, HQS_Bt_Large (habitat quality for brown trout)
  - HQS_Sal_Small, HQS_Sal_Large (habitat quality for salmon)
  - GSI, NAOI, Degree_Days

## Data caveats
- Some NFPD-named sites may also include HIFI data in metadata
- Coordinate discrepancies: Fish_Easting/Fish_Northing can differ between SiteTable and DataTable across years
- SurveyID values starting with -9999 indicate UoH data corresponding to NFPD sites
- Regional and year-to-year survey data alignment may require careful cross-checking

## GIS implications and usage
- Enables spatial visualization of fish densities across English rivers with consistent regional schema
- Covariates support habitat suitability and climate influence mapping
- Key join keys: Fish_SiteID and Fish_SurveyID; use coordinates for map display
- Be mindful of data updates (juvenile removals and covariate adjustments) when comparing across versions