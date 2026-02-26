# Climate hydrology and ecology research support system meteorology dataset (1961-2012) [CHESS-met]

## Overview
- Daily meteorological variables on a 1 km grid over Great Britain, spanning 1961–2012.
- Designed to support the Joint UK Land Environment Simulator (JULES) with daily disaggregation.
- Variables provided (with brief notes on timing): tas (air temperature, 09:00 GMT–09:00 GMT next day), huss (specific humidity), sfcWind (wind speed), rlds (downward longwave radiation), rsds (downward shortwave radiation), precip (precipitation), psurf (air pressure), dtr (daily temperature range).

## Data content for CHESS-met
- Includes the eight meteorological variables listed above.
- Precipitation data are scaled CEH-GEAR rainfall estimates to the required units; other variables derived from coarser resolution inputs.
- Daily values are mean values for each 24-hour period, except daily temperature range (DTR) which is treated separately.

## Data sources and inputs
- Input meteorological data:
  - MORECS dataset (air temperature, vapour pressure, hours of bright sunshine, wind speed).
  - CRU TS 3.21 (daily temperature range).
  - WATCH Forcing Data (air pressure).
- Other input data:
  - IHDTM, 50 m resolution elevation.
  - 1 km wind speed grid from ETSU.
- Data origins and roles:
  - MORECS provides key surface variables and sunshine metrics.
  - CRU TS 3.21 supplies temperature range.
  - WATCH provides atmospheric pressure forcing.
  - Elevation, wind field, and slope/aspect information refine spatial calculations.

## Methods to derive meteorological variables
- Precipitation (P): scaled from CEH-GEAR daily totals (mm/day) to kg m^-2 s^-1 for model compatibility.
- Air temperature (Ta): interpolated MORECS temperature with bicubic spline, elevation-adjusted per 1 km grid cell using IHDTM; valid at 1.2 m reference height.
- Specific humidity (qa): interpolated from MORECS vapour pressure, computed with Ta and elevation adjustments.
- Downward shortwave (Sds) and longwave (Lds) radiation: derived from cloud cover factor (based on MORECS sunshine hours) and Sds adjusted for slope/aspect; Lds computed using Ta, qa.
- Wind (u10): interpolated MORECS wind, then adjusted using long-term ETSU wind averages.
- Surface pressure (psurf): mean-monthly climatology from WFD pressure, adjusted for 1 km grid elevation.
- Daily temperature range (DTR): reprojected from CRU TS 3.21 0.5° resolution, with no spatial interpolation.

## File format and access
- Data distributed in netCDF format (CF-compliant) following CEH gridded dataset conventions.
- Subset downloads contain all variables with requested temporal/spatial aggregations.
- NetCDF variable naming:
  - tas: air temperature
  - huss: specific humidity
  - sfcWind: wind speed
  - rlds: downward longwave radiation
  - rsds: downward shortwave radiation
  - precip: precipitation
  - psurf: air pressure
  - dtr: daily temperature range
- Original files are stored monthly, named chess_<var>_<year><month>.nc.

## Access and use considerations for data leaders
- Purpose-built for integration with JULES; suitable for high-resolution regional climate and hydrology studies.
- Thorough documentation of data provenance, input sources, and transformation steps supports traceability and governance.
- Metadata and CF-compliance enhance discoverability and interoperability across partners and networks.
- Clear versioning via file naming (year/month) and subset options facilitates updates and reuse across projects.
- References to primary data sources (MORECS, CRU TS 3.21, WATCH, CEH-GEAR, IHDTM, ETSU) enable assessment of strengths, uncertainties, and reproducibility in data delivery.

## References (selected)
- JULES model description and relevance to data usage.
- Key input data sources and methodological foundations (MORECS, CRU TS 3.21, WATCH, CEH-GEAR, IHDTM, ETSU).
- Related methodological and data composition studies cited for calibration and validation.