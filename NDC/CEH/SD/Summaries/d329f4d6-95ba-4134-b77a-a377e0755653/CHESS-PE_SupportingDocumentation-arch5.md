# Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2012) [CHESS-PE]

## Overview
- Provides two daily potential evapotranspiration estimates on a 1 km resolution grid over Great Britain for 1961–2012.
- Derived from CHESS-met meteorological variables and CEH-GEAR precipitation; two ET variables cover the same time and space:
  - PET: Penman-Monteith potential evapotranspiration for a well-watered grass surface.
  - PETI: PET with interception correction, accounting for rainfall interception and canopy drying.

## Data content and variables
- PET (mm/day): Evapotranspiration under a well-watered grass assumption.
- PETI (mm/day): PET adjusted for interception losses; on wet days, interception store influences transpiration.
- Both variables share identical temporal and spatial coverage (daily values on a 1 km grid for Great Britain).

## Input data and data sources
- CHESS-met meteorological variables: air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), surface air pressure (pa).
- CEH-GEAR precipitation (rainfall) data used in PETI calculations.
- Key sources and context:
  - Robinson et al. (2015): CHESS-met dataset.
  - Tanguy et al. (2014); Keller et al. (2015): CEH-GEAR precipitation.
  - FAO guidelines (for the standard PET calculation framework).

## Calculation and methodology
- PET (E_P) is calculated using the Penman-Monteith equation with:
  - Grass surface assumption and a constant stomatal resistance (r_s) of 70 s m^-1.
  - Standard constants (latent heat, cp, air density, psychrometric constant, etc.).
- PETI (E_PI) uses the same equation for PET, plus:
  - On wet days, an interception component is computed by temporarily setting stomatal resistance to zero to estimate interception evaporation (E_I).
  - PETI combines interception evaporation and PET with an exponential dry-down of the interception store (S0, Stot) to produce total PETI.
- FAO-standard reference surface and methodologies underpinning both PET and PETI.

## File format, organization, and access
- File format: netCDF, CF-compliant, following CEH gridded dataset conventions.
- Organization: monthly files for each variable.
- File naming: chess_<var>_wwg_<year><month>.nc
  - <year> between 1961 and 2012; <month> between 01 and 12.
  - Variables:
    - pet: potential evapotranspiration
    - peti: potential evapotranspiration with interception correction
- Example: chess_peti_wwg_197206.nc contains PETI data for June 1972.

## Provenance and documentation
- Full methodology and calculation details are described in the associated documentation and references:
  - Robinson, Blyth, Clark, Finch, and Rudd (2015): CHESS-met dataset.
  - Robinson et al. (in prep): Trends in evaporative demand in Great Britain using high-resolution meteorological data.
  - Tanguy et al. (2014); Keller et al. (2015): CEH-GEAR precipitation.
  - FAO (1998): Guidelines for computing crop water requirements (reference for PET framework).
- Data are documented with DOIs and are intended for hydrological and ecological applications.

## Data quality, limitations, and governance considerations
- Assumptions and limitations:
  - PET relies on a fixed grass surface and fixed stomatal resistance (70 s m^-1).
  - PETI includes interception dynamics with parameters S0 and Stot; interception modeling adds complexity on wet days.
  - PETI requires precipitation inputs and interception store parameters, which introduce potential uncertainty on rainfall days.
- Governance and stewardship aspects:
  - Data are organized for discoverability and reuse (CF-compliant, standardized naming).
  - Documentation and references support provenance and reproducibility.
  - Suitable for inclusion in data catalogs with metadata describing inputs, methods, and assumptions; clearly specify usage scope (hydrological/ecological modelling) and citations.