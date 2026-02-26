# Supporting information for: Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

- Purpose and scope
  - Provides Grid-to-Grid (G2G) hydrological model estimates of monthly mean soil moisture on a 1km x 1km grid across Great Britain (GB) and Northern Ireland (NI), driven by UKCP18 Regional (12km) projections.
  - Part of UK-SCAPE WP2 research on climate change impacts on water quantity; covers December 1980 to November 2080 under RCP 8.5.
  - Includes a 12-member perturbed parameter ensemble (PPE) of the Met Office Hadley Centre Regional Climate Model (RCM).

- What is in the dataset
  - Soil moisture outputs: monthly averages of daily mean soil moisture in the unsaturated zone, expressed as between 0 and 1 (depth-integrated across the soil column).
  - Spatial domain:
    - GB: 1km grid over a 700 km x 1,000 km domain on the GB National Grid.
    - NI: 1km grid over a 187 km x 170 km domain on the GB grid.
  - Temporal format:
    - 30-day months due to a 360-day calendar in the climate model data.
    - Time stamps in NetCDF: days since 1900-01-01; data cover Dec 1980 to Nov 2080.
  - Lake information:
    - Two additional datasets identify majority lake cells for GB and NI to aid interpretation.
    - Lake grid cells are included in the soil moisture outputs; lakes are not modeled with storage effects (treated as rivers for the purpose of the dataset).

- Model details
  - Hydrological model: Grid-to-Grid (G2G), a national-scale model providing gridded soil moisture and river-flow estimates; calibrated with global, not catchment-specific, parameters where possible.
  - Required inputs: daily precipitation, daily potential evapotranspiration (PE), and daily min/max temperatures (for optional snow module).
  - Data processing:
    - Precipitation bias-corrected via monthly multiplicative factors.
    - PE derived with Penman-Monteith using MORECS-like assumptions and adjustments for elevated CO2.
    - 12km RCM data downscaled to 1km using spatial weighting for precipitation, 1km downscaled PE, and elevation-based lapse rate for temperature with diurnal downscaling via a sine curve.
  - Output type: monthly mean soil moisture (m water/m soil), interpreted as volumetric content (0–1) for the unsaturated zone.

- Ensemble and recommended usage
  - 12 PPE ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (note: members 02, 03, and 14 are excluded).
  - For robust comparison across periods, use the same ensemble member for both historical and future periods.
  - Comparisons against observation-based soil moisture are statistical over multi-decadal scales; direct time-point pointwise comparisons are not advised due to inherent non-equivalence of weather features.

- Data formats and file conventions
  - Files: NetCDF4 format, one file per ensemble member, separate for GB and NI.
  - GB file naming: G2G_GB_mmsoil_UKCP18RCM_ensnum_1980_2080.nc
  - NI file naming: G2G_NI_mmsoil_UKCP18RCM_ensnum_1980_2080.nc
  - Lake grid guidance files:
    - UKSCAPE_G2G_GB_SoilMoisture_LakeGrid.nc
    - UKSCAPE_G2G_NI_SoilMoisture_LakeGrid.nc
  - Spatial extents:
    - GB: 700 km x 1,000 km domain coordinates on the GB National Grid (0,0) to (700000,1000000) metres.
    - NI: 187 km x 170 km domain on the GB grid (−7000, 440000) to (180000, 610000) metres.
  - Time conventions:
    - 30-day months; 360-day calendar; first day of each month corresponds to the monthly mean value.
    - Time units: days since 1900-01-01.

- Usage notes and caveats
  - Lake and downstream regulation effects are not modeled; lakes are treated as rivers in terms of their influence on flows, and lake areas can appear as soil-moisture grid cells.
  - No catchment-specific calibration; model parameters are globally applied; natural-flow regimes influence performance (better in natural catchments).
  - Historical comparisons to observation-driven data are possible but should be statistical, not direct time-point matching.

- Related datasets and context
  - Complementary datasets cover river flows for GB and NI and the MaRIUS-G2G-WAH2 dataset (weather@home2 driving data).
  - Acknowledges support from the Natural Environment Research Council (NERC) under award NE/R016429/1 as part of the UK-SCAPE programme.

- Practical guidance for data leaders
  - Use these soil-moisture time series to assess potential climate-change impacts on soil moisture across GB and NI at high spatial resolution.
  - Leverage ensemble spread to quantify uncertainty in projections.
  - Coordinate use with other UK-SCAPE hydrological datasets to build a cohesive view of climate impacts on water quantity and hydrological extremes.