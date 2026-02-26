# Supporting documentation

- Overview
  - Dataset provides model outputs of arable land area in Great Britain on a 2 km x 2 km grid for 2000–2089.
  - Four scenarios combining climate pathway (standard climate change vs AMOC collapse) and irrigation availability (with vs without widespread irrigation).
  - Climate data driven by UK HadRM3-PPE-UK projections; bias-corrected to align with observed 1960–1989 data.

- Dataset scope and scenarios
  - Grid: 2 km x 2 km resolution across Great Britain (400 hectares per grid cell).
  - Period: 2000–2089, yearly outputs.
  - Scenarios (Ag_model_sc{scenario #}):
    - 1: Climate tipping point = No; Irrigation = No
    - 2: Climate tipping point = No; Irrigation = Yes
    - 3: Climate tipping point = Yes; Irrigation = No
    - 4: Climate tipping point = Yes; Irrigation = Yes

- Data sources and climate modelling
  - Baseline climate driving the agricultural model: HadRM3-PPE-UK (Hadley Centre, UKCP09), 25 km resolution, using 30-year seasonal means (April–September) after bias correction.
  - AMOC collapse scenario: derived from HadGEM3 GC2 simulations with progressive AMOC weakening (2030–2050) and post-perturbation steady-state data (50–80 years after perturbation) used for temperature and rainfall.
  - Irrigation scenario: implemented as a threshold-based rainfall condition representing achieving optimal GB arable rainfall.

- Data structure and files
  - Four CSV files: Ag_model_sc{scenario #}.csv, each containing:
    - Unique grid cell identifier
    - Arable land area in hectares (0–400)
  - Grid coordinates file: Ag_model_grid_2km.csv
    - Provides easting/northing (cell center) and corner coordinates
    - Matches grid cell IDs to arable area data
  - Files together enable spatial mapping of arable area across GB for each scenario.

- Data quality, provenance, and methods
  - Quality control framework based on Fezzi & Bateman (2011) methods, central to the UK National Ecosystem Assessment approaches.
  - Input land use data sourced from the June Agricultural Census (GB) mapped to 2 km grid using 1972–2010 records (ten unevenly spaced years).
  - Extensive peer-reviewed references underpin methodology and interpretation (UK NEA/Follow-On, climate and land-use modeling studies).

- Accessibility, governance, and usage notes for Data Stewards
  - Versioned, scenario-based dataset with clear naming (Ag_model_sc{scenario #}) and accompanying grid coordinates for traceability.
  - Metadata should document: data sources, bias correction, climate model specifics, AMOC perturbation approach, irrigation definition, and spatial-temporal extents.
  - Potential considerations: large dataset size due to 2 km resolution over long time horizon; ensure appropriate storage, transfer, and indexing; note any updates or refinements to model inputs or bias correction.
  - Usage considerations: suitable for spatial policy analysis, climate-change impact assessment on land use, and evaluation of irrigation scenarios; align with related economic valuation work (referenced UK ecosystem studies).

- References
  - Bateman, I. et al. (2014, 2013), Fezzi et al. (2011, 2014, 2015), Jackson et al. (2015), Jenkins (2009), Mecking et al. (2016), Nakicenovic et al. (2000), NEA (2011), Safta et al. (2015), UKCP09 (HadRM3-PPE UK).