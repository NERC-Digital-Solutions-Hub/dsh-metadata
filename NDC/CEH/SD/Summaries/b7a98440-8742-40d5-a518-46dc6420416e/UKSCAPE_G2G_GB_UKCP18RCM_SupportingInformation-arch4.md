# Grid-to-Grid model estimates of river flow for Great Britain driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

- Overview
  - UK-SCAPE programme (UK Status, Change And Projections of the Environment) investigates climate change impacts on water quantity (river flow) across Britain.
  - Provides Grid-to-Grid (G2G) hydrological model outputs for Great Britain on a 1km × 1km grid, driven by UKCP18 Regional (12km) climate projections.
  - Time period: December 1980 to November 2080 under RCP 8.5; analysis uses a 12-member perturbed parameter ensemble (PPE) of the Hadley Centre Regional Climate Model.
  - Outputs support assessment of climate change impacts on river flows and serve as a basis for statistical comparisons to observe-based data or other model-driven datasets.

- What the dataset contains
  - Gridded river-flow time-series at 1km × 1km resolution for non-tidal rivers with catchment area ≥ 50 km².
  - Variables provided:
    - Monthly mean river flow (m³ s⁻¹)
    - Annual maxima of daily mean river flow (m³ s⁻¹) with dates of occurrence
    - Annual minima of 7-day mean river flow (m³ s⁻¹) with dates of occurrence
  - Coverage: all GB (excluding tidal areas) on a 700 km × 1000 km spatial domain; the time series use 30-day months due to the climate model calendar.
  - Data are organized by ensemble member and variable, stored as NetCDF4 files.

- Grid-to-Grid model and inputs
  - Model: Grid-to-Grid (G2G), a nationwide hydrological model that emphasizes spatial consistency and uses national-scale parameters when possible.
  - Inputs:
    - Meteorological inputs derived from UKCP18 Regional (12km) projections: daily precipitation, daily min/max temperature, and potential evapotranspiration (PE) derived via methods aligning with MORECS.
    - 12 PPE members on a 12km grid transformed to a 1km grid using downscaling methods (spatial weighting, temporal downscaling).
    - Precipitation bias correction applied (monthly multiplicative factors).
  - Snow module: uses daily min/max temperatures; optional snow-related calculations included.
  - Output units: river flow in m³ s⁻¹; monthly means and annual extreme values (with occurrence dates).

- Data products and formats
  - NetCDF4 format files, one file per ensemble member and per variable.
  - File naming conventions:
    - Monthly mean flow: G2G_GB_mmflow_UKCP18RCM_ensnum_1980_2080.nc
    - Annual maxima (with dates): G2G_GB_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
    - Annual minima (with dates): G2G_GB_aminflow_UKCP18RCM_ensnum_1980_2080.nc
  - Ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (02, 03, 14 excluded).
  - Spatial domain: 700 km × 1000 km GB National Grid; grid cells represent the centre of each 1km × 1km cell.
  - Valid data: non-tidal river cells with catchment area ≥ 50 km²; other cells set to missing (-9999).
  - Timekeeping: calendar uses 360-day year; time stamps in days since 1900-01-01; monthly mean flows assigned to the first day of each month; annual maxima/minima assigned to the start year of the corresponding 12-month period (water year or Dec–Nov year as specified).
  - Ancillary datasets included to aid use:
    - Digitally-derived catchment area (km²) draining to each 1km grid cell.
    - Estimated locations of NRFA river-flow gauging stations on the 1km grid, with station IDs and mapping to gauging stations.

- Ancillary and validation datasets
  - Validation/interpretation assistance datasets:
    - Flow gauging station locations aligned with NRFA stations to facilitate comparison with observed river flows.
    - Catchment-area grid to understand drainage attribution at the 1km scale.
  - These accompany the primary G2G outputs and support cross-dataset validation and interpretation.

- How to use the dataset
  - Historical comparisons:
    - Compare G2G outputs driven by UKCP18 Regional data with those driven by observation-based inputs or observed river flows for statistical patterns over multi-decadal periods (not pointwise comparisons due to differing weather realizations).
  - Baseline vs. future comparisons:
    - Statistically assess potential climate-change impacts on river flows across baseline and future periods, using consistent ensemble members (e.g., same PPE member for both periods).
  - Ensemble considerations:
    - Use the same ensemble member across periods (e.g., 01 for baseline and 01 for future) to ensure coherent comparisons.
  - Comparison caveats:
    - Do not perform exact time-by-time point comparisons with observed weather features; differences in the driving climate model PPE mean that only statistical, long-term comparisons are appropriate.
  - Relation to other datasets:
    - Future flow estimates are analogous to MaRIUS-G2G-WAH2-monthly datasets and are designed to support studies of drought risk and hydrological responses to climate change.

- Data quality, limitations, and caveats
  - G2G calibration uses nationally-applicable parameters rather than catchment-specific calibrations; performance is strongest in natural-flow regimes and where sub-surface hydrology is not unusually complex.
  - Model limitations in areas with significant artificial abstractions or discharges and in complex catchments.
  - Spatial discretisation to 1km can introduce errors for smaller catchments; caution in interpreting catchment-specific results for small basins.
  - Outputs are monthly means and annual extrema, not continuous daily flows; temporal downscaling and bias corrections introduce uncertainties.

- Access, provenance, and acknowledgements
  - Data are published in the NERC Environmental Information Data Centre (EIDC) under a dataset DOI; part of the UK-SCAPE programme funded by the Natural Environment Research Council (NERC).
  - Acknowledges contributions from researchers and support staff; references provided for model development, bias correction, and validation approaches.

- References (selected)
  - Key methodological and validation sources related to G2G, UKCP18 driving data, bias correction, and prior MaRIUS work (list includes Bell, Kay, Davies, Rudd, and others; specific citations provided in the dataset documentation).