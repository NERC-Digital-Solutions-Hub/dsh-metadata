# Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2019) [CHESS-met] Supporting information

- The CHESS-met dataset provides daily meteorological variables on a 1 km grid over Great Britain for 1961–2019, intended to support the Joint UK Land Environment Simulator (JULES) and related analyses.
- Variables include: air temperature (K), specific humidity (kg kg-1), wind speed (m s-1), downward longwave radiation (W m-2), downward shortwave radiation (W m-2), precipitation (kg m-2 s-1), air pressure (Pa), and daily temperature range (K).
- Daily means are from 09:00 GMT to 09:00 GMT the next day (except daily temperature range).

- The release supersedes the 2020 version and extends coverage to 2018–2019; netCDF metadata have been updated for all years.

- In GIS terms, data are suitable for map-based visualization and analysis at high spatial resolution (1 km), with CF-compliant netCDF files designed for interoperability.

- Data sources and variables
  - Precipitation: CEH-GEAR gridded rainfall estimates (1890–2019), scaled to model units.
  - Temperature, humidity, wind, and related variables: derived from MORECS, CRU TS (temperature range with various revisions), and WATCH Forcing Data (air pressure).
  - Elevation context: IHDTM (50 m) for elevation-based adjustments.
  - Wind resource context: ETSU 1 km wind speed dataset.

- Data preparation and variable creation
  - Precipitation: scaled from CEH-GEAR totals to model units (mm/day to mm/s).
  - Air temperature: interpolated MORECS values (bicubic spline) and elevation-adjusted using IHDTM; valid at 1.2 m reference height.
  - Specific humidity: interpolated from MORECS vapor pressure and adjusted for elevation.
  - Downward shortwave radiation (Sd): derived from cloud cover factor (based on MORECS sunshine hours) and corrected for slope and aspect.
  - Downward longwave radiation (Ld): computed from Sd, Ta, and qa, with cloud and elevation considerations.
  - 10 m wind speed (u10): interpolated from MORECS and upscaled/adjusted to long-term ETSU wind speed averages.
  - Surface air pressure (p*): climatology-based, adjusted for 1 km grid elevation.
  - Daily temperature range (DTR): reprojected from CRU TS monthly datasets (various versions by period) with no spatial interpolation.

- File format and organization
  - Data stored in CF-compliant netCDF files.
  - Monthly files, with one file per variable.
  - File codes (e.g., tas for air temperature, huss for specific humidity, sfcWind for wind speed, rlds for down longwave, rsds for down shortwave, precip for precipitation, psurf for air pressure, dtr for daily temperature range).

- Known issues and caveats for GIS users
  - ArcGIS may offset CF-netCDF layers when using projected coordinate systems due to a fixed WGS84 assumption in reading; CHESS-met layers reference a different datum, causing position offsets of roughly 10–100 m.
  - Offsets can be corrected by re-aligning layers with ArcGIS tools; refer to ArcGIS documentation for procedures.

- Data access and citation
  - Data are available via the Environmental Information Data Centre: https://doi.org/10.5285/835a50df-e74f-4bfb-b593-804fd61d5eab
  - Required citation in outputs: Robinson et al. (2023) CHESS-met dataset, NERC EDS EIDC.

- Practical relevance for GIS Specialists
  - Enables high-resolution, map-based exploration of meteorological conditions over GB for range of applications (policy, client reports, public-facing maps).
  - Facilitates integration with spatial datasets (elevation, land cover, hydrology) for GIS-based analyses and visualization.
  - Be mindful of datum-related alignment issues and ensure proper metadata review when importing into GIS workflows.