# Supporting information for Grid-to-Grid model estimates of river flow for Great Britain driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Overview
- UK-SCAPE program (five-year, NERC funded) includes Work Package 2 researching climate change impacts on water quantity across Britain.
- Provides Grid-to-Grid (G2G) hydrological model estimates of river flow on a 1 km x 1 km grid across Great Britain, driven by UKCP18 Regional (12 km) projections.
- Outputs include:
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1)
  - Annual minima of 7-day mean river flow (m3 s-1)
- Data cover December 1980 to November 2080 under RCP 8.5, using a 12-member Perturbed Parameter Ensemble (PPE) from the Met Office Hadley Centre Regional Climate Model (RCM).
- A complementary dataset provides G2G estimates driven by observation-based data.
- Two additional spatial datasets are provided: digitally-derived catchment areas on a 1 km grid and estimated locations of flow gauging stations on a 1 km grid with station information.

## G2G model and outputs
- G2G is a national-scale hydrological model operating at 1 km x 1 km grid with a 15-minute time-step.
- Produces spatially-consistent, gridded natural river flows for gauged and ungauged rivers across GB.
- Calibrations are not used to identify catchment-specific parameters; nationally applicable values are used where parameters are required.
- Outputs are provided for non-tidal river cells with catchments ≥ 50 km² and include:
  - Monthly mean flows
  - Annual maxima of daily mean flows
  - Annual minima of 7-day mean flows
  - Dates of occurrence for annual maxima and minima
- Model inputs include precipitation, potential evapotranspiration (PE), and daily min/max temperatures for optional snow module.

## G2G input data and processing
- Meteorological inputs derived from UKCP18 Regional (12 km) projections:
  - Daily precipitation
  - Daily min and max temperature
  - Daily PE (via a scheme linked to MORECS)
- Data prepared as a 12-member PPE for Dec 1980–Nov 2080 under RCP8.5, on native 12 km grid and a 12 km grid aligned with the GB grid.
- Bias correction:
  - Precipitation corrected using a monthly multiplicative bias-correction scheme.
  - PE calculated with Penman-Monteith, incorporating bias-corrected interception.
- Downscaling to 1 km:
  - Precipitation downscaled using a spatial weighting based on 1 km rainfall patterns; temporally downscaled by equally distributing over model time-steps.
  - PE downscaled to 1 km by copying and distributing over time-steps.
  - Temperature downscaled to 1 km using elevation-based lapse rates and temporally downscaled with a sine curve to approximate diurnal variation.
- Input data requirements include precipitation, PE, and daily min/max temperatures; snow module requires daily temperatures.
- Calendar notes: 360-day year used by the climate model; 30-day months are used in the data.

## Data formats and contents
- Gridded outputs on a 1 km x 1 km grid over a 700 km x 1000 km GB domain; grid cell centers represent data points.
- G2G values provided only for non-tidal river cells with catchments ≥ 50 km²; other cells are missing (-9999).
- Time conventions:
  - Monthly mean flows are assigned to the first day of the month.
  - Annual maxima/minima are assigned to the start year of the corresponding 12-month period (water year conventions described).
  - Dates of occurrence provided as days since 1900-01-01.
- NetCDF4 files:
  - Monthly mean river flow: G2G_GB_mmflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual maxima of daily mean river flow: G2G_GB_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual minima of 7-day mean river flow: G2G_GB_aminflow_UKCP18RCM_ensnum_1980_2080.nc
  - ensnum values correspond to ensemble members (01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15)
- Additional datasets to aid use:
  - Catchment area grid for grid cells draining to each 1 km cell: UKSCAPE_G2G_GB_CatchmentAreaGrid.nc
  - Estimated NRFA gauge station locations on the 1 km grid: UKSCAPE_G2G_GB_NRFAStationIDGrid.nc and NRFA station IDs in CSV
- Existing MaRIUS G2G dataset variations are acknowledged; minor model setup changes may exist.

## Ancillary datasets
- Catchment area grid (km²) for each 1 km grid cell.
- NRFA gauge station location grid with station IDs; helps compare G2G estimates with observed flows at gauging stations.
- Additional NRFA stations provided in a CSV file; station codes use 0 for land, -9999 for sea.

## How to use the dataset
- Historical comparisons:
  - Can compare G2G outputs driven by UKCP18 Regional data with those driven by observation-based inputs or observed river flow, but only via statistical comparisons over multi-decadal timescales (not point-by-point time series).
- Ensemble usage:
  - Use the same ensemble member when comparing across different periods (e.g., baseline vs future) to maintain consistency.
- Context and comparability:
  - Outputs are analogous to MaRIUS-G2G-WAH2-monthly data, which used a different climate model input (weather@home).
- Practical applications:
  - Investigate potential climate-change impacts on river flows, including seasonal changes and extremes.
  - Use the 1 km resolution outputs to analyze regional hydrology and to support local decision-making.
- Caution in interpretation:
  - Discrepancies can occur due to the discretisation of river catchments to 1 km grids, particularly for smaller catchments.
  - The G2G model is designed for natural flow regimes; performance may decline where artificial abstractions or complex subsurface hydrology dominate.

## Caveats and limitations
- The 360-day calendar and 30-day months are used in the climate model data, which affects temporal alignment.
- Annual maxima/minima and dates of occurrence are tied to the start of the respective 12-month periods, which may require careful interpretation when aligning with standard hydrological years.
- While checks for NRFA station locations are performed, some derived catchment areas at the 1 km grid may differ from observed NRFA catchments, especially for small basins.
- Comparisons with observed weather features should be statistical rather than point-for-point due to potential mismatches between modelled and observed weather features.

## Acknowledgements and references
- Funded by the Natural Environment Research Council under award NE/R016429/1 as part of the UK-SCAPE programme.
- Acknowledgements to colleagues for advice and to cited references detailing model development, bias correction, downscaling, and validation.