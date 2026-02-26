# Supporting information for: Grid-to-Grid model estimates of river flow for Great Britain driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Purpose and scope
- Provides Grid-to-Grid (G2G) hydrological model outputs of river flow for Great Britain on a 1km x 1km grid.
- Driven by UKCP18 Regional (12km) data over 1980–2080 under RCP8.5; a 12-member perturbed parameter ensemble (PPE).
- Outputs include monthly mean river flow, annual maxima of daily mean river flow, and annual minima of 7-day mean river flow.
- Data are designed to support comparisons with observations or other climate-driven scenarios at multi-decadal scales; not designed for point-by-point weather-to-flow comparisons.

## What is provided
- Gridded river-flow time series for Great Britain on a 1km grid:
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1); dates of occurrence
  - Annual minima of 7-day mean river flow (m3 s-1); dates of occurrence
- Driven by UKCP18 Regional (12km) projections using a 12-member PPE under RCP8.5.
- Coverage includes both historical-driven (UKCP18) data and baseline/future periods for climate-change impact assessment.
- A complementary dataset exists for flows driven by observation-based input data (not included for Northern Ireland here; NI data will be provided separately).
- Additional spatial datasets:
  - Digitally-derived catchment areas on a 1km grid
  - Estimated locations of flow gauging stations on the 1km grid (NRFA stations), with station information in a CSV

## Model and inputs (Grid-to-Grid, G2G)
- G2G is a national-scale hydrological model run on a 1km x 1km grid with a 15-minute time-step.
- Outputs are spatially consistent gridded estimates of natural river flows for gauged and ungauged rivers; calibration is not catchment-specific.
- Inputs:
  - Precipitation and potential evaporation (PE) time-series
  - Daily minimum and maximum temperature (for optional snow module)
- Key processing steps:
  - Precipitation bias correction (monthly multiplicative factors)
  - PE estimated via Penman-Monteith (tuned to replicate MORECS)
  - PE values downscaled to 1km; precipitation downscaled both spatially and temporally
  - Temperature downscaled to 1km using elevation-based lapse rates and a diurnal sine curve
- Domain and data inclusion:
  - Non-tidal river cells with catchment area ≥ 50 km²
  - 1km grid cells; missing values (-9999) elsewhere
  - 360-day calendar in climate model input (30-day months)

## Data format and file structure
- NetCDF4 files, one per ensemble member and per variable:
  - Monthly mean river flow: G2G_GB_mmflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual maxima of daily mean river flow: G2G_GB_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
  - Annual minima of 7-day mean river flow: G2G_GB_aminflow_UKCP18RCM_ensnum_1980_2080.nc
- Window and domain:
  - 700 km x 1000 km GB spatial domain on the GB National Grid
  - Each grid cell represents the centre of the 1km x 1km cell
  - Time stamps use days since 1900-01-01; monthly data nominally assigned to the first day of the month; annual maxima/minima assigned to the start year of the respective 12-month period
  - 30-day months due to the 360-day calendar
- Ensemble members:
  - 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15
- Supporting spatial datasets:
  - UKSCAPE_G2G_GB_CatchmentAreaGrid.nc (catchment area in km² per 1km grid cell)
  - UKSCAPE_G2G_GB_NRFAStationIDGrid.nc (estimated NRFA station IDs per 1km grid cell; station details in CSV)

## Ensemble, baselines, and comparisons
- Ensemble members correspond to the driving PPE member from the underlying climate model; consistent ensemble membership should be used when comparing baseline and future periods.
- Comparable with MaRIUS-G2G-WAH2-monthly datasets (driven by different climate model data but analogous structure and purpose).
- Comparisons:
  - Historical period: statistical comparisons (not point-by-point) between UKCP18-driven G2G outputs and observation-based inputs or observed river flow over multi-decadal periods.
  - Baseline vs future periods: statistical assessments of potential climate-change impacts on river flows.

## How to use the data
- Use for detecting broad patterns and correlations in river-flow responses to climate drivers, and for informing predictions of climate-change impacts on water quantity.
- Do not perform direct, time-by-time point comparisons between observations and model outputs; rely on multi-decadal statistical analyses.
- Ensure when comparing periods that the same ensemble member is used for both baseline and future data.
- Use the supplementary NRFA-station grid to compare G2G estimates to observed river flow at corresponding NRFA locations, where appropriate.

## Limitations and cautions
- G2G emphasizes natural flow regimes and uses globally applicable parameter values; performance is best in catchments with natural flows and accurate baseline data, and may be poorer in areas with strong artificial regulation or complex subsurface hydrology.
- Discretisation to 1km grid can create discrepancies with observed NRFA catchment delineations, especially for smaller catchments.
- The 360-day calendar and 30-day months introduce non-standard temporal framing relative to real-world calendars.
- The dataset covers Great Britain only; Northern Ireland data are available in separate datasets.
- Data are provided as gridded estimates; direct attribution to specific real-world events should be done with statistical caution.

## Acknowledgements and references
- Funded by the Natural Environment Research Council under award NE/R016429/1 as part of UK-SCAPE National Capability.
- Acknowledgement of contributors and key references related to the G2G model, bias correction, and climate-model inputs (e.g., Bell et al. 2009, 2016, 2018; Kay et al.; Murphy et al.; Guillod et al.; Rudd et al.).