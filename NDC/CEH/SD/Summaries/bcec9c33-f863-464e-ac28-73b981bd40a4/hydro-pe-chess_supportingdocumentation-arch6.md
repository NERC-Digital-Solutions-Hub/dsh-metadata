# Potential evapotranspiration derived from Climate Hydrology and Ecology Research Support System Meteorological gridded climate observations (Hydro-PE CHESS), 1961-2019 Supporting information

## Overview
- Dataset contains two potential evapotranspiration variables:
  - PET: daily total potential evapotranspiration (kg m^-2 d^-1), equivalent to mm d^-1
  - PETI: daily total potential evapotranspiration with interception correction (kg m^-2 d^-1)
- Derived from CHESS-met for Great Britain (1961-2019) on a 1 km grid
- Developed for hydrological modelling in the UK; PETI aligned with MORECS v2.0 conventions
- Aimed at enabling hydrological analysis and data-inspired decision-making

## What is included
- PET and PETI variables (daily totals)
- Time: daily means from 1961-01-01 to 2019-12-31
- Spatial grid: 1 km resolution on the British National Grid (BNG / OSGB 1936), EPSG:27700
- Coordinate and location data: grid cell centres (x, y in metres), bounds, and corresponding lat/lon in WGS84 (EPSG:4326)
- File structure: netCDF files (CF v1.8) with monthly files for each variable
- Metadata fields: time, time_bnds, CRS, and grid coordinate information

## Data sources and inputs
- Primary input: CHESS-met dataset (Great Britain, 1961-2019), interpolated from MORECS 40 km to 1 km grid
- Daily input variables for PET and PETI calculations:
  - Air temperature (tas)
  - Specific humidity (huss)
  - Air pressure (psurf)
  - Wind speed (sfcWind)
  - Downwelling shortwave radiation (rsds)
  - Downwelling longwave radiation (rlds)
- For PETI (interception correction) additionally used:
  - Daily total precipitation (prec, P) from 09:00 UTC day D to 09:00 UTC day D+1

## Methods and calculations
- PET calculation:
  - Penman-Monteith equation parameterised for a well-watered grass surface
  - Incorporates derived inputs: specific humidity at saturation, air density, total net radiation, aerodynamic resistance
  - Parameters largely drawn from MORECS v2.0 documentation to ensure historical consistency
- Interception correction (PETI):
  - On days with precipitation, correct PET to account for canopy interception
  - Interception water CI calculated from precipitation and leaf area index; canopy evaporation rate EI estimated assuming open water evaporation, with adjustments for multiple daily precipitation events
  - PETI equals PET on zero-precipitation days; on precipitation days PETI is PET adjusted by canopy interception
- Derived products and consistency:
  - Additional inputs derived for the Penman-Monteith calculation (e.g., salinity adjustments not mentioned; focus on humidity, density, net radiation, resistances)
  - Calculations aligned with Hydro-PE CHESS adaptations for UK hydrology

## File format and structure
- Format: netCDF conforming to CF Metadata Conventions v1.8 and ACDD v1-3
- Temporal coverage: daily means
- Spatial coverage: 1 km grid aligned to OSGB 27700 (BNG)
- File organization: monthly netCDF files, with separate files for PET and PETI
- Variables in files include:
  - pet or peti (PET or PETI)
  - time (hours since 1961-01-01)
  - time_bnds (start and end times of each day)
  - crsOGB (BNG coordinate reference system)
  - x, x_bnds (eastings)
  - y, y_bnds (northings)
  - lat, lon (centroid coordinates; WGS84)

## Spatial and temporal information
- Spatial: 1 km resolution; OSGB 1936 / British National Grid; projection EPSG:27700
- Lat/Lon provided as WGS84 (EPSG:4326)
- Temporal: daily means from 1961-01-01 to 2019-12-31

## Known issues and considerations
- ArcGIS reading CF-compliant files with projected coordinate systems can offset layers by ~10–100 m due to datum assumptions (WGS84). Users may need to adjust layers using ArcGIS tools to align with the correct datum.

## Acknowledgements
- Funded by Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme

## References
- Hough, M. (1995). The Meteorological Office Rainfall and Evaporation Calculation System: MORECS v2.0
- Richards, J. M. (1971). Simple expression for saturation vapor pressure
- Robinson, E. L. et al. (2023). Hydro-PE: gridded datasets of historical and future Penman-Monteith potential evaporation for the United Kingdom
- Robinson, E. L. et al. (2023). CHESS-met dataset for Great Britain (1961-2019)
- Stewart, J. B. (1989). On the use of the Penman-Monteith equation for determining areal evapotranspiration