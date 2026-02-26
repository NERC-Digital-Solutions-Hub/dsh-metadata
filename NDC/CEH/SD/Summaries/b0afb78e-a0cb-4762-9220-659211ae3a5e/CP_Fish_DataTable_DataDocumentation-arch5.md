# Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017.

## Overview
- A compiled dataset of fish abundance, habitat quality, water quality, flow, and climate variables for English rivers from 1975 to 2017.
- Data are organized by region (Anglian, Midlands, North East, North West, Thames, Southern, South West) and presented in separate DataTable region files.
- Key outputs include fish densities by species, habitat quality scores (HABSCORE), Gulf Stream Index (GSI), North Atlantic Oscillation Index (NAOI), and environmental covariates such as Degree Days.
- Approximate data collection period: 2019/04/03–2022/07/26; geographic focus: England.
- Principal authors: Rachel Ainsworth and Andy Nunn (University of Hull); funding from NERC Chempop.

## Data content and structure
- Core data: CP_Fish_DataTable_Region.csv containing fish densities (#/100 m2) for each species per survey, plus covariates (GSI, NAOI, Degree_Days) and HABSCORE-related habitat covariates.
- Regional structuring: Data are split into regional files; each row links to fish site, survey date, species, and density.
- Linking files: Fish_SiteID links to site variables and hydrology/chemistry data; Fish_SurveyDate, Fish_SurveyID used for survey-level records; Fish_SpeciesCode references CP_Fish_SpeciesTable.csv.
- Data coverage: Site tables and DataTables are linked; site coordinates are provided as Fish_Easting/Fish_Northing in both SiteTable and DataTable with occasional differences.
- Versioning: Multiple versions exist (e.g., 20211116_HIFI_Fish_JuvenileFish England_SiteTable.csv; 20220505_NFPD_Fish_England_PrioritySitesOnly_DataTable_JuvenileRemoved_Yorkshire); changes include corrections to juvenile site start/end dates, added covariates, removal of juvenile data from certain tables, and regional file splits.

## Provenance and licensing
- Data provenance: Derived from Environment Agency’s National Fisheries Population Datasets (NFPD), HABSCORE data from EA/UoH, and CHEMPOP/HQS values; supplemented with environmental indices (GSI, NAOI) and Degree Days.
- Data sources and citations: Datasets underpinning the file include NFPD fish counts, HABSCORE, and CHEMPOP data; Degree Days derived from water temperature data and modeling.
- Licenses: 
  - NFPD and EA surface water temperature archive data: Open Government Licence v3.0.
  - CHESS-MET air temperature data: copyrighted and licensed by UKCEH.
  - HABSCORE data: copyright/licensed by University of Hull.
- Data DOIs/links: 
  - Dataset citation: doi:10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e
  - NFPD data portal: data.gov.uk dataset on freshwater fish surveys
  - CHESS-MET data: CEH catalogue
- Related data: Data are related to ancillary datasets via Fish_SiteID, SiteVariables, and DataTables.

## Processing and quality assurance
- Data processing:
  - NFPD raw data filtered to sites surveyed at least 10 times.
  - Fish densities computed by converting counts to densities (per 100 m2) using recorded fishing area; handling of RUN1 and standard counts to normalize across semi-quantitative and first-run quantitative surveys.
  - Handling of missing standard counts, presence/absence notes, and [Best Run]/[Survey] suffixes to derive reasonable abundance estimates.
  - Aggregation of densities when multiple EA codes map to a single Chempop code.
  - Degree Days calculated to reflect water temperature exposure for prior year surveys; GSI/NAOI/air temperature incorporated as covariates.
- Quality assurance:
  - Data checked and cleaned; GAMM-based water temperature modelling and validation performed.
  - Model validation metrics reported (RMSE, normalized RMSE, Scatter Index).
- Software/tools:
  - Python 3 (Jupyter) for air temperature data processing.
  - R (R Studio) for Degree Days modeling and GAMM validation (packages such as MASS, scales, xts, lubridate, dplyr, ggplot2, mgcv, visreg, tidyverse).

## Metadata, standards, and discoverability
- Metadata completeness: Includes dataset title, author affiliations, data collection period, geographic scope, funding, licensing, data sources, file relationships, data processing steps, and QA details.
- Data model clarity: Clear linkage keys (Fish_SiteID, Fish_SurveyDate, Fish_SpeciesCode) and explicit regional file organization to support data discovery and interoperability.
- Documentation notes: Data caveats highlight occasional coordinate differences between SiteTable and DataTable, and that some NFPD sites may also include HIFI data; -9999 used for missing data codes.

## Access, distribution, and citations
- Public access: Data available via NFPD and CHESS-MET repositories, with archival links provided in the documentation.
- Citation guidance: Dataset should be cited using the provided citation and DOI; associated publications are not listed as linked in this record.
- Embargoes and usage: Open licensing for primary datasets; follow license terms for CHESS-MET and HABSCORE components.

## Versioning and updates
- File updates reflect corrections and additions (e.g., juvenile data handling, site date corrections, covariate additions, file splitting by region).
- Notable version changes: 
  - 2021 updates for juvenile site start/end dates and covariate data adjustments.
  - 2022 updates for juvenile removal from certain datasets and reorganization of region-specific files.
- Roll-forward planning: Data stewards should track versioned files and ensure downstream analyses reference the appropriate version to maintain reproducibility.

## Known caveats and data caveats
- Some sites labeled as NFPD may also contain HIFI data in metadata.
- Occasional discrepancies between coordinates in SiteTable vs DataTable due to survey-level location differences across years.
- Survey IDs beginning with -9999 indicate UH (NFPD) data for corresponding sites.
- Datasets require careful handling of runs, survey types, and coverage to ensure consistent density estimates across time and space.

## People and roles
- Key contributors: Rachel Ainsworth, Andy Nunn, Virginie Keller, Nuria Bachiller Janero, Monika Jurgens, Dina Sadykova, Pete Scarlett, Michael Eastman, Ian Cowx (and others listed as involved in data collection, processing, analysis, and submission).