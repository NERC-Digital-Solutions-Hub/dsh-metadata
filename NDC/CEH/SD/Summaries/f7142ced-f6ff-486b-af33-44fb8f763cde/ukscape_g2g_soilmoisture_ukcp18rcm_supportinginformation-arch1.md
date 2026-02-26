# Supporting information for: Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Overview
- UK-SCAPE programme, Work Package 2, investigates climate-change impacts on water quantity.
- Grid-to-Grid (G2G) provides monthly mean soil moisture on a 1km x 1km grid across Great Britain (GB) and Northern Ireland (NI), driven by UKCP18 Regional (12km) projections.
- Data are generated for a 12-member perturbed parameter ensemble (PPE) of the Met Office Hadley Centre Regional Climate Model, covering December 1980 to November 2080 under RCP 8.5.
- A complementary dataset uses observation-based input data; related datasets exist for river flows (GB and NI).
- Two additional spatial datasets identify majority lake cells for GB and NI.

## Hydrological model (Grid-to-Grid)
- G2G is a national-scale hydrological model on a 1km x 1km grid with a 15-minute time-step, extended to NI and certain ROI sub-catchments draining to NI rivers.
- Outputs include spatially consistent gridded estimates of natural river flows and soil moisture.
- Model calibration is not used for individual catchments; parameters are nationally applied (e.g., lateral routing).
- Urban/suburban land-cover effects are included; lakes, reservoirs, abstractions, and discharges are not simulated.
- Model performance is better for naturally flowing catchments with accurate flow records; performance declines with artificial regulation or complex sub-surface hydrology.

## Input data and processing
- Meteorological inputs come from UKCP18 Regional (12km) projections: daily precipitation, daily min/max temperature, and daily potential evapotranspiration (PE) derived from other variables.
- Data include 12 PPE members, 1980–2080, on native grid and downscaled to 12km GB grid; used here on the GB grid.
- Bias correction: monthly multiplicative factors applied to precipitation.
- PE calculated with Penman-Monteith, aligned with MORECS-like methodology; stomatal resistance adjusted for CO2 in future years.
- Spatial downscaling: 12km daily precipitation downscaled to 1km via spatial weights; daily PE downscaled to 1km; temperature downscaled using elevation-based lapse rates and daily sine curves for diurnal cycles.
- Timekeeping uses a 360-day calendar in the climate model data.

## Soil moisture output and interpretation
- Output is monthly averages of daily mean soil moisture in the unsaturated zone, expressed as m water per m soil (θ, 0 to 1).
- Values are depth-integrated across the soil column and apply to all non-sea 1km grid boxes, including lake cells.
- Lake grids are provided to distinguish land vs. lake cells in the domain.

## Data structure and access
- Gridded data are stored as NetCDF4 files, one per ensemble member, separately for GB and NI.
- File naming: G2G_GB_mmsoil_UKCP18RCM_ensnum_1980_2080.nc (GB) and G2G_NI_mmsoil_UKCP18RCM_ensnum_1980_2080.nc (NI).
- Ensemble members included: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (02, 03, 14 are excluded).
- GB domain: 700 km x 1000 km grid on the GB National Grid; NI domain: 187 km x 170 km on the GB grid.
- Time resolution: 30-day months; time stamps are days since 1900-01-01; monthly mean soil moisture assigned to the first day of each month.
- Lake grids: UKSCAPE_G2G_GB_SoilMoisture_LakeGrid.nc and UKSCAPE_G2G_NI_SoilMoisture_LakeGrid.nc, indicating land vs lake cells (1 = land, 2 = lake, -9999 = sea).

## How to use and limitations
- Historical period comparisons to observation-based data should be statistical (not point-by-point) due to non-equivalence of weather features between observed data and the climate model, especially across multi-decadal timescales.
- Baseline vs. future comparisons should also be statistical to assess climate-change impacts on soil moisture.
- Lakes and reservoirs are not modeled for their storage or regulation effects; lake cells are treated as rivers by the dataset.
- Use the same ensemble member across periods when comparing, e.g., baseline and future (avoid mixing members).
- These soil moisture series are analogous to MaRIUS-G2G-WAH2 monthly soil moisture data, but driven by different climate model data.

## Acknowledgements and references
- Funded by Natural Environment Research Council, award NE/R016429/1, as part of the UK-SCAPE programme.
- Key references include works by Bell, Kay, Davies, Lane, Rudd, and others detailing the G2G model, UKCP18 inputs, and related hydrological studies.