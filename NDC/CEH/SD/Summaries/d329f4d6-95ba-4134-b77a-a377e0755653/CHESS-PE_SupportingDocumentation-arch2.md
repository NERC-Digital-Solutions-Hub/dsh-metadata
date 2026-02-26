# Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2012) [CHESS-PE]

## Overview
- Provides two daily potential evapotranspiration (PET) estimates on a 1 km grid over Great Britain for 1961–2012.
- Derived from CHESS-met meteorological data and CEH-GEAR precipitation.
- PET and PETI cover the same time period and extent; PET is the standard FAO-defined reference, PETI includes interception effects.

## Data and variables
- PET (mm/day): Penman-Monteith PET for a well-watered grass surface.
- PETI (mm/day): PET with interception correction; includes rainfall interception and subsequent canopy drying dynamics.
- PET and PETI are daily values, available on a 1 km grid.

## Input data sources
- CHESS-met: temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), surface air pressure (p*).
- CEH-GEAR precipitation: daily areal rainfall estimates, used to compute PETI.

## Calculation methods
- PET calculation: Penman-Monteith equation assuming a well-watered grass surface; stomatal resistance fixed at 70 s m⁻¹.
- PETI: uses the same PET equation plus interception components; interception store initialized (S0) and modeled with exponential drying toward total store (Stot).
- PET represents atmospheric evaporative demand; PETI accounts for canopy interception effects on days with rainfall.

## File format and access
- Data distributed as netCDF (CF-compliant) files following CEH gridded dataset conventions.
- Monthly files per variable:
  - chess_pet_wwg_<year><month>.nc
  - chess_peti_wwg_<year><month>.nc
- Example: chess_peti_wwg_197206.nc contains PETI data for June 1972.

## Provenance and references
- Key sources: Robinson et al. (CHESS-met), Tanguy et al. (CEH-GEAR), Allen et al. (FAO guidelines), Monteith (1965).
- Supporting documentation and DOIs provided for dataset lineage and methods.

## Use in environmental monitoring
- Enables consistent assessment of atmospheric evaporative demand across Great Britain over 1961–2012.
- Useful for hydrological and ecological modelling, climate impact analyses, and trend assessments.
- Facilitates integration with other environmental data to monitor policy performance and environmental health over time.

## Limitations and caveats
- PETI relies on interception modeling with assumptions about initial interception store (S0) and drying dynamics.
- PET assumes a standard grass surface; outputs depend on land surface representation and input data accuracy (CHESS-met and CEH-GEAR).
- Temporal coverage limited to 1961–2012 for GB.