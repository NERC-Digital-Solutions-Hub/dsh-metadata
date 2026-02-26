# Supporting documentation

## Overview
- Describes a dataset of modelled yearly arable land area for Great Britain on a 2 km grid from 2000 to 2089.
- Four scenario combinations: standard climate change vs AMOC tipping point (collapse) and with vs without widespread irrigation.
- Driven by regional climate projections and an agricultural land-use model; outputs are provided as gridded arable-area data (in hectares).

## Data content and structure
- Four CSV files named Ag_model_sc{scenario #}.csv, each containing:
  - Unique grid cell identifiers
  - Arable land area per grid cell (in hectares; max 400 ha)
- One grid file: Ag_model_grid_2km.csv containing:
  - Grid cell coordinates (easting, northing)
  - Corner coordinates (min/max x and y)
  - Match keys to the arable-area files
- Scenario mapping:
  - 1: Climate tipping point = No; Irrigation = No
  - 2: Climate tipping point = No; Irrigation = Yes
  - 3: Climate tipping point = Yes; Irrigation = No
  - 4: Climate tipping point = Yes; Irrigation = Yes

## Data sources and modeling approach
- Climate driver: UKCP09 HadRM3-PPE-UK projections (HadRM3-PPE-UK) for the 21st Century, using the SRES-A1B medium-emissions framework; bias-corrected against 1960–1989 observations.
- AMOC tipping point: Simulated using HadGEM3 with freshwater hosing to induce collapse; linear weighting during 2030–2050 to represent progressive AMOC weakening; outputs represent seasonal means after the system reaches a quasi-steady state.
- Irrigation: Implemented as grid boxes receiving at least a threshold rainfall, representing the optimal rainfall level for GB arable farming based on historical data.
- Baseline data sources: Land-use inputs from the June Agricultural Census on a 2 km grid (1972–2010).

## Data quality and provenance
- Methodology aligned with Fezzi & Bateman (2011, 2014, 2015) and the UK National Ecosystem Assessment framework; data described as peer-reviewed and validated within the referenced literature.
- Outputs are on a consistent 2 km x 2 km grid (400 ha per cell) across Great Britain.
- Grid-cell matching ensured via grid identifiers and coordinate data; dataset integrates climate, land-use, and scenario assumptions.

## File structure and access details
- Four scenario-specific arable-area CSV files: Ag_model_sc{1..4}.csv
  - Each file includes grid cell identifiers and corresponding arable area in hectares.
- Grid metadata CSV: Ag_model_grid_2km.csv
  - Provides centre coordinates and corner bounds for each grid cell; used to map arable-area values to spatial locations.
- Grid cells are 2 km on a side (400 ha each); arable area per cell ranges up to 400 ha.

## Limitations and considerations
- AMOC collapse representation is idealised and not instantaneous; the speed and linearity are simplifications relative to some climate models.
- Irrigation is represented by a fixed rainfall-threshold proxy; real-world applicability may vary with local practices.
- Climate projections are bias-corrected and model-dependent (HadRM3-PPE-UK; UKCP09); uncertainties inherent to scenario-based projections apply.
- Temporal scope is 2000–2089; data are annualized by grid cell but seasonal aggregation details are described only for climate inputs (seasonal means used in model inputs).

## Implications for data governance and usage
- Clear data lineage: climate projections, AMOC scenario treatment, irrigation proxy, and land-use inputs are explicitly described, supporting reproducibility and auditing.
- Structured, discoverable data products: consistent file naming and explicit grid mapping facilitate integration into broader data systems and policy analyses.
- Suitable for scenario planning and policy evaluation, with attention to underlying assumptions and acknowledged idealisations in the AMOC and irrigation components.
- Documentation references provide traceability to foundational methods and prior work, aiding validation and methodological alignment across teams.