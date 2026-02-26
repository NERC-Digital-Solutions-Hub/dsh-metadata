# Climate hydrology and ecology research support system meteorology dataset (1961-2012) [CHESS-met]

## Overview
- A 1 km resolution daily meteorological dataset for Great Britain designed to support the Joint UK Land Environment Simulator (JULES) with daily disaggregation.
- Covers 1961–2012, providing essential variables for climate hydrology and ecology analyses on a gridded basis.
- Variables are prepared to be readily usable in GIS workflows and data analyses, with CF-compliant netCDF output.

## Data and variables
- tas: air temperature (Kelvin)
- huss: specific humidity (kg/kg)
- sfcWind: wind speed (m/s)
- rlds: downward longwave radiation (W/m^2)
- rsds: downward shortwave radiation (W/m^2)
- precip: precipitation (kg/m^2/s)
- psurf: surface air pressure (Pa)
- dtr: daily temperature range (K)
- Temporal scope: daily means from 09:00 GMT to 09:00 GMT the next day (except dtr, which is reprojected from CRU TS 3.21 data with no spatial interpolation)

## Input data sources
- MORECS: daily mean air temperature, vapour pressure, hours of bright sunshine, wind speed
- CRU TS 3.21: daily temperature range (and baseline climatic data)
- WATCH Forcing Data: air pressure
- IHDTM: 50 m elevation model
- ETSU wind speed dataset: 1 km wind speed basemap
- CEH-GEAR: daily rainfall estimates used to scale precipitation

## Methods and processing
- Precipitation: scaled from CEH-GEAR daily totals to units required by JULES (kg/m^2/s)
- Temperature: MORECS temperature interpolated with bicubic spline, elevation-adjusted using IHDTM; valid at 1.2 m reference height
- Specific humidity: derived from interpolated MORECS vapour pressure and temperature, elevation-adjusted
- Shortwave and longwave radiation: downward shortwave corrected for slope/aspect; downward longwave derived from cloud cover factor (based on sunshine hours) and other variables
- Wind: 10 m wind speed interpolated from MORECS and adjusted using long-term ETSU wind speeds
- Pressure: mean-monthly climatology of WFD pressure, elevation-adjusted to 1 km
- Daily temperature range: reprojected from CRU TS 3.21 0.5° monthly data with no spatial interpolation
- Grid: 1 km resolution across Great Britain; elevation and terrain effects accounted for in radiation and temperature adjustments

## File formats and access
- Data distributed in netCDF format, CF-compliant, following CEH gridded dataset conventions
- Subset downloads via Order Manager include all variables for the requested temporal/spatial aggregation
- Variable naming in netCDF:
  - tas: air temperature
  - huss: specific humidity
  - sfcWind: wind speed
  - rlds: downward longwave radiation
  - rsds: downward shortwave radiation
  - precip: precipitation
  - psurf: air pressure
  - dtr: daily temperature range
- Original files (monthly): chess_<var>_<year><month>.nc

## Relevance to GIS
- Provides a harmonised, resampled 1 km GB-wide gridded meteorological dataset suitable for GIS analyses, spatial overlays, and map-based visualisations.
- CF-compliant netCDF facilitates interoperability with common GIS and scientific software; consistent variable naming aids scriptable data access.
- Elevation-aware processing and terrain corrections enable more accurate spatial analyses of energy fluxes, precipitation, and other climate variables.

## References
- Best, M. J. et al. (2011). The Joint UK Land Environment Simulator (JULES), model description - Part 1: Energy and water fluxes.
- Hough, M. N., & Jones, R. J. A. (1997). MORECS v2.0 overview.
- Jones, P. D., & Harris, I. (2013). CRU TS3.21 dataset description.
- Tanguy, M. et al. (2014). CEH-GEAR: gridded rainfall estimates for the UK.
- Weedon, G. P. et al. (2011). Creation of the WATCH Forcing Data.
- Additional methodological and data-source references as listed in the CHESS-met documentation.