# Supporting documentation

- Dataset containing model outputs from JULES (land surface model) and ECO-AG (economic agricultural land-use model) for Great Britain at kilometre-scale resolution under unmitigated climate change.
- Focuses on eight scenarios exploring the separate and combined effects of climate, CO2, and irrigation on land use indicators.

## Overview and purpose
- Provides high-resolution model outputs to support environmental health monitoring, policy scrutiny, and future decision-making.
- Enables assessment of how climate change, CO2 concentrations, and irrigation affect arable area, vegetation productivity, runoff, and irrigation demand.
- Supports evaluation of policy options by separating the impacts of climate, CO2, and irrigation on land use and ecosystem services.

## Models and driving data
- JULES (land surface model)
  - Outputs at 1.5 km x 1.5 km grid for Great Britain.
  - Variables: net primary productivity (npp), runoff, and irrig_water.
  - Data organized in tar files per variable, with 132 files per tar (11 years of monthly data per grid cell).
  - Present-day climate driven; future climate uses a high-end CO2 scenario.
- ECO-AG (agricultural land-use model)
  - Outputs on a 2 km x 2 km grid over Great Britain.
  - Variable: arable land area (hectares per grid cell).
  - Based on agricultural census data (1972–2010) and ecological-economic modeling approaches.
- Driving climate data
  - Regional Climate Model (RCM) runs at 1.5 km resolution; daily data.
  - Present climate: 1998–2008; future climate: 11-year realizations for the end of the century.
  - CO2 level: future scenario uses about 936 ppm (RCP8.5), present CO2 corresponds to present-day values.
  - ECO-AG scenarios do not incorporate CO2 variations.

## Scenarios and what they isolate
- Eight scenarios exploring combinations of:
  - Climate (present vs future)
  - CO2 (present vs future, though ECO-AG cannot vary CO2)
  - Irrigation (on vs off)
- ECO-AG Climate & Irrigation, ECO-AG Climate only, ECO-AG Irrigation only, JULES Climate only, JULES Irrigation only, JULES Climate & CO2, JULES Climate, CO2 & Irrigation, etc.
- Purpose: disentangle impacts of climate change, CO2 fertilization effects, and irrigation on arable land use and productivity.

## Spatial and temporal coverage
- Spatial: Great Britain, with:
  - JULES outputs on a 1.5 km grid.
  - ECO-AG outputs on a 2 km grid.
  - Grid coordinates provided for matching outputs (ECO_AG_grid_2km.csv with easting/northing and cell extents).
- Temporal: 11-year monthly data blocks for each scenario:
  - Present climate period (1998–2008) and future climate period (end-of-century)
  - File naming reflects whether data are driven by present or future climate (future labeled 100 years later).

## Data structure and access
- JULES_output
  - Tar files for each variable; each tar contains 132 files (11 years × 12 months) with monthly grid-cell means plus coordinates.
  - File naming format: {scenario_run}_{variable}_yyyymm.nc
  - Variables:
    - npp: Net Primary Productivity by plant functional type (broadleaf trees, needleleaf trees, C3/C4 grasses, shrubs)
    - runoff: Runoff rate (mm s-1)
    - irrig_water: Irrigation water demand to alleviate water stress (mm s-1)
- ECO_AG_output
  - CSV files named ECO_AG_{scenario_run}.csv; grid-cell arable area (ha) per 2 km grid.
  - Grid cell coordinates file: ECO_AG_grid_2km.csv (centroids and corners; coordinates for matching data)
- File role and provenance
  - JULES: community-developed UK Met Office and CEH model, version vn4.9 (Rose suite u-ao645)
  - ECO-AG: approach from Fezzi & Bateman (2011) used in UK National Ecosystem Assessment and follow-ons
- Access notes
  - Data and model details referenced in published literature; registration and repository details provided for JULES access.

## Quality, provenance, and references
- JULES is a widely used, community-validated model; access requires registration to the JULES/ROSE repository.
- ECO-AG methodology and data provenance documented in Fezzi et al. and UK NEA follow-ons; input data include the June Agricultural Census and established environmental-economics approaches.
- References include key publications on ecosystem services valuation, land-use modeling, and climate-change impacts on agriculture and water.

## How this supports monitoring and policy evaluation
- Enables policymakers to quantify potential climate-change impacts on arable land and productivity at very high spatial resolution.
- Allows evaluation of how irrigation and CO2 scenarios modify water demand, runoff, and land-use patterns.
- Supports data governance and transparency requirements by providing explicit scenario definitions, grid-level outputs, and links to data sources.
- Highlights data-related challenges relevant to monitoring programs: data availability at suitable resolution, metadata completeness, data transformation needs, and the importance of traceable data provenance.