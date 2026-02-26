# Climate hydrology and ecology research support system meteorology dataset (1961-2012) [CHESS-met]

- Overview
  - Provides daily meteorological variables on a 1 km grid across Great Britain (1961–2012) to support the Joint UK Land Environment Simulator (JULES) with daily disaggregation.
  - Variables cover temperature, humidity, wind, radiation, precipitation, pressure, and daily temperature range.
  - Precipitation data are CEH-GEAR estimates scaled to required units; other variables are derived from coarser-resolution datasets.
  - Data are distributed as CF-compliant netCDF files following CEH gridded dataset conventions.

- Data Coverage and Resolution
  - Spatial: 1 km grid covering Great Britain
  - Temporal: 1961–2012
  - Daily mean values (09:00 GMT to 09:00 GMT next day) for all variables except daily temperature range (DTR)

- Variables Included
  - tas: air temperature (K)
  - huss: specific humidity (kg kg-1)
  - sfcWind: wind speed (m s-1)
  - rlds: downward longwave radiation (W m-2)
  - rsds: downward shortwave radiation (W m-2)
  - precip: precipitation (kg m-2 s-1)
  - psurf: surface air pressure (Pa)
  - dtr: daily temperature range (K)

- Data Sources and Derivation
  - Input data sources
    - MORECS: daily mean air temperature, vapour pressure, hours of bright sunshine, and wind speed
    - CRU TS 3.21: daily temperature range
    - WATCH Forcing Data: air pressure
  - Other inputs
    - IHDTM: 50 m resolution elevation
    - ETSU: 1 km mean wind speeds
  - Derivation and processing
    - Precipitation (P) scaled from CEH-GEAR daily totals (mm/day) to model units (kg m-2 s-1)
    - Air temperature (Ta) interpolated from MORECS and elevation-adjusted; valid at 1.2 m reference height
    - Specific humidity (qa) interpolated from vapour pressure and Ta; elevation-adjusted
    - Cloud cover factor derived from sunshine hours; used to compute S_d and L_d
    - S_d (downward shortwave radiation) corrected for slope and aspect
    - L_d (downward longwave radiation) computed using Ta, qa, and cloud factor
    - 10 m wind speed (u10) interpolated from MORECS and adjusted by long-term ETSU wind averages
    - p* (surface pressure) climatology adjusted for 1 km grid elevation
    - DTR reprojected from CRU TS 3.21 with no spatial interpolation
  - Reference
    - Full methodological details are presented in Robinson et al. (in prep)

- File Formats and Access
  - Format: netCDF, CF-compliant, CEH gridded dataset conventions
  - Subsetting: Order Manager allows retrieval of required temporal/spatial aggregations; all variables included in a subset file
  - File naming
    - Monthly originals: chess_<var>_<year><month>.nc
    - Variables abbreviations in netCDF: tas, huss, sfcWind, rlds, rsds, precip, psurf, dtr

- Use for Monitoring and Policy
  - Provides standardised, high-resolution meteorological inputs for environmental monitoring and policy performance assessment over time
  - Enables data provenance through multiple established sources and consistent interpolation and adjustment procedures
  - Supports reproducible analyses and integration with model outputs (e.g., JULES energy and water fluxes)

- References (selected)
  - Best et al. (JULES model description)
  - Hough & Jones (MORECS)
  - Jones et al. (CRU TS3.21)
  - Weedon et al. (WATCH Forcing Data)
  - Tanguy et al. (CEH-GEAR)
  - Morris & Flavin (IHDTM)
  - Newton & Burch (ETSU wind data)
  - Robinson et al. (trends in evaporative demand; in prep)