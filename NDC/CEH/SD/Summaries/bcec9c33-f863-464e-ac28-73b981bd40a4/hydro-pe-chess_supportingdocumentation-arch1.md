# Potential evapotranspiration derived from Climate Hydrology and Ecology Research Support System Meteorological gridded climate observations (Hydro-PE CHESS), 1961-2019 Supporting information

- A dataset providing two daily potential evapotranspiration (PET) variables for Great Britain at 1 km resolution, 1961–2019:
  - PET: daily total potential evapotranspiration (kg m-2 d-1), equivalent to mm d-1
  - PETI: daily PET with interception correction (kg m-2 d-1), accounts for canopy interception on precipitation days
- Derived from CHESS-met meteorology data (1961–2019) interpolated from MORECS 40 km to a 1 km grid

- Inputs and calculation approach
  - PET and PETI computed using Penman–Monteith formulation for a well-watered grass surface
  - Interception correction (PETI) applied only on days with precipitation; otherwise PETI = PET
  - Additional inputs derived from CHESS-met: specific humidity, air density, net radiation, and aerodynamic/canopy resistances
  - PETI uses daily precipitation (0900 UTC day D to 0900 UTC day D+1) to determine interception effects
  - Calculations aligned with MORECS v2.0 parameterisations to ensure historical consistency

- Data specifics and formats
  - Spatial grid: 1 km, aligned to British National Grid (BNG) OSGB 1936; projection EPSG 27700; lat/lon provided (WGS84 EPSG 4326)
  - Temporal coverage: daily mean values from 1961-01-01 to 2019-12-31
  - File format: NetCDF CF v1.8 with ACDD v1-3 conventions
  - File structure: monthly NetCDF files; one file per variable
  - Metadata includes: time (hours since 1961-01-01), time_bnds, grid coordinates (x, y, lat, lon), and projection details
  - Known issue: ArcGIS may offset layers when reading projected coordinate systems; adjust layers to correct position

- Usage context and purpose
  - Designed for hydrological modelling in the UK; suitable for assessing evapotranspiration patterns and water balance
  - PETI provides an interception-corrected ET potential useful for studies needing canopy interception effects
  - PET and PETI are compatible with historical MORECS data for cross-validation and trend analyses

- Data provenance and references
  - Supported by Natural Environment Research Council grant NE/S017380/1 (Hydro-JULES)
  - Key references: MORECS v2.0 (Hough, 1995); Penman–Monteith formulations (Stewart, 1989); Robinson et al. 2023 (Hydro-PE dataset)
  
- Practical considerations for analysts
  - Local-scale data gaps or scale mismatches may limit applicability at very fine resolutions or in non-UK regions
  - Data processing requires NetCDF-compatible tools; ensure ArcGIS/workflows account for projection datum differences
  - Metadata and data provenance enable reproducibility and discoverability of derived datasets

- Potential analyses enabled
  - Correlation of PET/PETI with climate drivers (temperature, humidity, radiation, wind)
  - Spatial and temporal trends in potential evapotranspiration
  - Integration into hydrological models to estimate water demand, drought risk, or irrigation needs
  - Comparative analyses with MORECS-based datasets or other PET datasets for validation