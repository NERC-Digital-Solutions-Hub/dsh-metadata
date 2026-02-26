# Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2015) [CHESS-PE]

- Provides two daily potential evapotranspiration (PET) estimates on a 1 km resolution grid over Great Britain, for 1961–2015.
- Derived from the CHESS-met meteorological variables and CEH-GEAR precipitation; two variables cover the same time and spatial extent.

## Variables

- PET (mm/day): Penman–Monteith PET for a well-watered grass surface (FAO standard).
- PETI (mm/day): PET with interception correction, accounting for rainfall interception by canopy and its drying during the day.

## Calculation and assumptions

- PET uses the Penman–Monteith equation with inputs from CHESS-met: air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), and surface air pressure (p*). Assumes a well-watered grass surface with stomatal resistance of 70 s m⁻¹.
- PETI adds interception processes:
  - On wet days, potential interception (Ei) is calculated with zero stomatal resistance.
  - PETI is the sum of interception evaporation and transpiration, with interception forced to dry down over time.
  - Interception is modelled using an initial store S0 and total store capacity Stot.

## Input data

- PET: derived from CHESS-met variables Ta, qa, Ld, Sd, p*.
- PETI: uses the same CHESS-met variables plus CHESS-met precipitation (CEH-GEAR), scaled to appropriate units.

## Data format and access

- NetCDF format, CF-compliant, following CEH gridded dataset conventions.
- Data stored as monthly files; one file per variable (PET and PETI).

## Geographic scope and resolution

- Great Britain at 1 km resolution.

## Usage for GIS and analysis

- Suitable for map-based visualisations and spatial analyses in GIS.
- Useful for hydrological and ecological modelling, allowing comparisons between PET and PETI across space and time.

## References

- FAO Guidelines for computing crop water requirements (Allen et al., 1998).
- CEH-GEAR: gridded rainfall estimates for the UK (Keller et al., 2015; Tanguy et al., 2016).
- Penman (Monteith, 1965) and related CHESS-met dataset documentation (Robinson et al., 2015; in review, 2016).