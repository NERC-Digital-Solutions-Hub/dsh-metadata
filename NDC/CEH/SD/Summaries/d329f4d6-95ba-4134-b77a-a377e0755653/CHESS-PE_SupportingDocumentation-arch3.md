# Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2012) [CHESS-PE]

## Overview
- Provides two daily potential evapotranspiration (PET) estimates on a 1 km resolution grid over Great Britain for 1961–2012.
- Derived from CHESS-met meteorological variables and CEH-GEAR precipitation.
- PET and PETI (interception-corrected PET) cover the same time and space extent.
- PET represents evaporation demand for a well-watered grass surface; PETI accounts for rainfall interception and canopy drying, yielding a more realistic evaporation potential on wet days.

## Data sources and inputs
- CHESS-met meteorological data: air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), surface air pressure (p*).
- CEH-GEAR precipitation data for PETI adjustments.
- PETI additionally uses rainfall data to model interception storage and its depletion over time.

## Variables and calculation
- PET (mm/day): Penman-Monteith estimation for a well-watered grass surface (standard FAO approach; stomatal resistance fixed at 70 s m⁻¹).
- PETI (mm/day): same Penman-Monteith calculation plus interception correction on wet days. Interception store S0 and total capacity Stot govern the interception component; PETI combines interception and transpiration with a dry-down dynamics model.
- PETI reduces to PET on days with no rainfall; on rainfall days, interception is added and subsequently diminishes as the interception store dries.

## File format and access
- Data distributed as CF-compliant netCDF files following CEH gridded dataset conventions.
- Monthly files, one per variable:
  - chess_pet_wwg_YYYYMM.nc
  - chess_peti_wwg_YYYYMM.nc
- Variables contained: pet (potential evaporation) and peti (potential evaporation with interception correction).
- Example: chess_peti_wwg_197206.nc contains PETI for June 1972.

## Metadata, provenance and documentation
- Full methodological details provided in Robinson et al. (in prep).
- Supporting documentation available via doi: 10.5285/80887755-1426-4dab-a4a6-250919d5020c.
- References include FAO guidelines (Allen et al. 1998), CEH-GEAR (Keller et al. 2015), Penman-Monteith fundamentals (Monteith 1965), and CHESS-met data (Robinson et al. 2015).

## Relevance for monitoring and policy decisions
- Enables high-resolution assessment of atmospheric evaporative demand across Great Britain for hydrological and ecological monitoring.
- Supports evaluation of water balance, drought risk, and land-surface process modelling at policy and planning levels.
- Demonstrates data provenance, standardization, and openness (netCDF/CF compliance; clear naming conventions) to facilitate data sharing, reproducibility, and governance.
- Highlights ongoing data quality considerations common in monitoring frameworks: metadata completeness, transformation needs, and ensuring datasets meet standards before public dissemination.