# CP_Fish_DataTable_readme.txt

## Overview
- Describes a dataset on fish abundance, chemical, river flow, and environmental variables for English rivers from 1975 to 2017.
- Focuses on annual time series of fish densities and covariates derived from Environment Agency’s National Fisheries Population Datasets (NFPD).
- Covariates include Habitat Quality Scores (HABSCORE), climatic indices (NAOI, Gulf Stream Index), and water temperature indicators (degree days above 12°C).
- Authors: Dr. Rachel Ainsworth and Dr. Andy Nunn (contact emails provided).

## Dataset structure and contents
- Site table and Data table are organized as separate regional files by region (Anglian, Midlands, North East, North West, Thames, Southern, South West).
- Species table is a single file listing species referenced in Fish_SpeciesCode.
- Main region file: CP_Fish_DataTable_Region.csv containing fish abundance, densities, and covariates (including NAOI, GSI, HABSCORE, and cumulative degree days above 12°C).

## File relationships
- Key identifier Fish_SiteID in the DataTable files aligns with Fish_SiteID in the SiteTable, Hydrology, and Chemical Determinand files.
- Data integrity relies on consistent site and survey coding across files.

## Provenance and data sources
- Derived from Environment Agency’s National Fisheries Population Datasets (NFPD) for fish counts, site details, and survey data.
- HABSCORE data sourced from multiple EA and University of Hull datasets.
- Climate covariates:
  - Gulf Stream Index (GSI) from Gulf Stream data sources.
  - North Atlantic Oscillation Index (NAOI) from NCAR/climate data guide.
  - Degree Days calculated from modeled water temperature (based on CEH CHESS-MET air temperature, EA water temperature archive, and CEH National River Flow Archive).
- Degree Days are computed as cumulative hours above 12°C for the year prior to each fish survey.

## Methodology and data processing
- Data collection: EA NFPD fish data downloaded 05/03/2019; filtered to sites surveyed at least 10 times.
- Densities: Convert raw counts to densities (numbers per 100 m2) using Run1 data from semi-quantitative surveys or first catch of quantitative surveys; special rules applied for various abundance indicators (present, best run, survey, etc.).
- Handling missing data: Surveys without FISHED_AREA are removed; densities summed across Chempop codes where appropriate; fry data combined with juvenile data from UoH.
- Covariates: HABSCORE (habitat quality), GSI, NAOI, and Degree_Days incorporated as site- and survey-level covariates.
- Processing steps: Regional data structure mirrors the same schema across regions; a dedicated Species table links species codes to metadata.

## Software and validation
- Degree Days computation performed in R (degree days model) and Python (Jupyter) for data preparation steps.
- GAMM-based water temperature modeling used to generate Degree_Days; model validation performed using RMSE, normalised RMSE, and Scatter Index.
- Documentation notes required packages and software (R, Python) and versioning details.

## Data structure and fields (key variables)
- Fish_SiteID: site code
- Fish_SurveyID: unique survey identifier
- Fish_Easting / Fish_Northing: site coordinates
- Fish_SurveyDate: survey date
- Fish_SpeciesCode: species code (links to Fish_SpeciesTable.csv)
- Fish_Densities: density of each species per 100 m2
- HQS_Bt_Small / HQS_Bt_Med / HQS_Bt_Large: habitat quality scores for brown trout by size class
- HQS_Sal_Small / HQS_Sal_Large: habitat quality scores for salmon by size class
- GSI: Gulf Stream Index
- NAOI: North Atlantic Oscillation Index
- Degree_Days: cumulative degree days above 12°C for the prior year

## Data caveats and notes
- Some NFPD sites may also contain HIFI data in metadata.
- Occasionally, Fish_Easting/Fish_Northing values differ between the SiteTable and DataTable due to survey-level location variations across years.
- SurveyID values starting with -9999 represent UoH data for corresponding NFPD sites.
- The dataset has multiple versions; a noted update (20220505_NFPD_Fish_England_PrioritySitesOnly_DataTable_JuvenileRemoved_Yorkshire HABSCORE) corrected start/end dates for some juvenile sites, adjusted covariates, and removed juvenile sites from NFPD data and site tables.

## Versioning
- Yes, multiple versions exist.
- Example update: 2022-06-13 (13/6/2022) addressing juvenile site corrections and covariate adjustments.

## Access and contact
- Primary authors listed with email addresses for provenance and methodological clarification.