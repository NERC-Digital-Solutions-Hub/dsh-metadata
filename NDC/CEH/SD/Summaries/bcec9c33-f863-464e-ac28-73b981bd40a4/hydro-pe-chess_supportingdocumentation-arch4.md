# Potential evapotranspiration derived from Climate Hydrology and Ecology Research Support System Meteorological gridded climate observations (Hydro-PE CHESS), 1961-2019 Supporting information

- Overview
  - A dataset containing daily total potential evapotranspiration (PET) and PET with interception correction (PETI) for Great Britain (1961–2019) on a 1 km grid.
  - Based on CHESS-met meteorology data (1961–2019) and developed for hydrological modelling in the UK.
  - PET and PETI units: kg m-2 d-1 (equiv. mm d-1).

- Data content
  - Variables included: PET and PETI (daily totals).
  - Time coverage: 1961-01-01 to 2019-12-31 (daily means).
  - Spatial coverage: 1 km grid aligned to British National Grid (BNG, OSGB 1936; EPSG:27700); lat/lon provided in WGS84 (EPSG:4326).
  - File format: NetCDF with CF v1.8 conventions; AC DD v1-3; monthly files per variable.
  - NetCDF structure includes: pet or peti, time, time_bnds, crsOGB, x/x_bnds, y/y_bnds, lat, lon.

- Computation method
  - PET calculated with the Penman–Monteith equation parameterised for a well-watered grass surface.
  - Interception-corrected PET (PETI) additions follow MORECS v2.0; interception correction applied on days with precipitation.
  - Calculations use daily CHESS-met variables and derived quantities (specific humidity at saturation, air density, total net radiation, aerodynamic resistance).
  - Parameterisations and constants adapted from MORECS v2.0 (e.g., grass canopy height ~0.15 m; ground heat flux as a monthly mean).

- Inputs and data provenance
  - Primary input: CHESS-met dataset (Great Britain, 1961–2019) interpolated from MORECS 40 km to a 1 km grid.
  - CHESS-met variables used: daily mean air temperature (tas), specific humidity (huss), air pressure (psurf), wind speed (sfcWind), shortwave radiation (rsds), longwave radiation (rlds); precipitation (prec) used for PETI.
  - Data alignment to historical MORECS data ensures consistency with existing records.

- Interception correction details
  - On days with P > 0, canopy interception water (CI) reduces PETI via an evaporation rate (EI) calculation; CI is enhanced in spring/summer/autumn for multiple daily precipitation events.
  - PETI is adjusted as either equal to PET (P = 0) or reduced/increased by interception water depending on CI and EI, following predetermined conditions.
  - All precipitation events are treated as rainfall within this correction.

- Spatial and temporal information
  - Spatial grid: 1 km resolution, OSGB 1936, EPSG:27700; coordinates provided in eastings/northings.
  - Temporal: daily means, spanning 1961-01-01 to 2019-12-31.

- Data quality, limitations, and caveats
  - ArcGIS readIssues: CF-projected coordinates can cause 10–100 m offsets when reading in ArcGIS; adjustment may be required.
  - PETI relies on interception modelling and MORECS v2.0 parameterisations; differences may arise compared with other evapotranspiration products.
  - PET uses daily mean inputs rather than separate day/night calculations (as in some versions of MORECS).

- Access, usage, and governance
  - Data are provided as NetCDF with standardized metadata (CF conventions; discoverability via ACDD).
  - Suitable for hydrological modelling, climate impact studies, and integration with related CHESS-Hydro datasets.
  - Acknowledges support from Natural Environment Research Council (NE/S017380/1) under the Hydro-JULES programme.

- Acknowledgements and references
  - Acknowledges contributions from M. Hough (MORECS v2.0), Richards (1971), and Robinson et al. (2023) for Hydro-PE and CHESS-met development.
  - Key references include MORECS v2.0 documentation and related methodological papers.