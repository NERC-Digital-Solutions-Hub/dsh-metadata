# Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2012) [CHESS-PE]

## Overview
- Provides two daily potential evapotranspiration (PET) estimates on a 1 km resolution grid across Great Britain for 1961–2012.
- Derived from CHESS-met meteorological variables and CEH-GEAR precipitation; two variables cover the same time span and space.
- PET is the Penman-Monteith PET for a well-watered grass surface (FAO standard).
- PETI is PET with interception correction, accounting for rainfall interception and canopy interception dynamics.
- Data are CF-compliant netCDF files distributed monthly for each variable.

## What data are provided
- PET (mm/day): Penman-Monteith PET for a well-watered grass surface.
- PETI (mm/day): PET with interception correction, incorporating rainfall interception and a drying interception store.

## Input data and variables
- PET inputs: air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), surface air pressure (p*), from CHESS-met.
- PETI inputs: all PET inputs plus CHESS-met precipitation (CEH-GEAR rainfall) scaled to appropriate units.

## Calculation and methodology
- PET calculation: uses the Penman-Monteith equation, assuming a well-watered grass surface, with stomatal resistance typically fixed (rs = 70 s/m).
- PETI calculation: identical PET basis plus interception correction; on wet days calculate interception E I with zero stomatal resistance; PETI combines interception and transpiration with an exponential dry-down of the interception store (parameters S0 and Stot).
- FAO reference standard followed for PET; PETI represents interception-modified evaporation.
- Key constants: latent heat λ = 2.5 × 10^6 J kg^-1; cp = 1010 J kg^-1 K^-1; γ = 0.004 K^-1.

## File format and data organization
- Data are distributed as netCDF files, CF-compliant, following CEH gridded dataset conventions.
- Monthly files for each variable:
  - chess_<var>_wwg_<year><month>.nc
  - <var> = pet or peti
- Example: chess_peti_wwg_197206.nc contains PETI for June 1972.

## Example and provenance
- Example file name format provided to locate monthly data easily (e.g., chess_peti_wwg_197206.nc).
- References and provenance include CHESS-met, CEH-GEAR, and FAO guidelines; key sources include Robinson et al. (CHESS-met), Tanguy et al. (CEH-GEAR), and Monteith (1965).

## Practical notes for use
- PET indicates atmospheric evaporative demand under well-watered grass assumptions; PETI is useful when modelling interception effects after rainfall.
- Suitable for hydrological and ecological modelling in Great Britain; data are provided at high spatial resolution (1 km) and long temporal coverage (1961–2012).
- Users should consider the land-surface assumptions and the interception dynamics when selecting between PET and PETI for their models.