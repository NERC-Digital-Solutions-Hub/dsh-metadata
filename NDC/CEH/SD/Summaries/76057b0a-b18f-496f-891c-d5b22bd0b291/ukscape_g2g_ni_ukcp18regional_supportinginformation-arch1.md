# Supporting information for: Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080) v2

## Overview
- Presents supporting information for Grid-to-Grid (G2G) hydrological model estimates of NI river flows driven by UKCP18 Regional (12 km) projections.
- Covers data hierarchy, processing steps, dataset contents, formatting, and usage considerations.
- Targets users seeking to analyse or apply climate-driven river-flow projections, including comparisons with observations or future scenarios.

## What is included
- Grid-to-Grid outputs for Northern Ireland on a 1 km x 1 km grid:
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1) with dates
  - Annual minima of 7-day mean river flow (m3 s-1) with dates
- Domain and coverage:
  - Non-tidal river cells with catchment area >= 50 km2
  - NI-focused dataset; includes some flows within lakes (lake storage effects not modelled)
- Ensemble information:
  - 12 PPE ensemble members from the UKCP18 Regional Climate Model
  - Ensemble numbers: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15
- Additional supporting spatial datasets:
  - Digitally-derived catchment areas (1 km grid)
  - Majority lake cells (1 km grid)
  - Estimated NRFA gauging station locations (1 km grid) and CSV

## Model and performance
- Hydrological model: Grid-to-Grid (G2G), 1 km x 1 km grid, 15-minute time-step.
- Coverage includes NI and adjacent Irish catchments draining to NI rivers; aligned with GB national grid.
- Calibration:
  - Generally uses nationally applicable parameter values (not calibrated per catchment)
  - Accounts for urban/suburban runoff via model structure
- Performance notes:
  - Good performance for catchments with natural flow regimes
  - Less accurate where artificial water regulation or complex subsurface hydrology dominates
  - NI-specific assessment shows generally good performance except near Lough Neagh where flood regulation limits observed flows

## Input data and processing
- Meteorological inputs derived from UKCP18 Regional (12 km) projections:
  - Daily precipitation, daily min/max temperature, daily PE (via a MORECS-like method)
- Ensemble and period:
  - 12 PPE members, December 1980 to November 2080, under RCP8.5
  - 360-day calendar used by the RCM; months treated as 30 days in some steps
- Downscaling steps to 1 km:
  - Precipitation: bias-corrected 12 km data downscaled using a 1 km rainfall pattern weighting; temporally downscaled by equal distribution over model steps
  - Potential evapotranspiration: downscaled to 1 km and partitioned across time-steps
  - Temperature: downscaled to 1 km using elevation-based lapse rates; diurnal variation interpolated with a sine curve
- Additional inputs:
  - Topography and soil data aligned with the 1 km grid
- Data availability timing:
  - Monthly mean flows assigned to the first day of each month
  - Annual maxima/minima assigned to the start year of the respective 12-month or Dec–Nov period
- Limitations:
  - No lake storage or reservoir regulation effects included; lakes treated as rivers
  - Some grid cells within lakes produce river-flow values; an extra lake grid map helps identify majority lake cells

## How to use the dataset
- Historical comparisons:
  - Compare G2G outputs driven by UKCP18 with those driven by observation-based input data or NRFA observations for statistical, not point-by-point, assessments
- Change analysis:
  - Compare baseline vs future periods statistically to explore climate-change impacts on river flows
- Ensemble use:
  - Use the same ensemble member for cross-period comparisons (e.g., member 01 baseline vs member 01 future)
- Cautions:
  - Recognize that lake storage and regulation are not modelled; results reflect naturalized river flows
  - When comparing to NRFA or observations, account for timing and meteorological differences between datasets

## Format and access
- Data format: NetCDF4 files, one file per ensemble member and per variable
- File naming conventions:
  - Monthly flows: G2G_NI_mmflow_UKCP18RCM_ ensnum _1980_2080.nc
  - Annual maxima: G2G_NI_amaxflow_UKCP18RCM_ ensnum _1980_2080.nc
  - Annual minima: G2G_NI_aminflow_UKCP18RCM_ ensnum _1980_2080.nc
- Spatial domain:
  - NI domain on GB National Grid, 1 km resolution
  - Non-tidal river cells with catchment area >= 50 km2; missing values (-9999) elsewhere
- Time representation:
  - Time units: days since 1900-01-01
  - 30-day months due to 360-day calendar in climate model data
- Supporting spatial files:
  - CatchmentAreaGrid.nc, LakeGrid.nc, NRFAStationIDGrid.nc, and NRFAStationIDs.csv

## Data access and citation
- License: Open Government Licence v3
- Citation requirement:
  Kay, A.L.; Rudd, A.C.; Davies, H.N.; Lane, R.A.; Bell, V.A. (2022). Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080) v2. NERC EDS Environmental Information Data Centre. Dataset. https://doi.org/10.5285/76057b0a-b18f-496f-891c-d5b22bd0b291

## Acknowledgements and references
- Funded by Natural Environment Research Council under UK-SCAPE National Capability award NE/R016429/1
- Acknowledges contributions from team members and related methodological references (UKCP18, MORECS-based evaporation, high-resolution hydrological modelling, and supporting datasets)

## Key caveats for analysts
- Lakes and reservoirs are not explicitly modelled; downstream flows may omit lake-storage effects
- Calibration is not catchment-specific; ensemble spread reflects climate model uncertainty rather than local parameter tuning
- Direct, point-by-point meteorological equivalence with observations is not expected; use long-term statistical comparisons
- Some catchments or smaller basins may exhibit larger discretisation errors due to 1 km grid resolution
- Ensure consistent ensemble member usage when comparing across periods or scenarios