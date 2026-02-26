# Climate hydrology and ecology research support system meteorology dataset (19612017) [CHESS-met] data set provides daily meteorological variables on a 1km grid over Great Britain

- Overview
  - CHESS-met provides daily meteorological variables on a 1km grid over Great Britain.
  - Variables: air temperature (K), specific humidity (kg/kg), wind speed (m/s), downward longwave radiation (W/m²), downward shortwave radiation (W/m²), precipitation (kg/m²/s), air pressure (Pa), and daily temperature range (K).
  - Daily means from 09:00 GMT to 09:00 GMT the next day.
  - Precipitation is from CEH-GEAR; other variables are derived from coarser input datasets.
  - This release extends coverage to 2016–2017 and updates metadata for CF-compliance; supersedes the 2017 release.

- Input meteorological data sources
  - CEH-GEAR for daily areal rainfall (precipitation) across the UK (1890–2017)
  - MORECS for daily mean air temperature, vapour pressure, hours of bright sunshine, and wind speed
  - CRU TS 3.21/3.24/4.03 for daily temperature range (1961–2017, with year-specific datasets)
  - WATCH Forcing Data for air pressure

- Other input data
  - Integrated Hydrological Digital Terrain Model (IHDTM), 50 m resolution elevation
  - ETSU 1 km resolution mean wind speeds

- Methods for creating meteorological variables
  - Precipitation (P): scaled from CEH-GEAR totals to units used by JULES (mm/s)
  - Air temperature (Ta): bicubic interpolation of MORECS temperature, elevation-adjusted to 1.2 m reference height
  - Specific humidity (qa): interpolated from MORECS vapour pressure and Ta, elevation-adjusted
  - Downward shortwave radiation (Sd) and longwave radiation (Ld): computed from cloud cover factor derived from MORECS sunshine hours; Sd corrected for slope/aspect; Ld uses Ta and qa
  - Wind speed at 10 m (u10): interpolated MORECS wind speed, adjusted to long-term ETSU wind averages
  - Surface pressure (p*): mean-monthly climatology of WFD pressure, elevation-adjusted
  - Daily temperature range (DTR): reprojected from CRU TS datasets with no spatial interpolation
  - Notes: 1961–2015 values match the previous CHESS-met release; metadata updated for CF compliance; files are not identical to prior versions.

- File format and access
  - NetCDF format, CF-compliant, following CEH gridded dataset conventions
  - Data stored as monthly files, one file per variable
  - Data availability: Environmental Information Data Centre
  - Download: https://catalogue.ceh.ac.uk/documents/2ab15bf0-ad08-415c-ba64-831168be7293

- Known issues
  - Reading CF-compliant files with projected coordinate systems in ArcGIS can offset layers by 10–100 m due to assumed WGS84 datum; adjust layers with ArcGIS tools as needed.

- References
  - Foundational datasets and methods: CEH-GEAR, MORECS, CRU TS, WATCH forcing data, IHDTM, ETSU; and CHESS-met methodological papers and updates.