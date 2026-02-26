# Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017

## Overview
- A dataset of fish abundance, habitat quality, water quality, flow, and climate data from English rivers covering 1975–2017.
- Data are organized by survey date and region, including fish densities, HABSCORE habitat scores, and climatic/water temperature covariates.
- Key data products are site-level and survey-level tables linking species densities to site characteristics and covariates.

## Authors, timing, and scope
- Authors: Rachel Ainsworth et al. (University of Hull)
- Date of data collection: Approx. 2019-04-03 to 2022-07-26
- Geographic scope: England
- Funding: NERC Chempop grant NE/S000100/2

## Access, licensing, and provenance
- Licenses:
  - NFPD and EA surface water temperature archive data: Open Government Licence v3.0 Crown copyright and database rights
  - CHESS-MET air temperature data: copyright licensed by UKCEH
  - HABSCORE data: copyright licensed by University of Hull
- Public access:
  - Data and licences information available via provided public links (NFPD and CHESS-MET)
- Data provenance and relationships:
  - Derived from Environment Agency National Fisheries Population Datasets (NFPD) and HABSCORE data
  - Linked data: Fish_SiteID and Fish_SurveyDate connect to SiteVariables and DataTables; Fish_SpeciesCode referenced in CP_Fish_SpeciesTable.csv
  - Related datasets include branch data like CP_Fish_SpeciesTable.csv and multiple region-specific files
- Citation:
  - Ainsworth et al. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017. NERC EDS Environmental Information Data Centre. https://doi.org/10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e

## Structure and content of the data
- Data files:
  - CP_Fish_DataTable_Region.csv: NFPD fish abundance and covariate data including density estimates for each species, GSI, HABSCORE, cumulative degree days, NAOI, site and survey date
- Regional organization:
  - Data tables are separated into regional files (Anglian, Midlands, North East, North West, Thames, Southern, South West)
- Key variables (example):
  - Fish_SiteID, Fish_SurveyID, Fish_Easting, Fish_Northing, Fish_SurveyDate
  - Fish_SpeciesCode, Fish_Densities (per 100 m2)
  - HABSCORE covariates (HQS_Bt_Small, HQS_Bt_Med, HQS_Bt_Large, HQS_Sal_Small, HQS_Sal_Large)
  - GSI, NAOI, Degree_Days
- Data relationships:
  - Fish_SiteID links site variables, hydrology, and chemical determinants
  - Fish_SpeciesCode is described in CP_Fish_SpeciesTable.csv
- Versions:
  - Multiple data versions exist, including 20211116_HIFI_Fish_JuvenileFish_England_SiteTable.csv and 20220505_NFPD_Fish_England_PrioritySitesOnly_DataTable_JuvenileRemoved_Yorkshire
  - Updates include juvenile data adjustments, covariate data redistribution, and regional file splits

## Methodology and data processing
- Data sources and collection:
  - NFPD fish data downloaded 2019-03-05 from EA data portal; filtered to sites surveyed at least 10 times
  - HABSCORE data provided by EA and University of Hull
  - GSI and NAOI climate indices integrated from external sources
- Density calculation:
  - Raw fish counts converted to densities (numbers per 100 m2) to account for varying sampling areas
  - Only semi-quantitative surveys and RUN1 from quantitative surveys used for density estimation
  - Where counts were incomplete or qualitative:
    - Use midpoints for abundance ranges (e.g., 1–9 → 5; 10–99 → 55; etc.)
    - Present or best-run indicators translated into equivalent densities according to defined rules
  - Densities for species with a single Chempop code but multiple EA codes summed
  - Surpluses with missing fishing area data removed
- Covariates and modelling:
  - Degree Days derived from water temperature data
  - Water temperature modelled using GAMMs (R: mgcv) and validated against EA gauging stations
  - Air temperature data prepared in Python; degree days and other covariates prepared accordingly
- Quality assurance:
  - Data checked by researchers; GAMM model performance evaluated using RMSE, NRMSE, Scatter Index
- Software and tools:
  - Air temperature: Python 3 (Jupyter, pandas, netCDF4, xarray, etc.)
  - Degree Days and GAMM: R (MASS, scales, xts, lubridate, dplyr, mgcv, etc.)

## Data quality, caveats, and notes
- Data quality checks performed; model validation conducted for predictive components
- Caveats:
  - Some site names in NFPD data also include HIFI data in metadata
  - Minor discrepancies between site coordinates in Fish_Easting/Fish_Northing across SiteTable and DataTable
  - SurveyID values starting with -9999 indicate UoH (NFPD) data
- Missing data:
  - Missing data codes: -9999
- Coverage and granularity:
  - Regional data files and multiple versions may affect cross-region comparisons
  - Juvenile data adjustments and site-level start/end date corrections reflected in updated versions

## How this data supports data leadership and data strategy
- System-wide view: Combines fish abundance, habitat quality, hydrology, water quality, and climate across multiple English regions and decades
- Data quality and governance: Clear provenance, licensing, and version history; standardized densities and covariates across regions
- Discoverability and reuse: Public licensing, links to datasets and publications, and explicit data relationships enable integration into broader data ecosystems
- User-centric product development: Rich metadata and covariates support tailored analyses for policy colleagues and cross-network collaboration
- Data gaps and coordination: Highlights data availability constraints (e.g., site coverage, juvenile data handling) and the need for ongoing harmonization across regional datasets