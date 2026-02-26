# Potential evapotranspiration derived from Climate Hydrology and Ecology Research Support System Meteorological gridded climate observations (Hydro-PE CHESS), 1961-2019 Supporting information

## Overview
- Provides two potential evapotranspiration variables for Great Britain (1961–2019):
  - PET: daily total potential evapotranspiration (kg m^-2 d^-1), equivalent to mm d^-1
  - PETI: daily total potential evapotranspiration with interception correction (kg m^-2 d^-1)
- Derived on a 1 km grid, aligned to the British National Grid (BNG) OSGB 1936; daily means on a 1961–2019 basis
- PET is calculated with a Penman-Monteith formulation for a well-watered grass surface; PETI adds interception correction on days with precipitation
- PET and PETI are designed for hydrological modelling in the UK and are made to be consistent with MORECS v2.0 parameterisations

## Data inputs and derivation
- Input dataset: CHESS-met (1961–2019) for Great Britain
- CHESS-met data are interpolated from MORECS 40 km resolution onto a 1 km grid
- Daily mean inputs used for both PET and PETI:
  - Air temperature, specific humidity, air pressure, wind speed, downwelling shortwave and longwave radiation
- PETI uses daily total precipitation (0900 UTC day D to 0900 UTC day D+1)
- Key derivations and computations:
  - Penman-Monteith equation with adjustments, including derived variables: specific humidity at saturation, air density, total net radiation, aerodynamic resistance
  - Parameters set for a well-watered short grass surface (consistent with MORECS v2.0)
  - Ground heat flux (monthly mean), canopy and stomatal resistances, and leaf area index inform resistance calculations

## Interception correction (PETI)
- On days with zero precipitation: PETI = PET
- On days with non-zero precipitation:
  - Compute canopy interception water (CI) as a function of precipitation and leaf area index
  - Interception enhancement in spring–autumn to reflect multiple daily events
  - Evaporation from canopy water (EI) assumed at a near-open-water rate by setting canopy resistance to zero
  - PETI determined as PETI = EP I or adjusted by canopy interception until the canopy dries, then reverts to PET
- Assumption: all precipitation is rainfall for interception calculations

## File format and metadata
- Data packaged as NetCDF, CF Metadata Conventions v1.8 and ACDD v1-3
- Daily values stored in monthly NetCDF files; one file per variable (PET or PETI)
- Variables included: time, time bounds, coordinate reference system (OSGB), grid coordinates (x, y), latitude, longitude, and their bounds
- Spatial information:
  - 1 km grid aligned to OSGB 27700 (EPSG:27700)
  - Projection coordinates in metres (eastings/northings); WGS84 latitude/longitude (EPSG:4326) provided as well
- Temporal information:
  - Daily mean values from 1961-01-01 to 2019-12-31

## Spatial and temporal coverage
- Spatial: Great Britain on a 1 km grid (BNG/OSGB 1936; EPSG:27700)
- Temporal: 1961-01-01 to 2019-12-31 (daily means)

## Data governance, accessibility and caveats
- Methodology emphasizes consistency with historical MORECS data and transparency through documentation and references
- Known practical considerations:
  - ArcGIS reading issues with projected coordinate systems can cause small positional offsets; adjust layers as needed
  - CHESS-met inputs and derived variables rely on parameterisations from MORECS v2.0
- Data provenance and citations provided to support traceability and reproduction

## Acknowledgements and references
- Funded by Natural Environment Research Council (award NE/S017380/1) as part of the Hydro-JULES programme
- References include MORECS v2.0 documentation, Richards (1971) on vapor pressure, and Robinson et al. (2023) on Hydro-PE and CHESS-met datasets