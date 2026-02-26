# CP_Fish_DataTable_readme.txt

## Overview
- WP/task: Compile fish abundance, chemical, river flow, and environmental variables for English rivers, 1975–2017.
- Dataset: Annual time series of fish abundance/densities and covariates; includes habitat quality indicators (HABSCORE), climatic variables (Gulf Stream Index, NAO Index), and water temperature indicators (cumulative degree days ≥12°C).
- Authors: Dr Rachel Ainsworth (r.ainsworth@hull.ac.uk) and Dr Andy Nunn (A.D.Nunn@hull.ac.uk).

## Data & File Organization
- Structure: Site table and Data table are separate regional files (Anglian, Midlands, North East, North West, Thames, Southern, South West); Species table is a single file listing species codes.
- Primary file: CP_Fish_DataTable_Region.csv containing NFPD fish abundance and covariate data (including species-specific densities and covariates).
- Covariates included: NAOI, GSI, HABSCORE, and cumulative degree days (Degree_Days) derived from water temperature data.
- Relationships: Fish_SiteID matches across DataTable files, Hydrology files, and Chemical determinand files.
- Versions: Multiple; updated file 20220505_NFPD_Fish_England_PrioritySitesOnly_DataTable_JuvenileRemoved_Yorkshire_HABSCORE (juvenile sites removed, start/end dates corrected, covariates adjusted). 
- Update date: 13 June 2022.

## Provenance & Data Sources
- Derived from Environment Agency’s National Fisheries Population Datasets (EA NFPD) including Freshwater Fish Counts and site/survey information.
- HABSCORE data provided by EA and University of Hull; various HABSCORE datasets listed (multiple files from 2020–2021).
- Climate covariates:
  - Gulf Stream Index (GSI) from Gulf Stream data resource.
  - North Atlantic Oscillation Index (NAOI) from NCAR Climate Data Guide.
  - Degree_Days derived from water temperature data using CEH CHESS-MET temperature data; rainfall/air temperature inputs and river basin data described.
- Processing and validation tools referenced:
  - Python 3 (Jupyter) for air temperature and degree days calculations.
  - R (GAMM) for modeling water temperature and validation.

## Methods

### Data Collection
- Source: NFPD fish data downloaded 05/03/2019; filtered to sites surveyed ≥10 times.
- Density calculation: Convert raw counts to densities (counts per 100 m2) using Run1 data; adjust for sampling area (FISHED_AREA); address varying survey types (RUN1, ALL_RUNS) to standardize densities.
- Handling missing or special cases:
  - When Run1 data missing, estimate abundances from qualitative categories using EU FAME/EFI+ conventions (midpoints for ranges, 1 for “Present,” etc.).
  - Special suffix handling: "[Best Run]" → first catch; "[Survey]" → use first-catch contribution to total; remove surveys with "[Survey]" when no standard counts and multiple runs.
  - Surveys with no FISHED_AREA removed; densities summed for taxa with multiple Chempop codes.
  - Fry data integrated with UoH juvenile data.
- HABSCORE, GSI, NAOI, and Degree_Days: Integrated per survey/year; Degree_Days computed from temperature data with GAMM-based modeling.

### Data Processing
- Filtering: Retain only NFPD sites surveyed ≥10 times; remove taxa without Chempop codes; sum densities where appropriate.
- Covariates: Integrate HABSCORE values for relevant sites/surveys; assign GSI/NAOI per year; compute Degree_Days for 12 months prior to survey.
- Software usage: Python for temperature-related calculations; R for GAMM modeling; QA performed on outputs.

### Quality Assurance (QA)
- Data reviewed by Dr. Andy Nunn (as of 14/07/2022).
- Model validation metrics for GAMM-derived temperature predictions: RMSE, normalised RMSE (NRMSE), Scatter Index (SI).

## Data Structure & Variables

### DataTable Region
- Structure: Regional files with 19 variables (layout consistent across regions).
- Key columns:
  - Fish_SiteID, Fish_SurveyID
  - Fish_Easting, Fish_Northing (site coordinates)
  - Fish_SurveyDate
  - Fish_SpeciesCode (reference to CP_Fish_SpeciesTable.csv)
  - Fish_Densities (density per 100 m2 per survey)
  - HQS_Bt_Small / HQS_Bt_Med / HQS_Bt_Large (brown trout habitat quality)
  - HQS_Sal_Small / HQS_Sal_Large (salmon habitat quality)
  - GSI (climate covariate)
  - NAOI (climate covariate)
  - Degree_Days (cumulative degree days >12°C; climate/fish covariate)

### Species Table
- Single file indicating species corresponding to Fish_SpeciesCode used in the data tables.

## Data Caveats
- Some NFPD-named sites may also include HIFI data in metadata.
- Occasionally, Fish_Easting/Northing coordinates differ between SiteTable and DataTable due to year-specific survey locations.
- SurveyID values starting with -9999 indicate UoH data for corresponding NFPD sites.

## File Lists & Relationships
- File: CP_Fish_DataTable_Region.csv (NFPD abundance and covariates; regionally segmented)
- Relationship: Fish_SiteID in the DataTable aligns with identifiers in Hydrology and Chemical determinand files to enable integrated analyses.

## Additional Notes for Data Support
- The dataset is designed to enable data discovery, combination with climate and habitat covariates, and the creation of self-serve analyses and dashboards for policy and research use.
- Users should be aware of versioned updates (notably 2022 juvenile-site removals and date corrections) when merging with external datasets or performing longitudinal analyses.