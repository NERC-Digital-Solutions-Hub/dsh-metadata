# Supporting information for: Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

- Overview
  - UK-SCAPE programme, Phase: Work Package 2, investigates climate change impacts on water quantity across Britain.
  - Provides Grid-to-Grid (G2G) soil moisture estimates on a 1km x 1km grid across Great Britain (GB) and Northern Ireland (NI) using UKCP18 Regional (12km) projections.
  - Data produced from a 12-member perturbed parameter ensemble (PPE) of the Met Office Hadley Centre Regional Climate Model, for 1980–2080 under RCP8.5.
  - A complementary dataset exists for G2G driven by observation-based data; related datasets cover river flows for GB and NI.

- The Grid-to-Grid (G2G) model
  - National-scale hydrological model on a 1km x 1km grid with 15-minute time steps (GB; NI and parts of ROI drain to NI rivers implemented in extended domain).
  - Outputs: spatially consistent gridded estimates of natural river flows and soil moisture.
  - Calibration: uses spatial datasets; no catchment-specific calibration; uses universal parameter values when required (e.g., kinematic wave speeds).
  - Exclusions: lakes, reservoirs, and anthropogenic abstractions/discharges are not represented; lakes are treated as rivers in the model.

- Input data and downscaling
  - Meteorological drivers derived from UKCP18 Regional (12km) projections: daily precipitation, daily min/max temperature, daily potential evapotranspiration (PE).
  - PPE ensemble comprises 12 members; data transformed to a 12km grid aligned with the GB national grid and bias-corrected for precipitation (monthly multiplicative factors).
  - PE calculated via Penman-Monteith with preseason adjustments to account for future CO2 effects on stomatal resistance.
  - Downscaling: 12km data downscaled to 1km using spatial weighting for precipitation, downscaled PE to 1km, and temperature downscaled with elevation-based lapse rates; temporal downscaling by equal distribution over model time-steps.
  - Time conventions: 30-day months, 360-day calendar as per climate model data.

- Model outputs and interpretation
  - Soil moisture output: monthly averages of daily mean soil moisture in the unsaturated zone, expressed as m water/m soil (0–1 depth-integrated).
  - Spatial domain: GB 700 km by 1000 km grid; NI 187 km by 170 km grid, both aligned to the GB national grid; outputs include cells that lie within lakes.
  - Two additional files identify majority lake cells to aid interpretation of the moistures in water bodies.

- Data formats and file naming
  - Gridded data stored as NetCDF4, one file per ensemble member, separate for GB and NI.
  - GB file name: G2G_GB_mmsoil_UKCP18RCM_ensnum_1980_2080.nc
  - NI file name: G2G_NI_mmsoil_UKCP18RCM_ensnum_1980_2080.nc
  - Ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15
  - Lake grid files: UKSCAPE_G2G_GB_SoilMoisture_LakeGrid.nc; UKSCAPE_G2G_NI_SoilMoisture_LakeGrid.nc
  - Lake grid convention: land=1, lake=2, sea=-9999; lake cells identified where >85% area is water (based on Land Cover Map 2015).

- Usage guidance
  - Historic comparisons: G2G soil moisture driven by UKCP18 can be compared qualitatively to those driven by observation-based input data; statistical, not point-by-point, comparisons are recommended due to non-identical weather features.
  - Baseline vs future: use statistical comparisons over multi-decadal periods to explore climate-change impacts on soil moisture; use the same ensemble member across periods.
  - Lake effects: outputs in lake cells are not representative of lake storage effects; interpret lake-adjacent values with caution.
  - Ensemble considerations: comparisons across periods should pair identical ensemble members (e.g., member 01 baseline with member 01 future).

- Related context and references
  - Relation to MaRIUS-G2G-WAH2 monthly soil moisture data (climate-model-derived) as a methodological analogue.
  - Acknowledges limitations in representing lakes, reservoirs, and anthropogenic water management within G2G.
  - Supported by NERC award NE/R016429/1 as part of UK-SCAPE National Capability.

- Acknowledgements and references
  - Acknowledgement of support from Natural Environment Research Council (NERC NE/R016429/1).
  - Key methodological references include Bell et al. (2009, 2007, 2016, 2018), Kay et al. (2021a, 2021b), Guillod et al. (2017, 2018), Monteith (1965), Hough and Jones (1997), among others.