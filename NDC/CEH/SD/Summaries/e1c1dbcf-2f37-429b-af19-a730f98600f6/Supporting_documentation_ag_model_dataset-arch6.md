# Supporting documentation

- Overview
  - Dataset of model output from an agricultural land use model at 2 km grid resolution over Great Britain.
  - Covers 2000–2089 for four scenarios combining climate pathway (standard climate change vs AMOC collapse tipping point) and irrigation presence (with vs without irrigation).
  - Output: yearly arable area per grid cell, in hectares (0–400 ha per 2 km x 2 km cell).

- Climate and scenario details
  - Driving climate data: UK HadRM3-PPE-UK from UKCP09 projections (Hadley Centre).
  - Climate scenario options:
    - Standard climate change (SRES-A1B)
    - Climate tipping point via AMOC collapse
  - Irrigation: modeled as all grid boxes receiving at least a threshold rainfall, representing the optimal rainfall level for GB arable farming.
  - Bias correction: future projections bias-adjusted by shifting to align with observed data for 1960–1989.

- AMOC collapse and irrigation modeling
  - AMOC perturbation simulated with HadGEM3 (GC2 configuration); gradual collapse modeled 2030–2050 with a linear weighting function to reflect a progressive change.
  - Temperature and rainfall inputs used as seasonal (April–September) averages over 50–80 years after perturbation has ended for steady-state conditions.
  - Irrigation effect implemented as a threshold-based irrigation proxy tied to historical optimum rainfall.

- Data quality and provenance
  - Methodological basis: Fezzi & Bateman (2011, 2013) and UK National Ecosystem Assessment (NEA) approaches; widely peer-reviewed.
  - Grid and inputs: 2 km grid over Great Britain; land-use data derived from the June Agricultural Census at 2 km resolution for 1972–2010.
  - Quality considerations: aligns with established agro-environmental policy modeling frameworks; validated within referenced studies.

- Data structure and files
  - Four scenario CSV files: Ag_model_sc{scenario #}.csv
    - Scenario mapping:
      - 1: Climate tipping point = No; Irrigation = No
      - 2: Climate tipping point = No; Irrigation = Yes
      - 3: Climate tipping point = Yes; Irrigation = No
      - 4: Climate tipping point = Yes; Irrigation = Yes
    - Each file contains:
      - Grid cell identifier
      - Total arable land area per cell (hectares; maximum 400 ha)
  - Grid coordinates file: Ag_model_grid_2km.csv
    - Provides easting and northing coordinates for grid cell centers and corner extents (min/max x/y) matched to grid cell identifiers.
  - Grid and data scale: 2 km x 2 km grid across GB (400 hectares per cell).

- Usage and potential applications
  - Enables comparative analysis of arable land under different climate and irrigation scenarios.
  - Supports spatial policy analysis, climate risk assessment, and land-use planning at regional scales.
  - Data products designed to enable self-service exploration and facilitate linkage with other datasets (via the shared 2 km grid and cell identifiers).

- References (key sources)
  - Fezzi, Bateman, and colleagues on structural agricultural land-use modeling and environmental/economic assessment
  - UK National Ecosystem Assessment and follow-on studies
  - UK climate projection sources (UKCP09, HadRM3-PPE-UK)
  - AMOC-related climate modeling studies (HadGEM3, GC2 configurations)