# Climate hydrology and ecology research support system meteorology dataset (1961-2012) [CHESS-met]

- Overview
  - CHESS-met provides daily meteorological variables on a 1 km grid over Great Britain for 1961–2012.
  - Variables enable running the Joint UK Land Environment Simulator (JULES) with daily disaggregation.
  - Variables included: air temperature (tas), specific humidity (huss), wind speed (sfcWind), downward longwave radiation (rlds), downward shortwave radiation (rsds), precipitation (precip), air pressure (psurf), and daily temperature range (dtr). All except dtr are daily means from 09:00 GMT to 09:00 GMT the next day.
  - Precipitation uses CEH-GEAR daily rainfall estimates scaled to model units; other variables derived from coarser resolution datasets.
  - Further methodological information available in Robinson et al. (in prep).

- Input meteorological data sources
  - MORECS for daily mean air temperature, vapour pressure, hours of bright sunshine, and wind speed.
  - CRU TS 3.21 for daily temperature range.
  - WATCH Forcing Data for air pressure.
  - Elevation data from IHDTM (50 m resolution); 1 km wind speeds from ETSU.
  - Daily wind field adjustments incorporate long-term ETSU wind data.

- Data processing and variable construction
  - Precipitation (P) scaled from CEH-GEAR daily totals (mm/day) to kg m^-2 s^-1.
  - Temperature (Ta) created by bicubic interpolation of MORECS temperature, then elevation adjustments; valid at 1.2 m reference height.
  - Specific humidity (qa) derived by interpolating MORECS vapour pressure and combining with Ta; elevation-adjusted.
  - Cloud cover factor derived from MORECS sunshine hours, interpolated, used to compute downward shortwave (Sds) and, with Ta and qa, downward longwave (Lds) radiation.
  - Sds corrected for slope and aspect; south-facing slopes receive more energy.
  - 10 m wind speed (u10) interpolated from MORECS wind speed and adjusted using long-term ETSU wind speeds.
  - Surface air pressure (psurf) a mean-monthly climatology of WFD pressure, adjusted for 1 km grid elevation.
  - Daily temperature range (DTR) reprojected from CRU TS 3.21 monthly data, with no spatial interpolation.

- File format, access, and naming
  - Data distributed as netCDF files (CF-compliant) following CEH gridded dataset conventions.
  - Subset downloads via an Order Manager; files include all variables for requested temporal/spatial aggregations.
  - NetCDF variable names:
    - tas: air temperature
    - huss: specific humidity
    - sfcWind: wind speed
    - rlds: downward longwave radiation
    - rsds: downward shortwave radiation
    - precip: precipitation
    - psurf: air pressure
    - dtr: daily temperature range
  - Original files stored monthly, one file per variable; filenames like chess_<var>_<year><month>.nc for year 1961–2012 and months 01–12.

- References and provenance
  - Datasets and methods drawn from: MORECS, CRU TS, WATCH Forcing Data, IHDTM, ETSU wind dataset.
  - Key references include Best et al. (JULES model description), Hough & Jones (MORECS), Jones & Harris (CRU TS), Weedon et al. (WATCH Forcing Data), and others listed in the document.
  - Further methodological details available in Robinson et al. (in prep).