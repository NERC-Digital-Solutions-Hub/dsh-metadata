# Supporting information for Grid-to-Grid model estimates of river flow for Great Britain driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Overview
- UK-SCAPE WP2 dataset providing Grid-to-Grid (G2G) river flow estimates across Great Britain on a 1km × 1km grid, driven by UKCP18 Regional (12km) projections.
- Time period: December 1980 to November 2080, under RCP8.5.
- 12-member perturbed parameter ensemble (PPE) from the Met Office Hadley Centre Regional Climate Model (RCM).
- Outputs cover non-tidal, non-sea grid cells with catchment area ≥ 50 km².
- Two accompanying spatial datasets: digitally-derived catchment areas and estimated NRFA gauging station locations (both on a 1km grid).

## What is included
- Hydrological model estimates produced by G2G for Britain:
  - Monthly mean river flow (m³ s⁻¹)
  - Annual maxima of daily mean river flow (m³ s⁻¹)
  - Annual minima of 7-day mean river flow (m³ s⁻¹)
- Outputs are provided on a 1km × 1km grid across GB for every non-tidal grid cell meeting the catchment threshold.
- For each metric, data are available for each ensemble member and include the dates of occurrence for the annual maxima and minima.
- Additional dataset identifying the 1km grid cell that best represents each NRFA gauging station location (along with a CSV containing station information).

## Model and driving data
- Hydrological model: Grid-to-Grid (G2G)
  - National-scale, grid-based model (1km × 1km, 15-minute time-step) producing spatially consistent river flow estimates for gauged and ungauged rivers.
  - Uses spatial datasets rather than catchment-specific calibration; where parameters are needed (e.g., kinematic wave speeds), nationally applicable values are used.
  - Accounts for urban/suburban land cover effects on runoff and downstream flows.
- Input data requirements:
  - Precipitation and potential evapotranspiration (PE) time-series, plus daily min/max temperatures (for optional snow module).
  - Driving data: UKCP18 Regional (12km) projections, 12 PPE members, 1980–2080, RCP8.5.
- Data processing and downscaling:
  - Precipitation bias-corrected with monthly multiplicative factors.
  - Potential evapotranspiration derived via Penman-Monteith (with MORECS-based stomatal resistance adjustments for future CO₂).
  - 12km RCM data downscaled to 1km:
    - Daily precipitation downscaled using a spatial weighting based on 1km rainfall patterns; temporally downscaled by equal division across model time-steps.
    - Daily PE copied to 1km grid and divided across time-steps.
    - Daily min/max temperatures downscaled to 1km using elevation-based lapse rates; temporal downscaling via a sine curve within the day.
- Temporal and spatial specifics:
  - Model domain aligned with the GB National Grid, 700 km × 1000 km, coordinates from (0,0) to (700000,1000000) metres.
  - 1km × 1km grid cells represent the centre of each pixel.
  - Calendar is 360-day (12 months × 30 days) per model input; monthly data therefore reflect 30-day months.
  - Time stamps in NetCDF: days since 1900-01-01; monthly mean flows assigned to the first day of the month; maxima/minima assigned to the start year of the 12-month period (water year interpretation provided).
- Model outputs and quality:
  - G2G focuses on natural river flows; performance is best in natural-flow regimes and where observational weather features align with model inputs.
  - Outputs are suitable for statistical comparisons across periods and ensembles rather than point-by-point observational comparisons.

## Data format and file naming
- Data files are in NetCDF4 format, one file per ensemble member and per variable.
- File naming conventions:
  - Monthly mean river flow: G2G_GB_mmflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual maxima of daily mean river flow: G2G_GB_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual minima of 7-day mean river flow: G2G_GB_aminflow_UKCP18RCM_ensnum_1980_2080.nc
- Ensemble members are labeled: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (02, 03, 14 omitted).
- Temporal and spatial metadata:
  - Domain covers 700 km × 1000 km on the GB National Grid; 1km grid cells with centre coordinates as grid references.
  - Data provided for non-tidal river cells with catchment area ≥ 50 km²; missing data coded as -9999 elsewhere.
  - Time stamps use a 30-day month convention; date of occurrence for extrema supplied in separate variables (days since 1900-01-01).

## Data coverage and ancillary datasets
- Catchment area data: UKSCAPE_G2G_GB_CatchmentAreaGrid.nc (km² per 1km grid cell).
- NRFA gauging station locations: UKSCAPE_G2G_GB_NRFAStationIDGrid.nc (grid-based station IDs) and NRFAStationIDs.csv (station details).
  - Grid identifies best 1km cell representations for 1038 NRFA gauging stations; 0 indicates land, -9999 sea, positive values the NRFA station numbers.
  - Additional 18 stations included in the CSV, sharing grid cells with existing NRFA stations.

## How to use the dataset
- Comparisons:
  - For historical baselines, compare G2G outputs driven by UKCP18 Regional data with those driven by observation-based inputs or observed river flows; perform statistical (multi-decadal) comparisons rather than point-by-point time series matching.
  - Use the same ensemble member when comparing baseline and future periods to maintain consistency.
  - The UKCP18-driven G2G outputs can be used to assess potential climate-change impacts on river flows via statistical analyses across ensemble members and periods.
- Relationship to other datasets:
  - Outputs are analogous to MaRIUS-G2G-WAH2-monthly datasets (driven by weather@home data), enabling cross-dataset context.

## Limitations and caveats
- Calibration style:
  - G2G uses globally applicable parameter values rather than catchment-specific calibration; may be less accurate in regulated or highly anthropogenically influenced basins.
- Spatial resolution and discretisation:
  - Although at 1km resolution, some small catchments may have catchment areas in the 50–100 km² range, introducing potential discretisation-related errors.
- Observational vs model comparisons:
  - Direct time-point equality between observed weather features and PPE realizations is not expected; use long-tail statistical comparisons over multi-decadal periods.
- Calendar and time conventions:
  - 360-day year and 30-day months may affect interpretation of monthly aggregations and event timing relative to real-world calendars.

## Acknowledgements and references
- Supported by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme.
- References include foundational G2G and UKCP18 literature detailing model development, data processing, and prior applications (e.g., Bell et al., Kay et al., Rudd et al., Guillod et al., and others).