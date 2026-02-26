# Supporting information for: Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Overview
- UK-SCAPE program under NERC; Work Package 2 investigates climate change impacts on water quantity across Britain.
- Provides Grid-to-Grid (G2G) hydrological model outputs of monthly mean soil moisture (m water / m soil) on a 1 km x 1 km grid across Great Britain (GB) and Northern Ireland (NI).
- Datasets are driven by UKCP18 Regional (12 km) projections, using a 12-member perturbed parameter ensemble (PPE) of the Met Office Hadley Centre Regional Climate Model (RCM), covering Dec 1980 to Nov 2080 under RCP8.5.
- Related datasets exist for observed data (soil moisture), river flows, and NI-specific flows; two additional spatial datasets identify majority lake cells.
- Emphasizes data governance by providing clear provenance, format, and usage notes to aid discovery and reuse.

## Model and inputs
- Model: Grid-to-Grid (G2G) is a national-scale hydrological model, typically on 1 km x 1 km grid with 15-minute timesteps; outputs natural river flows and soil moisture. Calibration is applied via globally applicable parameters rather than catchment-specific calibration.
- Spatial scope: GB grid aligned with GB national grid; NI and some Irish sub-catchments draining to NI rivers also included.
- Limitations: Does not account for lakes, reservoirs, abstractions, or downstream water regulation; lakes are treated as rivers in the soil moisture grid.

- Required inputs:
  - Precipitation and potential evapotranspiration (PE) time-series; daily min and max temperature for optional snow module.
  - Input data are bias-corrected (monthly multiplicative factors for precipitation) and downscaled to 1 km; PE downscaled to 1 km.
  - PE calculation uses Penman-Monteith with adjustments for future stomatal resistance due to CO2.

- Data processing:
  - 12 km RCM PPE precipitation downscaled to 1 km using spatial weighting; temporal downscaling distributes monthly factors across model time-steps.
  - 12 km RCM daily PE downscaled to 1 km; temperature downscaled with elevation-based lapse rates and daily sine-curves for diurnal variation.
  - Topography and soil data follow Bell et al. (2009) conventions.

## Data content and format
- Gridded data format:
  - NetCDF4 files, one per ensemble member, separate for GB and NI.
  - Time period: Dec 1980 – Nov 2080; 30-day months due to the model’s 360-day calendar.
  - Spatial domain:
    - GB: 700 km x 1000 km on the GB National Grid (0,0 to 700000,1000000 meters).
    - NI: 187 km x 170 km on the GB grid (−7000, 440000 to 180000, 610000 meters).
- Variable: monthly mean soil moisture in the unsaturated zone (m water / m soil), equivalent to volumetric soil moisture θ (0–1). These are depth-integrated over the soil column.

- Lake-related data:
  - Two additional grid files identify majority lake cells (≥85% water) to aid interpretation.
  - Lakes are included in the soil moisture grids; the lake grid files encode land, lake, and sea.

- Ensemble members:
  - PPE member numbers: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (02, 03, 14 omitted).
  - For comparisons across periods, use the same ensemble member for both baseline and future periods.

- File naming conventions:
  - GB: G2G_GB_mmsoil_UKCP18RCM_ensnum_1980_2080.nc
  - NI: G2G_NI_mmsoil_UKCP18RCM_ensnum_1980_2080.nc
  - ensnum corresponds to the PPE ensemble member (01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15)

- Documentation and conventions:
  - NetCDF4 format; days since 1900-01-01 with first day of each month assigned to monthly mean values.
  - Time dimension uses 30-day months due to the 360-day calendar of the climate model data.
  - Lake grids provided to aid interpretation; lake areas may influence downstream flow is not modeled.

## Usage and interpretation
- Historical vs observational comparisons:
  - Compare G2G soil moisture driven by UKCP18 Regional data with those driven by observation-based input data statistically (not point-by-point); multi-decadal statistics are appropriate, not direct time-matching year-for-year comparisons.
- Baseline and future comparisons:
  - Use the same ensemble member to compare baseline and future periods; assess climate-change impacts on soil moisture through multi-ensemble statistics.
  - Data are analogous to MaRIUS-G2G-WAH2 datasets that used weather@home climate model inputs.

- Limitations and caveats:
  - Lakes, reservoirs, and water storage effects are not represented in the hydrological routing; lakes are treated as rivers in the data.
  - Soil moisture values are depth-integrated across the soil column; interpretation should consider variability in soil depth and properties.
  - The model emphasizes spatial consistency over catchment-specific calibration.

## Data governance and provenance
- Provenance:
  - Generated within the UK-SCAPE program under NERC, using UKCP18 Regional (12 km) projections and PPEs.
- Format and access:
  - Data are stored as NetCDF4 per ensemble member; GB and NI are stored separately.
  - Documentation includes detailed file naming conventions, spatial extents, and calendar specifics to support reproducibility and discovery.
- Related datasets and references:
  - Closely related datasets include observed-data-driven soil moisture, river flows for GB and NI, and lake-grid identifiers.
  - Key references include Bell et al. (2009, 2007, 2016), Kay et al. (2021a, 2021b), Guillod et al. (2017, 2018), and Met Office UKCP18 documentation.

## Acknowledgments and references
- Supported by Natural Environment Research Council award NE/R016429/1 as part of the UK-SCAPE programme.
- References to methodology and data sources for G2G, bias correction, PE calculation, and downscaling are provided within the dataset documentation.