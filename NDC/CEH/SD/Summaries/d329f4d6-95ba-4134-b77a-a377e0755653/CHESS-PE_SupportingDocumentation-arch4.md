# Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2012) [CHESS-PE]

## Overview
- Provides two daily potential evapotranspiration estimates on a 1 km grid over Great Britain for 1961–2012.
- Derived from CHESS-met meteorological variables and CEH-GEAR precipitation data; full details available in Robinson et al. (in prep).
- Two PET variants accommodate different modelling needs:
  - PET: Penman-Monteith PET for a well-watered grass surface.
  - PETI: PET with interception correction, accounting for rainfall interception and canopy drying.

## What’s in the dataset
- PET (mm/day): PET assuming a well-watered grass surface (FAO standard).
- PETI (mm/day): PET with interception correction; on days with rainfall, rainfall adds to an interception store that inhibits transpiration, with a dynamic dry-down of interception.
- Temporal extent: daily values from 1961 to 2012.
- Spatial resolution: 1 km grid across Great Britain.
- File contents: two variables (pet and peti) stored in monthly netCDF files.

## Calculation methods
- PET calculation: Penman-Monteith equation using meteorological inputs; assumes grass surface with stomatal resistance of 70 s m^-1.
- PETI calculation: same equation for EP; on wet days, calculates interception by setting stomatal resistance to zero; total PETI combines interception storage and PET with a dry-down dynamics (exponential decay).
- Inputs:
  - CHESS-met variables: air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), surface air pressure (p*).
  - For PETI: CHESS-met precipitation (CEH-GEAR precipitation).
- Documentation: full calculation details in Robinson et al. (in prep); references include FAO guidelines and MONTEITH (1965).

## Data format and structure
- File format: netCDF, CF-compliant, following CEH gridded dataset conventions.
- Organization: monthly files, one per variable.
- File naming: chess_<var>_wwg_<year><month>.nc
  - Example: chess_peti_wwg_197206.nc contains PETI for June 1972.
- Variables: pet (potential evapotranspiration) and peti (PET with interception correction).

## Provenance, sources, and references
- Primary inputs: CHESS-met meteorological dataset; CEH-GEAR gridded precipitation dataset.
- Key references:
  - FAO (1998) guidelines for crop evapotranspiration.
  - Keller et al. (2015) CEH-GEAR dataset.
  - Monteith (1965) and Robinson et al. (2015) for CHESS-met context.
- DOI for CHESS-PE resource: 10.5285/80887755-1426-4dab-a4a6-250919d5020c
- Supporting documentation and data lineage available through associated data centre pages and Robinson et al. (in prep).