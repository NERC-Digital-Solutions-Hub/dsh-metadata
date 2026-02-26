# Potential evapotranspiration derived from Climate Hydrology and Ecology Research Support System Meteorological gridded climate observations (Hydro-PE CHESS), 1961-2019 Supporting information

## Overview
- Dataset provides two daily potential evapotranspiration variables: PET and PETI (with interception correction).
- Derived from the CHESS-met dataset for Great Britain (1961–2019) on a 1 km grid.
- PET computed with Penman–Monteith for a well-watered grass surface; PETI includes interception correction for days with precipitation.
- Units are kg m^-2 d^-1, equivalent to mm d^-1.
- Developed for UK hydrological modelling; tuned to be consistent with MORECS v2.0 parameterisations.

## Data Content
- Variables: daily total PET and daily total PETI (interception-corrected).
- Temporal coverage: 1961-01-01 to 2019-12-31 (daily mean values).
- Spatial coverage and grid: 1 km resolution, British National Grid (OSGB 1936), EPSG:27700; latitude/longitude also provided in WGS84 (EPSG:4326).
- Metadata and structure:NetCDF files following CF v1.8 conventions and ACDD v1-3; daily data stored in monthly NetCDF files, one file per variable.
- File content includes: time, time_bnds, crsOGB, x/x_bnds, y/y_bnds, lat, lon, with PET or PETI as the primary data variable.

## Methods and Calculations
- Penman–Monteith equation used to estimate PET, with adaptations for a well-watered short grass surface.
- Core inputs (daily means from CHESS-met): air temperature (tas), specific humidity (huss), air pressure (psurf), wind speed (sfcWind), downwelling shortwave (rsds) and longwave (rlds) radiation.
- Derived inputs: saturation humidity and its derivative, air density, total net radiation, and aerodynamic resistance (function of wind speed).
- Parameterisations drawn from MORECS v2.0 to ensure historical consistency, including long‑wave correction and grass-surface properties (ground heat flux, canopy and stomatal resistances, LAI).

## Interception Correction
- PETI equals PET on days with no precipitation.
- On days with precipitation (P > 0), interception by canopy is accounted for: CI calculated from P and LAI; EI computed as open-water evaporation; PETI adjusted to reflect canopy interception dynamics, following MORECS v2.0 methodology.
- The calculation treats all precipitation as rainfall for interception purposes.

## Data Format and Access
- Format: NetCDF files (CF v1.8) with ACDD v1-3 compliance.
- Temporal format: daily values aggregated into monthly NetCDF files (one per variable: PET, PETI).
- Spatial specifics: 1 km grid aligned to OSGB 1936 (EPSG:27700); supports reprojecting to WGS84 (EPSG:4326) for mapping.
- Known issue: ArcGIS may offset layers when reading non-WGS84 CF projections; adjust layers as needed using ArcGIS tools.

## Spatial and Temporal Information
- Spatial grid: 1 km resolution on the British National Grid; coordinates provided in eastings/northings and corresponding lat/lon.
- Temporal resolution: daily means; period 1961-01-01 to 2019-12-31.

## Reproducibility and Consistency
- Parameterisations and input handling align with MORECS v2.0 documentation to maintain historical comparability with established datasets.
- CHESS-met inputs and calculations documented to enable replication and integration with other CHESS-derived products.

## Usage and Applications
- Intended for hydrological modelling and environmental monitoring in the UK.
- Useful for standardised assessments of potential evaporation trends and for integration with other environmental datasets.
- Datasets to be stored and shared via appropriate data portals, enabling broader accessibility.

## Challenges and Considerations
- Increasing the value of datasets by linking PET/PETI with additional environmental data for broader analyses (dataset reuse beyond single-use applications).
- Ensuring open access to underlying data used for final outputs to support transparency and secondary analyses.

## Acknowledgements
- Funded by Natural Environment Research Council award NE/S017380/1 as part of the Hydro-JULES programme.

## References
- Hough, M. (1995). The Meteorological Office Rainfall and Evaporation Calculation System: MORECS v2.0.
- Richards, J. M. (1971). A simple expression for the saturation vapour pressure of water.
- Robinson, E. L. et al. (2023). Hydro-PE: gridded datasets of historical and future Penman-Monteith potential evaporation for the United Kingdom.
- Robinson, E. et al. (2023). CHESS-met dataset for Great Britain (1961–2019).
- Stewart, J. B. (1989). On the use of the Penman–Monteith equation for determining areal evapotranspiration.