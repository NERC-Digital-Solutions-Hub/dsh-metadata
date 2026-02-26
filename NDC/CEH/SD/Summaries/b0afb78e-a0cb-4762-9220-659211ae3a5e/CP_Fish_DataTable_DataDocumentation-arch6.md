# Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017

## Overview
- A compiled dataset of fish abundance, habitat quality, water quality, flow and climate metrics for English rivers spanning 1975–2017.
- Authors: Rachel Ainsworth et al. (University of Hull) with collaborators; funding from NERC Chempop.
- Data collection period: approx. 2019–2022 for metadata and processing; core data originate from EA and related sources.
- Geographic scope: England.

## Data Content
- Variables/covariates:
  - Fish data: Fish_SiteID, Fish_SurveyID, Fish_Easting, Fish_Northing, Fish_SurveyDate, Fish_SpeciesCode, Fish_Densities (per 100 m2).
  - Habitat quality: HQS_Bt_Small, HQS_Bt_Med, HQS_Bt_Large; HQS_Sal_Small, HQS_Sal_Large.
  - Climate/flow covariates: GSI (Gulf Stream Index), NAOI (North Atlantic Oscillation Index), Degree_Days (cumulative degree days above 12°C for the prior year).
- Data products:
  - DataTables of region-specific data and a linkable CP_Fish_DataTable_Region.csv with density estimates, covariates, and site/survey metadata.
  - CP_Fish_SpeciesTable.csv provides mappings for Fish_SpeciesCode.
- Data processing outputs:
  - Densities computed from raw counts (Run1_densities = Run1_abundance / FISHED_AREA × 100).
  - Special handling for semi-quantitative and first-catch data to standardize densities.
  - HABSCORE data integrated for habitat covariates; degree-days derived from temperature data; GSI/NAOI added by year.

## File Structure and Linkages
- Regional data supplied as separate files: Anglian, Midlands, North East, North West, Thames, Southern, South West.
- Main data file: CP_Fish_DataTable_Region.csv (including 19 variables per region).
- Linkages:
  - Fish_SiteID connects DataTable, SiteVariables, and hydrology/chemical datasets.
  - Fish_SurveyDate ties survey-level data; Fish_SpeciesCode cross-referenced in CP_Fish_SpeciesTable.csv.
- Related updated files:
  - 20211116_HIFI_Fish_JuvenileFish_England_SiteTable.csv
  - 20220505_NFPD_Fish_England_PrioritySitesOnly_DataTable_JuvenileRemoved_Yorkshire
  - Updates include juvenile data handling, date corrections, covariate additions/removals, and regional splits.

## Data Sources and Provenance
- Primary fish data from Environment Agency National Fisheries Population Datasets (NFPD): raw counts converted to densities after filtering to sites surveyed at least 10 times.
- HABSCORE habitat data provided by EA and University of Hull.
- Climate data:
  - Gulf Stream Index (GSI) from external source.
  - North Atlantic Oscillation Index (NAOI) from Climate Data Guide.
  - Air temperature via CEH CHESS-MET; water temperature via EA archive; degree-days modelled using GAMM in R.
- Coverage includes site-level and survey-level data linked through site identifiers and dates.

## Processing and Methods
- NFPD data processing:
  - Convert raw counts to densities (per 100 m2) using measured or modeled sampling areas.
  - Exclude surveys without FISHED_AREA; sum densities for multi-code species where appropriate.
  - Remove taxa without Chempop codes; exclude fry data when juvenile data from UoH available.
- HABSCORE integration for habitat covariates by site and survey.
- Climate covariates:
  - GSI/NAOI included as covariates; Degree_Days calculated from water temperature and air temperature data with a GAMM-based approach for temperature prediction.
- Tools used:
  - Python (Air temperature and related processing with Jupyter) and R (GAMM modeling, degree-day calculations, QA metrics).
- Quality checks:
  - Data checked by researchers; model validation for degree-day water temperature predictions using RMSE, NRMSE, Scatter Index.

## Licensing, Access and Citations
- Licenses:
  - NFPD and EA surface water temperature archive data: Open Government Licence v3.0.
  - CHESS-MET air temperature data: UKCEH license.
  - HABSCORE data: University of Hull copyright and license.
- Access: Dataset components and public data links provided; data suitable for public use with proper attribution.
- Citation: Ainsworth, R.F. et al. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017. NERC EDS Environmental Information Data Centre. DOI: 10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e

## Known Limitations and Caveats
- Some sites labeled as NFPD may also contain HIFI metadata; cross-reference carefully.
- Occasional discrepancies between coordinate sets:
  - Fish_Easting/Fish_Northing in SiteTable vs DataTable; survey locations may differ by year.
- Survey IDs starting with -9999 indicate UoH data for corresponding NFPD sites.
- Data are regionally partitioned; users should join region files via Fish_SiteID and Fish_SurveyDate to reconstruct complete site histories.

## Practical Use Guidelines for Data Support
- To enable self-service analysis:
  - Use Fish_SiteID to merge fish densities with site variables and hydrology/chemistry data.
  - Use Fish_SurveyDate and Fish_SpeciesCode to extract species-specific trends across surveys.
  - Leverage covariates HQS_Bt_*, GSI, NAOI, and Degree_Days to model fish densities against habitat and climate context.
  - Cross-check with CP_Fish_SpeciesTable.csv to map species codes to taxa.
- When updating analyses:
  - Be aware of file updates (e.g., juvenile data adjustments, date corrections, covariate changes) and apply consistency checks across regional files.