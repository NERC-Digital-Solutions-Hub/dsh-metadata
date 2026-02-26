# Potential evapotranspiration derived from Climate Hydrology and Ecology Research Support System Meteorological gridded climate observations (Hydro-PE CHESS), 1961-2019 Supporting information

## Overview
- Dataset provides two daily potential evapotranspiration variables:
  - PET: daily total potential evapotranspiration (kg m-2 d-1; equivalent to mm d-1)
  - PETI: daily total potential evapotranspiration with interception correction (kg m-2 d-1)
- Grid and period: 1 km grid over Great Britain for 1961–2019 (daily means)
- Method: Penman-Monteith calculation parameterised for a well-watered grass surface
- PETI adjustments: interception by grass canopy on days with nonzero precipitation following MORECS v2.0
- Purpose: hydrological modelling in the UK; parameterisations aligned with MORECS v2.0 documentation

## Data and inputs
- Input dataset: CHESS-met for Great Britain (1961–2019); interpolated from MORECS 40 km to a 1 km grid
- Daily mean inputs used for PET and PETI:
  - Air temperature (tas)
  - Specific humidity (huss)
  - Air pressure (psurf)
  - Wind speed (sfcWind)
  - Downwelling shortwave radiation (rsds)
  - Downwelling longwave radiation (rlds)
- PETI inputs: daily total precipitation (P) from 0900 UTC day D to 0900 UTC day D+1
- All data expressed on a 1 km British National Grid (BNG) framework

## Calculation approach
- PET calculated with the Penman-Monteith equation, using:
  - Specific humidity at saturation and its temperature/pressure derivatives
  - Air density and total net radiation
  - Aerodynamic resistance and canopy resistance
  - Parameters chosen for a well-watered short grass surface (e.g., canopy height ≈ 0.15 m)
  - Ground heat flux treated as a monthly mean
- Additional derived inputs:
  - Derived from CHESS-met: humidity at saturation, its derivative; air density; total net radiation
  - Aerodynamic resistance calculated as a function of wind speed
- Parameter sources: based on MORECS v2.0 documentation (Hough, 1995)

## Interception correction
- On dry days (P = 0): PETI equals PET
- On days with precipitation (P > 0): apply interception correction
  - Water intercepted by canopy (CI) computed as a function of P and leaf area index, enhanced during spring/summer/autumn
  - Canopy evaporation rate (EI) derived by setting canopy resistance to zero
  - PETI adjusted to account for canopy interception and its evaporation, following MORECS v2.0 methodology
- The resulting PETI accounts for canopy interception and its impact on daily PET

## Data format and metadata
- File format: NetCDF following CF Metadata Conventions v1.8 and ACDD v1-3
- File structure: daily data stored in monthly NetCDF files; one file per variable (PET or PETI)
- Variables included in files: time (hours since 1961-01-01), time_bnds, CRS (OSGB 1936 / British National Grid), x/y coordinates and bounds, lat/lon
- Spatial information: 1 km resolution aligned to OSGB 27700; coordinates in metres (eastings/northings); lat/lon provided in WGS84 (EPSG:4326)
- Known caveat: ArcGIS may offset projected coordinate systems due to datum differences; adjust layers as needed

## Spatial and temporal coverage
- Spatial: Great Britain on a 1 km grid (BNG / OSGB 1936)
- Temporal: daily means from 1961-01-01 to 2019-12-31

## Data governance, provenance, and usage notes
- Provenance: derived from CHESS-met (Robinson et al., 2023) and Hydro-PE CHESS methodology; parameterisations linked to MORECS v2.0 (Hough, 1995)
- Acknowledgements: supported by Natural Environment Research Council grant NE/S017380/1 (Hydro-JULES)
- Suggested usage considerations:
  - Ensure consistent datum handling when integrating with other GIS layers (ArcGIS datum offset caveat)
  - Use the CF-compliant metadata for data discovery and interoperability
  - Reference the Hydro-PE CHESS source dataset and MORECS v2.0 parameterisations for methodological context

## References
- Hough, M. (1995). The Meteorological Office Rainfall and Evaporation Calculation System: MORECS v2.0
- Richards, J. M. (1971). A simple expression for the saturation vapour pressure of water
- Robinson, E. L. et al. (2023). Hydro-PE: gridded datasets of historical and future Penman-Monteith potential evaporation for the United Kingdom
- Robinson, E. et al. (2023). Climate hydrology and ecology research support system meteorology dataset for Great Britain (1961-2019) [CHESS-met]