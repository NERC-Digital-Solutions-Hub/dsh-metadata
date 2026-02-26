# Potential evapotranspiration derived from HadUK-Grid 1km gridded climate observations 1969-2021 (Hydro-PE HadUK-Grid) Supporting information

## Introduction
- Gridded potential evapotranspiration (PET) calculated on a 1 km UK grid for 1969–2021.
- Provides two PET variables:
  - PET: daily total potential evapotranspiration (kg m^-2 d^-1), assuming a well-watered grass surface.
  - PETI: PET with interception correction (kg m^-2 d^-1), correcting for canopy interception on days with precipitation.
- Derived from HadUK-Grid data v1.0.3.0 (1969–2020) and v1.1.0.0 (2021); no differences between v1.0.3.0 and v1.1.0.0 for 1969–2020 for the variables used.
- PET and PETI calculations follow MORECS v2.0 parameterisations to ensure consistency with historical PET observations.

## Data products (PET and PETI)
- Daily PET and PETI fields on a 1 km UK grid.
- Units: kg m^-2 d^-1 (equivalent to mm d^-1).
- Intended for hydrological modelling and data-supported analyses in the UK.

## Input data and preparation
- Input: HadUK-Grid dataset (v1.0.3.0 for 1969–2020; v1.1.0.0 for 2021) on a 1 km grid, interpolated from station data to grid points.
- Temporal coverage: 1969–2021, with the start time dependent on variable and resolution; all PET inputs required from 1969.
- Variables used for PET and PETI:
  - Monthly mean water vapour pressure (pv), monthly mean sea level pressure (psl), monthly total sunshine hours (sun)
  - Daily values or interpolated daily values for wind speed at 10 m (u10), daily max/min temperatures (tasmax, tasmin)
  - Daily precipitation (rainfall, P) used for interception (PETI)
- Ancillary data:
  - Surface altitude (EU-DEM v1.1)
  - Ångström coefficients a, b, c
- Monthly data are interpolated to daily time steps via quadratic interpolation before calculations.

## Calculations and parameterisations
- Penman-Monteith equation used to compute PET (E_p), parameterised for a well-watered short grass surface.
- Inputs derived from HadUK-Grid data:
  - Daily mean temperature: average of tasmax and tasmin (with specific handling around day boundaries to align with rainfall timespan).
  - Specific humidity and its saturation value derived from temperature and pressure.
  - Air density from temperature and pressure.
  - Net radiation: sum of net shortwave (from sunshine hours using Ångström approach) and net longwave (from temperature and vapour pressure, following MORECS v2.0 methods).
  - Aerodynamic resistance and canopy resistance calculated as functions of wind speed and leaf area index, following MORECS v2.0.
  - Ground heat flux treated as a monthly mean value.
- Parameterisations align with MORECS v2.0 documentation to ensure comparability with historical PET data.

## Interception correction (PETI)
- On days with zero precipitation, PETI = PET.
- On days with precipitation (P > 0), interception water CI and canopy evaporation are modelled:
  - Interception water CI calculated from precipitation and leaf area index, enhanced in spring/summer/autumn to account for multiple daily events.
  - Evaporation from intercepted water EI computed with canopy resistance set to zero, then PETI combines PET with CI and EI using a defined rule to reflect canopy interception dynamics.
- Wet canopy effects and interception corrections ensure PETI reflects canopy evaporation losses beyond direct transpiration.

## Interpolation details and data continuity
- Quadratic interpolation used to convert monthly variables to daily values, with monthly timestamps assumed at mid-month (15th).
- To prevent backward changes when new years are added, daily values from the last interpolated year are kept intact and only the new monthly data are interpolated, preserving continuity and reducing end-of-range inconsistencies.

## File format and data access
- Data distributed as NetCDF files (CF Metadata Conventions v1.8; ACDD v1-3).
- Structure: monthly NetCDF files, one file per variable (pet or peti) and year.
- Spatial information:
  - 1 km grid aligned to the British National Grid (BNG), EPSG:27700.
  - WGS84 coordinates (EPSG:4326) provided as latitude/longitude.
  - Note: ArcGIS reading can show a small position offset when using projected coordinates due to datum handling; adjust as needed.
- Time information:
  - Daily mean values from 1969-01-01 to 2021-12-31.
  - Monthly variables interpolated to daily with mid-month timestamps.

## Spatial and temporal coverage
- Spatial: United Kingdom on a 1 km grid; projection EPSG:27700 with auxiliary WGS84 coordinates.
- Temporal: Daily time series from 1969-01-01 to 2021-12-31.
- Data are designed for hydrological modelling and long-term climate analyses, with PETI aligned to MORECS-based historical PET.

## Acknowledgements
- Funded by Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme.

## References
- MORECS v2.0 methodology and documentation.
- HadUK-Grid gridded climate observations (UK grid dataset).
- EU-DEM v1.1 and related data sources for elevation.
- Foundational methodological references for long-wave radiation, net radiation, and PET related formulations used in the dataset.