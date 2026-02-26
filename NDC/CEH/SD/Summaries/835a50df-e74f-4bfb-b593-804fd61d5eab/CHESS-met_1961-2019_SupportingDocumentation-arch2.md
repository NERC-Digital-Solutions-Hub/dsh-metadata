# Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2019) [CHESSmet] Supporting information

## Overview and purpose
- Provides daily meteorological variables on a 1 km grid over Great Britain for 1961–2019 to support the Joint UK Land Environment Simulator (JULES) with daily disaggregation.
- Variables are designed to enable consistent environmental monitoring and modelling of hydrology and ecology.

## Variables included
- Air temperature (K)
- Specific humidity (kg kg-1)
- Wind speed (m s-1)
- Downward longwave radiation (W m-2)
- Downward shortwave radiation (W m-2)
- Precipitation (kg m-2 s-1)
- Air pressure (Pa)
- Daily temperature range (DTR, K)
- Note: All variables (except DTR) are daily mean values from 09:00 GMT to 09:00 GMT the next day.

## Data sources and input data
- Precipitation: CEH-GEAR daily rainfall estimates (Keller et al., 2015; Tanguy et al., 2021)
- Air temperature, vapor pressure, sunshine hours, wind speed: MORECS (Hough and Jones, 1997)
- Daily temperature range: CRU TS versions (1961–2012: 3.21; 2013–15: 3.24; 2016–17: 4.03; 2018–19: 4.04)
- Air pressure: WATCH Forcing Data (Weedon et al., 2011)
- Elevation: Integrated Hydrological Digital Terrain Model (IHDTM) 50 m
- Wind speeds: ETSU 1 km resolution dataset

## Methods used to create meteorological variables
- Precipitation (P): scaled from CEH-GEAR daily totals to units required by JULES (mm/s).
- Air temperature (Ta): interpolate MORECS temperature using bicubic spline; adjust for grid cell elevation from IHDTM; valid at 1.2 m height.
- Specific humidity (qa): interpolate MORECS vapor pressure; compute from Ta and vapor pressure; elevation-adjusted; valid at 1.2 m.
- Downward shortwave radiation (Sd) and longwave radiation (Ld): derive cloud cover factor from MORECS sunshine hours; interpolate; adjust for slope and aspect; Ld computed with Ta and qa.
- Wind speed (u10): interpolate MORECS wind speed; adjust to long-term ETSU windspeed averages.
- Surface air pressure (psurf): climatology of WFD pressure adjusted for 1 km elevation.
- Daily temperature range (DTR): reprojected from CRU TS historical datasets with varying resolutions across years; no spatial interpolation beyond reprojection.
- All data are produced on a 1 km grid for Great Britain.

## File format and data organization
- NetCDF format, CF-compliant, following UKCEH gridded dataset conventions.
- Data stored as monthly files, one file per variable.
- File naming follows a consistent mapping between variables and file codes (e.g., tas for air temperature, dtr for daily temperature range, huss for specific humidity, sfcWind for wind speed, rlds for downward longwave radiation, rsds for downward shortwave radiation, precip for precipitation, psurf for air pressure).

## Known issues
- ArcGIS limitation: reading CF-compliant files with projected coordinate systems defaults to a WGS 1984 datum, causing a positional offset of 10–100 m for CHESS-met layers. Layers can be adjusted in ArcGIS to correct position.

## Data availability and citation
- Data are available from the Environmental Information Data Centre: https://doi.org/10.5285/835a50df-e74f-4bfb-b593-804fd61d5eab
- In publications or outputs, cite: Robinson et al. 2023, Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2019) [CHESS-met], NERC EDS Environmental Information Data Centre.

## Key references
- Methods and data sources underpinning CHESS-met, including CRU TS, MORECS, CEH-GEAR, WATCH Forcing Data, and ETSU wind data, as outlined in the accompanying references (e.g., Robinson et al. 2017; Best et al. 2011; Weedon et al. 2011; Keller et al. 2015; Tanguy et al. 2021).