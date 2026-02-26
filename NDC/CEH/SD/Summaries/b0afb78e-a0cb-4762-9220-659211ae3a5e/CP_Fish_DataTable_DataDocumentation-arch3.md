# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017.

## Overview
- A dataset documenting fish abundance, habitat quality, water quality, flow and climate variables for English rivers, spanning 1975–2017.
- Compiled by Rachel Ainsworth et al. (Universities of Hull) with contributions from multiple researchers; funding from NERC Chempop.
- Data assembled between 2019 and 2022; geographically limited to England.
- Primary aim aligned with monitoring framework authors: generate environmental health measures to scrutinise policy, inform decisions, and support future monitoring improvements.

## Data provenance and access
- Source data largely derived from Environment Agency National Fisheries Population Datasets (NFPD) and related HABSCORE data; supplemented with CHEMPop-derived variables.
- Licensing: 
  - NFPD and EA surface water temperature archive data – Open Government Licence v3.0 (Crown copyright and database rights).
  - CHESS-MET air temperature data – copyright/licensing by UKCEH.
  - HABSCORE data – University of Hull.
- Public access via:
  - NFPD dataset portal
  - CHESS-MET dataset catalog
- Data lineage includes explicit references to source datasets and the connections among site, survey, and species data (via Fish_SiteID, Fish_SurveyDate, and CP_Fish_SpeciesTable.csv).

## Dataset composition and structure
- File organization:
  - CP_Fish_DataTable_Region.csv containing fish densities, covariates, and site/survey metadata, regionally segmented (Anglian, Midlands, North East, North West, Thames, Southern, South West).
  - Linked via Fish_SiteID to SiteVariables and DataTables; Fish_SpeciesCode linked to CP_Fish_SpeciesTable.csv.
  - Regional data files and site tables (e.g., FishSite tables) support regional analyses.
- Content and covariates:
  - Fish densities (per 100 m2) for individual species per survey.
  - Habitat Quality Scores (HABSCORE) for trout and salmon by size class.
  - Climate/ocean covariates: Gulf Stream Index (GSI), North Atlantic Oscillation Index (NAOI).
  - Degree Days: cumulative water temperature above 12°C for the year prior to each survey.
- Metadata and data relationships:
  - FishSite_ID links site variables, hydrology data, and chemical determinands across tables.
  - Columns and site coordinates may have minor discrepancies between site tables and data tables.

## Methods and data processing
- NFPD data processing:
  - Filtered to sites surveyed at least 10 times; raw counts converted to densities (per 100 m2) to account for sampling area differences.
  - Handling of semi-quantitative RUN1 data and first-catch adjustments to harmonize quantitative and semi-quantitative surveys.
  - Rules applied to convert observed abundances into numeric estimates (midpoints for ranges, special handling for “Present”, “[Best Run]”, “[Survey]”).
  - Densities computed as Run1_abundance divided by FISHED_AREA, scaled to per 100 m2.
- Derived data:
  - HABSCORE entries integrated from EA and UoH sources.
  - GSI and NAOI values incorporated by year; Degree_Days computed from environmental data using R.
  - Degree Days modeled from air temperature (CHESS-MET) and water temperature data; GAMM models built in R for site-specific temperature estimates.
- Data processing and QA:
  - Data checked for consistency; GAMM model performance evaluated via RMSE, NRMSE, Scatter Index.
  - Software tools: Python (for air temperature and related processing), R (GAMMs, degree-day calculations, data transformations).

## Data quality, governance and use
- Quality assurance:
  - Data checked and validated; explicit QA processes described for GAMM model validation.
- Metadata and governance:
  - Clear provenance for each data stream; explicit data transformations and rules documented.
  - Open licensing facilitates reuse, subject to data provenance and licence terms; underlying data sharing constraints acknowledged (e.g., some datasets are restricted or require attribution).
- Potential barriers for users aligned with monitoring framework challenges:
  - Data gaps or inconsistent metadata can hinder reuse.
  - Territorial or dataset silos between sources may impede integration.
  - Public sharing requirements for some datasets may constrain the use of certain data components.

## Versions, updates and caveats
- Multiple data-file updates:
  - 20211116_HIFI_Fish_JuvenileFish_England_SiteTable.csv (juvenile data updates)
  - 20220505_NFPD_Fish_England_PrioritySitesOnly_DataTable_JuvenileRemoved_Yorkshire (data refinement, juvenile removal, covariate adjustments)
  - Rationale for updates includes correction of start/end dates for juvenile sites, data-table covariate adjustments, site removals, and regional file splitting.
- Caveats:
  - Some sites labeled as NFPD may also include HIFI data in metadata.
  - Coordinate discrepancies may exist between site-level and data-table coordinates.
  - Survey IDs beginning with -9999 correspond to UoH data for certain NFPD sites.

## Citation and use
- Data citation:
  - Ainsworth et al. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017. NERC EDS Environmental Information Data Centre. DOI: 10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e
- Intended use:
  - Provides environmental health indicators for monitoring and evaluating policy impacts on freshwater ecosystems; supports trend analysis, governance decisions, and future monitoring design.