# Supporting documentation

- The dataset combines outputs from two models (JULES and ECO-AG) to explore land use under unmitigated climate change across Great Britain at fine spatial scales.
- Key variables: arable area (ECO-AG), net primary productivity (NPP), runoff, and irrigation demand (JULES).
- Driving climate data come from Regional Climate Model runs for present (1998-2008) and future (11-year period at 2100) under RCP8.5, with CO2 levels of ~386.5 ppm present and ~936 ppm future.
- Eight scenario configurations cover combinations of climate, CO2, and irrigation settings.

## Models and outputs

- JULES (land surface model)
  - Grid resolution: 1.5 km x 1.5 km.
  - Outputs: npp (Net Primary Productivity; kg m-2 s-1), runoff (mm s-1), irrig_water (mm s-1).
  - Data packaging: tar files per scenario; each tar contains 132 files (11 years × 12 months) with monthly grid-wide means and grid coordinates.
  - File naming: {scenario_run}_{variable}_yyyymm.nc
  - NPP indices: 1-5 correspond to broadleaf trees, needleleaf trees, C3 grasses, C4 grasses, shrubs.

- ECO-AG (econometric agricultural land use model)
  - Grid resolution: 2 km x 2 km.
  - Outputs: arable land area per grid cell (hectares; up to 400 ha per cell).
  - Data packaging: per-scenario CSVs named ECO_AG_{scenario_run}.csv; a grid file ECO_AG_grid_2km.csv provides coordinates and cell boundaries.

## Scenarios and driving data

- Eight scenarios combining:
  - ECO-AG baseline, climate present, CO2 No, irrigation No
  - JULES baseline, climate present, CO2 present, irrigation No
  - Climate only (present vs future)
  - Irrigation only (present)
  - Climate & Irrigation
  - Climate & CO2
  - Climate, CO2 & Irrigation
- Climate drivers:
  - Present climate data: 1998-2008
  - Future climate data: 11-year period at 2100
  - Northern and southern GB data blended with a piecewise linear function
  - Present CO2 around 386.5 ppm; future CO2 around 936 ppm (RCP8.5)

## Data structure and formats

- JULES outputs
  - Directory: JULES_output
  - Files: tar archives containing 132 monthly files for 11 years per scenario
  - Variables: npp, runoff, irrig_water
  - File naming format: {scenario_run}_{variable}_yyyymm.nc
  - Present vs future labeled by year offset (future data labeled as 100 years later)

- ECO-AG outputs
  - Directory: ECO_AG_output
  - Files: ECO_AG_{scenario_run}.csv (grid-cell arable area in hectares)
  - Grid coordinates: ECO_AG_grid_2km.csv (grid center coordinates and corners; matches grid_cell_id)

## Data provenance and quality control

- JULES
  - Community-developed model led by UK Met Office and CEH
  - Version: vn4.9; configuration in Rose suite u-ao645, branch 'full_UK'
  - Access: JULES repository (registration required)

- ECO-AG
  - Based on Fezzi & Bateman (2011) methodology; used in UK NEA and follow-on studies
  - Data derived from June Agricultural Census (2 km grid across GB; 1972–2010)

- Documentation and references
  - Supporting methodological papers and UK ecosystem-service literature cited (Bateman et al., Fezzi et al., Kendon et al., NEA reports)

## Access and reuse

- JULES data access: https://code.metoffice.gov.uk/trac/jules (registration required)
- Rose workflow data: https://code.metoffice.gov.uk/trac/roses-u (registration required)

## How data can support analysis

- Enables cross-model comparison of climate, CO2, and irrigation effects on arable land and ecosystem service indicators.
- Facilitates spatially explicit, self-serve analyses of productivity, water balance, and irrigation demand at high resolution.
- Provides baseline and scenario-driven data for policy and planning studies in climate impact on land use.
- Supports incorporation into dashboards or data products for end users interested in regional GB land-use responses to unmitigated climate change.