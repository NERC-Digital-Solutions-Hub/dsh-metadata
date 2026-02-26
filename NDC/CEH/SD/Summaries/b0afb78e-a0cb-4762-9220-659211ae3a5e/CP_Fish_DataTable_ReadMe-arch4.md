# CP_Fish_DataTable_readme.txt

## Purpose and Scope
- English rivers, 1975–2017: annual time series of fish abundance, densities, and covariates (habitat quality, climate, water temperature).
- Source: Environment Agencies National Fisheries Population Datasets (NFPD).
- Authors: Dr. Rachel Ainsworth and Dr. Andy Nunn.

## Data Content and Structure
- Data are organized into regional site tables (Site and Data tables) and a single Species table.
- Regions included: Anglian, Midlands, North East, North West, Thames, Southern and South West.
- File of interest: CP_Fish_DataTable_Region.csv, containing fish densities for each species, covariates, and climate/water-temperature indicators (NAOI, GSI, HABSCORE, degree days ≥12°C) for each site and survey date.
- Relationship: Fish_SiteID links data across DataTable, Hydrology, and chemical determinand files.
- Species table describes species referenced in Fish_SpeciesCode.

## Versions and Updates
- Multiple versions exist; notable update: 20220505_NFPD_Fish_England_PrioritySitesOnly_DataTable_JuvenileRemoved_Yorkshire HABSCORE.
- Update reason: corrected start/end dates for juvenile sites, added covariates to data tables, removed juvenile sites from NFPD data and site tables, and removed some covariates from the sitetable.
- Update date: 13 June 2022.

## Provenance and Data Sources
- Primary source: Environment Agency’s National Fisheries Population Datasets (Freshwater Fish Counts, site and survey data).
- Additional covariates: HABSCORE data (EA/UoH), Gulf Stream Index (GSI), North Atlantic Oscillation Index (NAOI), degree days (Degree_Days).
- Degree Days: modeled water temperature above 12°C using air temperature (CEH CHESS-MET) and EA water temperature data.
- Software/tools: Python 3 (Jupyter) for temperature-derived covariates; R (various packages: MASS, mgcv, xts, etc.) for degree days and GAMM modeling.

## Methods and Processing
- Data collection: raw NFPD fish data downloaded 05/03/2019; filtered to sites surveyed at least 10 times.
- Density calculation: convert counts to densities (per 100 m2) to standardize across sampling effort; uses RUN1 and other rules to handle semi-quantitative vs. quantitative surveys; various handling rules for abundance categories and survey design.
- Covariates: HABSCORE, GSI, NAOI, Degree_Days added per survey/year.
- QA: Data checked by Dr. Andy Nunn (14/07/2022); GAMM model performance assessed with RMSE, normalized RMSE, and Scatter Index.

## Data Fields and Structure
- Data arrangement: regional SiteTable and DataTable files; a separate SpeciesTable file.
- Key variables in CP_Fish_DataTable_Region:
  - Fish_SiteID, Fish_SurveyID, Fish_Easting, Fish_Northing, Fish_SurveyDate
  - Fish_SpeciesCode, Fish_Densities
  - HQS_Bt_Small/Med/Large; HQS_Sal_Small/Large
  - GSI, NAOI, Degree_Days
- Data characteristics:
  - 19 variables per regional DataTable
  - SiteTable coordinates may differ slightly from DataTable coordinates; some SurveyID values begin with -9999 for UoH data.

## Data Caveats and Considerations for Data Leaders
- Some NFPD records also include HIFI metadata.
- Occasional coordinate discrepancies between SiteTable and DataTable; exact survey locations can vary year to year.
- Juvenile-site removal and regional data updates may affect coverage and covariate structure.
- Survey IDs with -9999 indicate University of Hull data for NFPD sites.

## Practical Implications for Data Leadership
- Clear lineage and documented processing steps support governance, audit trails, and reuse for policy or research.
- Structured regional segmentation aids scalable analytics and integration with broader data ecosystems.
- Ongoing attention to coordinate consistency, versioning, and documentation is essential to maintain data quality and comparability across years.