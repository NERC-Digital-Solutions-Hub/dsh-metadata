# Climate hydrology and ecology research support system meteorology dataset (19612017) [CHESS-met] data set

## Purpose and use
- Provides daily meteorological variables on a 1 km grid over Great Britain to support climate, hydrology, and ecology modelling (e.g., JULES) and to inform monitoring and policy evaluation.
- Enables disaggregation to daily timescales for input into environmental models and subsequent health- and policy-relevant analyses.

## Content and variables
- Variables included (daily mean values 09:00 GMT to 09:00 GMT next day): 
  - air temperature (K)
  - specific humidity (kg kg-1)
  - wind speed (m s-1)
  - downward longwave radiation (W m-2)
  - downward shortwave radiation (W m-2)
  - precipitation (kg m-2 s-1)
  - air pressure (Pa)
  - daily temperature range (K)
- Precipitation data sourced from CEH-GEAR and scaled to required units; other variables derived from coarser-resolution datasets.
- Dataset period extended to cover 2016–2017; metadata updated for CF-compliance.

## Data sources and inputs
- CEH-GEAR: daily/monthly areal rainfall estimates for the UK (1890–2017) for precipitation.
- MORECS: daily mean values for air temperature, vapour pressure, hours of bright sunshine, wind speed.
- CRU TS: daily temperature range from versions 3.21 (1961–2012), 3.24 (2013–2015), 4.03 (2016–2017).
- WATCH Forcing Data: air pressure.
- Additional inputs: IHDTM elevation (50 m), ETSU 1 km wind speeds.

## Methods and data production
- Precipitation: scaled from CEH-GEAR totals to model units (mm/day to mm/s).
- Temperature: interpolated MORECS values with bicubic spline; elevation-adjusted using IHDTM; valid at 1.2 m reference height.
- Specific humidity: derived from interpolated vapour pressure and temperature with elevation adjustments.
- Radiation: cloud cover factor derived from MORECS sunshine hours; downward shortwave corrected for slope and aspect; downward longwave computed with temperature, humidity, and cloud factor.
- Wind: 10 m wind speed interpolated from MORECS and adjusted using long-term ETSU wind-speed averages.
- Pressure: mean-monthly climatology adjusted for grid elevation.
- Daily temperature range: reprojected from CRU TS data with no spatial interpolation.
- Metadata updated for CF-compliance; 1961–2015 data consistent with prior CHESS-met release, with updated documentation.

## File format and organization
- NetCDF format, CF-compliant, following CEH gridded dataset conventions.
- Data stored as monthly files, with one file per variable.

## Known issues
- ArcGIS projection issue: reading CF-compliant files with non-WGS84 datums can cause layer position offsets (10–100 m). Can be corrected within ArcGIS using standard tools.

## Data availability and access
- Hosted by the Environmental Information Data Centre.
- Download: CEH catalogue page (link provided in the document).

## Versioning and updates
- Supersedes CHESS-met 2017b (previous release) and expands coverage to 2016–2017.
- Metadata updated to ensure CF-compliance; files are not identical to previous release due to metadata changes.

## References
- Key sources for data sources and methods include CEH-GEAR, MORECS, CRU TS, WATCH Forcing Data, IHDTM, ETSU wind data, and prior CHESS-met publications detailing methodology.