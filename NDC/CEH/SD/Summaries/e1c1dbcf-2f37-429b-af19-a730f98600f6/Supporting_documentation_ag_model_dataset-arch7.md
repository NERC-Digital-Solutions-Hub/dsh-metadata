# Supporting documentation

## Overview
- Datasets contain model outputs from an agricultural land use model for Great Britain (GB) at a 2 km x 2 km grid, covering 2000–2089.
- Four scenarios combine climate pathway (standard climate change vs AMOC collapse tipping point) with irrigation availability (no irrigation vs widespread irrigation).
- Target variable: arable land area per grid cell (hectares), up to 400 ha per cell.
- Data are designed for map-based GIS analyses and spatial visualization of land-use responses to climate and irrigation changes.

## Background
- Climate driving data: Met Office Hadley Centre Regional Model Perturbed Physics Ensemble simulations for UK domain (HadRM3-PPE-UK; UKCP09, 2014), at 25 km x 25 km resolution, bias-corrected to align with observed data (1960–1989).
- AMOC tipping point: derived from HadGEM3 model with a progressive AMOC collapse (years 2030–2050) using a linear weighting function; climate variables used are seasonal means (April–September) averaged over 30-year steady-state periods.
- Irrigation scenario: implemented as grid boxes receiving at least a threshold rainfall corresponding to historically optimal GB arable farming conditions.
- Quality control framework follows Fezzi & Bateman (2011) and related UK NEA work; data originate from the June Agricultural Census on a 2 km grid across GB for years 1972–2010.

## Data structure and content
- Four scenario-specific CSV files: Ag_model_sc{scenario #}.csv, each containing:
  - A unique grid cell identifier
  - Arable land area per grid cell (hectares; maximum 400 ha)
- Grid coordinate file: Ag_model_grid_2km.csv, providing:
  - Easting and northing coordinates (cell center)
  - Corner coordinates (min/max x and y)
  - Matching to the grid cell identifiers used in the arable land CSV files
- Scenario mapping:
  - 1: Climate tipping point = No; Irrigation = No
  - 2: Climate tipping point = No; Irrigation = Yes
  - 3: Climate tipping point = Yes; Irrigation = No
  - 4: Climate tipping point = Yes; Irrigation = Yes

## Data sources and references
- UK climate projections and related climate data:
  - UKCP09, Met Office Hadley Centre; HadRM3-PPE-UK
  - HadGEM3 model outputs for AMOC collapse scenarios
- Land-use and ecosystem context:
  - Fezzi & Bateman (2011, 2014, 2015); UK National Ecosystem Assessment and follow-ons
  - Bateman et al. (2013, 2014)
  - UK agricultural census data (for GB land-use baseline)
- Additional methodology and validation:
  - Jenkis (2009); Safta et al. (2015); Mecking et al. (2016); Jackson et al. (2015)

## Spatial scope and resolution
- Geography: Great Britain (GB)
- Spatial resolution: 2 km x 2 km grid (400 hectares per cell)
- Temporal coverage: 2000–2089 for arable land; climate inputs span 1950–2100 with bias correction applied

## Usage notes for GIS analysts
- Data are provided as CSV with a separate coordinate file; join both datasets on the grid cell identifier.
- The 2 km grid can be used to produce map-based visualizations of arable area under each scenario.
- Consider the assumptions and limitations:
  - AMOC collapse modeled with a linear weighting over 2030–2050; actual dynamics may differ.
  - Irrigation scenario relies on a rainfall threshold derived from historical GB data.
  - Bias correction and model chaining introduce uncertainties; refer to the cited validation studies.
- Useful for policy analysis, impact assessment, and spatial decision-making related to climate and irrigation policy.

## Related concepts and context
- Links to ecosystem service valuation, climate adaptation impacts on land use, and spatial agro-environmental policy analysis as described in the referenced literature.