# Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by UKCP18 Regional (12km) data (1980 to 2080)

## Overview
- UK-SCAPE WP2 project provides Grid-to-Grid (G2G) hydrological model outputs for monthly mean soil moisture (m water per m soil) on a 1km x 1km grid across Great Britain (GB) and Northern Ireland (NI), driven by UKCP18 Regional (12km) projections.
- Data cover December 1980 to November 2080 under RCP8.5 and use a 12-member perturbed parameter ensemble (PPE) of the Hadley Centre Regional Climate Model (RCM).
- Includes a complementary dataset driven by observation-based input data and links to related datasets for river flows (GB and NI).
- Two additional spatial datasets identify majority lake cells to aid interpretation.

## Data and scope
- Spatial coverage: GB 1km grid (GB domain 700 km x 1000 km) and NI grid (187 km x 170 km on the GB National Grid); includes lake cells and areas fully covered by lakes.
- Temporal coverage: 1980-12 to 2080-11; 30-day months due to 360-day calendar in the climate model.
- Output: monthly mean soil moisture in unsaturated zone (m water/m soil), interpreted as depth-integrated soil moisture (0 ≤ θ ≤ 1).
- Ensemble members: 12 PPE members (01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15). Do not mix different members between baseline and future periods.

## Hydrological model (Grid-to-Grid, G2G)
- G2G is a national-scale, grid-based hydrological model providing spatially consistent gridded estimates of natural river flows and soil moisture.
- Operates on a 1km grid (GB) with 15-minute time steps; extended to NI and sub-catchments draining to NI rivers.
- Calibration: uses nationally applicable parameter values; relies on land cover to represent urban runoff; does not account for lakes/reservoirs or anthropogenic abstractions/discharges in the river network.
- Performance: robust for natural-flow regimes; less accurate where artificial regulation or complex sub-surface hydrology dominates.

## Input data and processing
- Meteorological inputs from UKCP18 Regional (12km): daily precipitation, daily min/max temperature, and daily potential evapotranspiration (PE) derived via a MORECS-like method.
- Data processed on native 12km grid and transformed to 12km aligned with GB grid; then downscaled to 1km:
  - Precipitation: bias-corrected monthly factors, downscaled spatially using 1km annual rainfall patterns; temporally downscaled by dividing over model time-steps.
  - PE: downscaled to 1km and temporally distributed across time-steps.
  - Temperature: downscaled to 1km using elevation-based lapse rates and sine-curved diurnal variation.
- Snow module: uses daily min/max temperature; optional, but included as part of input data.
- Atmospheric and soil data: grounded in established UKCEH/Bell et al. methodologies.

## Format of the gridded datasets
- Data stored as NetCDF4 files, one file per ensemble member, separately for GB and NI.
- File naming:
  - GB: G2G_GB_mmsoil_UKCP18RCM_ensnum_1980_2080.nc
  - NI: G2G_NI_mmsoil_UKCP18RCM_ensnum_1980_2080.nc
- Time and space specifics:
  - 30-day months; calendar is 360-day.
  - Soil moisture values correspond to the first day of each month.
  - GB domain: 700 km x 1000 km; NI domain: 187 km x 170 km on GB National Grid.
- Lake information:
  - Two lake grid files identify majority lake cells to aid interpretation.
  - Lake cells may contain soil moisture values, treated as though they were rivers for the purposes of the dataset.

## How to use the dataset
- Historical comparisons: G2G soil moisture driven by UKCP18 can be compared statistically to observations-driven outputs (1980-2011) but not point-for-point; use multi-decadal statistics for comparisons.
- Baseline vs future: statistically compare baseline and future periods to assess climate-change impacts on soil moisture.
- Lake and downstream effects: note that lake storage and regulation are not modeled; lakes are treated as rivers in the grid, and some soil moisture values may appear in lake cells.
- Ensemble usage: maintain the same ensemble member when comparing across periods (e.g., member 01 baseline with member 01 future).
- Related datasets: analogous to MaRIUS-G2G-WAH2 monthly soil moisture data (driven by weather@home2), and related river-flow datasets for GB and NI.

## Acknowledgements and references
- Funded by the Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme.
- Key references include foundational G2G development and UKCP18 data processing methods, bias correction, and downscaling approaches (Bell et al., Kay et al., Rudd et al., Guillod et al., Robinson et al., and others listed in the dataset documentation).