# The Climate hydrology and ecology research support system potential evapotranspiration dataset for Great Britain (1961-2017) [CHESS-PE]

- What it is
  - A 1 km resolution gridded dataset for Great Britain (1961–2017) providing two daily potential evapotranspiration estimates: PET and PETI.
  - PET represents Penman-Monteith PET for a well-watered grass surface.
  - PETI includes interception correction (accounts for rainfall interception and canopy evaporation dynamics).

- Data content and inputs
  - PET is derived from CHESS-met variables: air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), and surface air pressure (p*).
  - PETI uses the same variables plus CEH-GEAR precipitation (rainfall), scaled to appropriate units.
  - Spatial resolution: 1 km across Great Britain; temporal coverage: 1961–2017 (with 2016–17 added in this release).

- Calculation and formats
  - PET: calculated with the Penman-Monteith equation assuming a well-watered grass surface; standard FAO parameters (stomatal resistance ~70 s m-1).
  - PETI: adds potential interception on wet days and models its exponential dry-down to compute total PETI.
  - File format: CF-compliant netCDF files, monthly files; data organized with one file per variable (PET and PETI).

- Data availability and access
  - Hosted by the Environmental Information Data Centre.
  - Download: CEH data catalogue (link provided in the documentation).

- Version updates and impact
  - This release extends data to 2016–2017 and updates netCDF metadata.
  - Bug fixes:
    - PET: humidity deficit (qs - qa) no longer negative; affects ~4% of data; overall mean PET up by ~0.001 mm/day (0.1%).
    - PETI: interception correction previously overestimated; corrections affect ~63% of data; PETI overall decreases by ~0.02 mm/day (~1.5%), with winter changes ~-4% and summer ~-1%; larger differences possible for some timesteps/locations.
  - These changes can lead to spatially and temporally varying differences from earlier releases.

- Known GIS-related issue
  - ArcGIS may offset CHESS-PE layers by 10–100 m due to datum handling; workaround is to adjust layers using ArcGIS tools to align with the correct datum as needed.

- Practical considerations for GIS specialists
  - Suitable for map-based analyses of atmospheric evaporative demand and hydrological modelling across GB.
  - Useful for integrating with other gridded datasets and for landscape-scale evapotranspiration mapping.
  - Consider resampling or reprojecting as needed to align with project coordinate systems, and account for the known ArcGIS datum offset when visualising.

- References (key sources)
  - FAO guidelines (Allen et al., 1998) for crop evapotranspiration
  - CEH-GEAR precipitation dataset (Keller et al., 2015; Tanguy et al., 2019)
  - CHESS-met meteorology dataset (Robinson et al., 2020)
  - CHESS-PE dataset (Robinson et al., 2016; extended release referenced here)