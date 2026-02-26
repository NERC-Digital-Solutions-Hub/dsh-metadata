CP_Fish_DataTable_readme.txt

## Overview
- Annual time series of fish abundance, densities, and covariate data for fish sites on English rivers, covering 1975–2017.
- Data include habitat quality indicators (HABSCORE), climatic covariates (Gulf Stream Index, NAO Index), and water temperature-related covariates (cumulative degree days above 12°C).
- Data derived from Environment Agency’s National Fisheries Population Datasets (NFPD) and related sources; processed to enable cross-site and cross-year analyses.

## Data Content
- Site table and Data table are separate regional files (Anglian, Midlands, North East, North West, Thames, Southern, South West); Species table is a single file listing species codes used in Fish_SpeciesCode.
- File CP_Fish_DataTable_Region.csv contains: fish abundance, densities (per 100 m2), NAOI, GSI, HABSCORE, and cumulative degree days above 12°C for each site and survey date.
- Species table identifies species referenced by Fish_SpeciesCode in the data tables.
- Relationship: Fish_SiteID is common across Fish_SiteID in DataTable files, Hydrology files, and chemical determinand files.

## File Structure and Relationships
- Regional files: CP_Fish_DataTable_Region.csv (region-specific data)
- Species linkage: CP_Fish_SpeciesTable.csv (species codes)
- Regions included: Anglian, Midlands, North East, North West, Thames, Southern, South West
- Data structure: 19 variables per region (vary by region)

## Provenance and Data Sources
- Primary source: Environment Agency’s National Fisheries Population Datasets (NFPD) – Freshwater Fish Counts for all species, areas, and years.
- Additional sources: HABSCORE data from EA and University of Hull; Gulf Stream Index (GSI) data; North Atlantic Oscillation Index (NAOI) data; Degree Days calculated from water temperature and air temperature data (CEH CHESS-MET, EA Water Temp Archive; BFI from CEH NRFA).
- Data processing lineage includes multiple historical files (e.g., 2019 EA data, various HABSCORE datasets) to assemble covariates and densities.

## Methodology and Processing
- Data collection: NFPD fish data downloaded 05/03/2019; filters applied to surveys with at least 10 visits per site.
- Densities: Convert raw counts to densities (numbers per 100 m2) using Run1 values from semi-quantitative surveys and first-catch values from quantitative surveys; apply rules for abundance categories (e.g., midpoints for ranges, assumptions for “Present”, “Best Run”, “Survey” suffixes).
- Data assembly: Run1_densities computed; densities summed across Chempop codes where needed; taxa without Chempop codes removed; fry data integrated with UoH juvenile data.
- Covariates:
  - GSI and NAOI: annual values aligned to survey year.
  - Degree_Days: cumulative degree days above 12°C prior to survey year, based on modeled water temperature (GAMM) and supporting temperature data (air from CHESS-MET, water from EA archive).
  - HABSCORE: habitat quality scores added for relevant sites/surveys.
- Software and tools: Python 3 (Jupyter) for data handling; R (GAMM modeling) for temperature modeling; packages include MASS, scales, xts, lubridate, dplyr, ggplot2, mgcv, visreg, and others.
- Quality checks: Data validated by Andy Nunn (14/07/2022); model performance assessed via RMSE, normalised RMSE (NRMSE), and Scatter Index (SI).

## Data Structure Details
- Site data fields include: Fish_SiteID, Fish_SurveyID, Fish_Easting, Fish_Northing, Fish_SurveyDate.
- Abundance data: Fish_SpeciesCode, Fish_Densities (per 100 m2).
- Covariates and habitat data: HQS_Bt_Small/Med/Large, HQS_Sal_Small/Large.
- Climate and timing covariates: GSI, NAOI, Degree_Days.
- DataTable structure per region: 19 variables (variable list varies by region; overall schema consistent across regions).

## Data Caveats and Notable Issues
- Some NFPD sites also contain HIFI data in metadata; coordinates between SiteTable and DataTable may differ for the same site across years.
- Survey IDs starting with -9999 correspond to University of Hull (UoH) data for NFPD sites.
- Survey data handling decisions (e.g., excluding some surveys, aggregation rules) can affect cross-year comparability.
- Some covariate data may be partial or regionally variable in coverage.

## Version History
- There are multiple dataset versions; notable update:
  - 20220505_NFPD_Fish_England_PrioritySitesOnly_DataTable_JuvenileRemoved_Yorkshire HABSCORE
  - Rationale: Corrections to start/end dates of some juvenile sites, addition of covariate data to data tables, removal of juvenile sites from NFPD data and site tables, and removal of some covariate data from the site table.
  - Update date: 13/06/2022
- Overall, dataset versions reflect refinements to juvenile site inclusion and covariate alignment.