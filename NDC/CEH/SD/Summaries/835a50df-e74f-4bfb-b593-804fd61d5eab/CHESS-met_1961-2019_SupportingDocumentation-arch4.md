# Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2019) [CHESS-met]

- Overview
  - Provides daily meteorological variables on a 1 km grid over Great Britain for 1961–2019.
  - Variables cover data needed to run the Joint UK Land Environment Simulator (JULES) with daily disaggregation.
  - This release extends coverage to 2018–2019 and updates metadata; supersedes the 2020 version.

- Variables included
  - Air temperature (K)
  - Specific humidity (kg kg-1)
  - Wind speed (m s-1)
  - Downward longwave radiation (W m-2)
  - Downward shortwave radiation (W m-2)
  - Precipitation (kg m-2 s-1)
  - Air pressure (Pa)
  - Daily temperature range (K)

- Data sources (input meteorological data)
  - CEH-GEAR: daily and monthly areal rainfall estimates (precipitation)
  - MORECS: daily mean air temperature, vapor pressure, sunshine hours, wind speed
  - CRU TS: daily temperature range across multiple versions (1961–2019)
  - WATCH Forcing Data: air pressure

- Other input data
  - Integrated Hydrological Digital Terrain Model (IHDTM) at 50 m elevation
  - ETSU 1 km mean wind speed dataset

- Methods (how variables are created)
  - Precipitation: scaled from CEH-GEAR totals to model units
  - Air temperature: interpolated MORECS temp and elevation-adjusted (1.2 m reference height)
  - Specific humidity: interpolated vapor pressure from MORECS and adjusted for elevation
  - Downward shortwave/longwave radiation: derived from cloud cover factor (based on MORECS sunshine hours) and adjusted for slope/aspect; longwave uses temp and humidity
  - Wind speed: interpolated MORECS wind, adjusted using long-term ETSU wind speeds
  - Surface pressure: mean-monthly climatology adjusted for 1 km elevation
  - Daily temperature range: reprojected from CRU TS across periods with no spatial interpolation

- File format and organization
  - NetCDF, CF-compliant, UKCEH gridded conventions
  - Monthly files, one file per variable
  - Variable-to-file naming: tas (air temperature), dtr (daily temperature range), huss (specific humidity), sfcWind (wind speed), rlds (downward longwave), rsds (downward shortwave), precip (precipitation), psurf (air pressure)

- Data availability and citation
  - Data available from the Environmental Information Data Centre: https://doi.org/10.5285/835a50df-e74f-4bfb-b593-804fd61d5eab
  - Recommended citation: Robinson et al. (2023). Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2019) [CHESS-met]. NERC EDS EIDC. https://doi.org/10.5285/835a50df-e74f-4bfb-b593-804fd61d5eab

- Known issues
  - ArcGIS read issue with CF-compliant files in projected coordinate systems due to WGS 1984 datum assumption; results in 10–100 m offset. Layers can be adjusted in ArcGIS; refer to ArcGIS documentation.

- Relevance for data leadership
  - Demonstrates the end-to-end creation of a high-resolution, standards-compliant data asset to support modeling (JULES) and ecological studies.
  - Highlights integration of diverse data sources, metadata currency, and practical data management considerations (quality, discoverability, updates).
  - Addresses accessibility constraints (data availability, documentation) and practical steps for coordinating data products across a wider user community.