# Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2019) [CHESS-met]

## Overview
- Provides daily meteorological variables on a 1 km grid over Great Britain (GB) for use with the Joint UK Land Environment Simulator (JULES) with daily disaggregation.
- Variables included: air temperature (K), specific humidity (kg kg-1), wind speed (m s-1), downward longwave radiation (W m-2), downward shortwave radiation (W m-2), precipitation (kg m-2 s-1), air pressure (Pa), and daily temperature range (K).
- Coverage extended to 2018-2019; this release supersedes the previous version (2017-2019) with updated metadata.
- Data are distributed as CF-compliant netCDF files and are suitable for environmental monitoring and policy-support analyses.

## Data sources and inputs
- Input meteorological data:
  - CEH-GEAR for daily rainfall (precipitation)
  - MORECS for daily mean air temperature, vapor pressure, hours of bright sunshine, and wind speed
  - CRU TS 3.21/3.24/4.x for daily temperature range (DTR) across periods
  - WATCH Forcing Data for air pressure
- Additional inputs:
  - Integrated Hydrological Digital Terrain Model (IHDTM) at 50 m resolution (elevation)
  - UK Energy Technology Support Unit (ETSU) 1 km wind speeds

## Processing methods
- Precipitation: scaled from CEH-GEAR daily totals (mm/day) to kg m-2 s-1 for JULES
- Air temperature: MORECS temperatures interpolated with bicubic splines and elevation-adjusted using IHDTM; valid at 1.2 m
- Specific humidity: interpolated from MORECS vapor pressure and adjusted for elevation; derived with temperature
- Downward shortwave radiation: computed from cloud cover factor (derived from MORECS sunshine hours), then corrected for slope and aspect
- Downward longwave radiation: calculated from temperature, humidity, and cloud cover
- Wind speed: 10 m wind interpolated from MORECS and adjusted to long-term ETSU wind speed climatology
- Surface pressure: mean-monthly climatology from WFD data, adjusted for 1 km elevation
- Daily temperature range (DTR): reprojected from CRU TS datasets for respective periods with no spatial interpolation
- File format: netCDF, CF-compliant, following UKCEH gridded dataset conventions

## File format and organization
- Files are distributed as monthly netCDF files, one per variable
- Variable-to-file naming conventions:
  - tas: air temperature
  - dtr: daily temperature range
  - huss: specific humidity
  - sfcWind: wind speed
  - rlds: downward longwave radiation
  - rsds: downward shortwave radiation
  - precip: precipitation
  - psurf: air pressure

## Known issues
- ArcGIS CF-reading issue with projected coordinate systems: geographic datum assumed as WGS 1984, causing 10–100 m positional offsets for CHESS-met layers. Offsets can be corrected with standard ArcGIS tools.

## Data availability and citation
- Availability: Environmental Information Data Centre (EIDC) DOI: https://doi.org/10.5285/835a50df-e74f-4bfb-b593-804fd61d5eab
- Required citation in publications: Robinson et al. (2023), CHESS-met dataset, NERC EDS Environmental Information Data Centre

## Relevance to monitoring frameworks
- Provides high-resolution, provenance-traceable meteorological data essential for environmental health monitoring and policy evaluation.
- Emphasizes transparency and data quality through CF-compliance, metadata updates, and clear data provenance.
- Supports evidence-based decision-making by enabling robust modeling (JULES) and clear documentation of data sources, processing methods, and governance.
- Addresses common monitoring-frame challenges: data availability, metadata completeness, data transformation needs, and data sharing considerations.