# Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2012) [CHESS-PE]

## Overview
- Provides two daily potential evapotranspiration (PET) estimates on a 1 km resolution grid over Great Britain.
- Derived from CHESS-met meteorological variables and CEH-GEAR precipitation.
- Time extent: 1961–2012; both PET and PETI cover the same daily time steps and spatial extent.
- Data format: CF-compliant netCDF files, following CEH gridded dataset conventions.

## Data coverage and structure
- Spatial coverage: Great Britain.
- Spatial resolution: 1 km.
- Temporal coverage: 1961–2012 (daily PET values).
- File organization: monthly netCDF files for each variable.
  - File naming: chess_<var>_wwg_<year><month>.nc
  - Example: chess_peti_wwg_197206.nc contains PETI data for June 1972.

## Variables and definitions
- PET (mm/day): Penman-Monteith potential evapotranspiration calculated for a well-watered grass surface (FAO standard).
- PETI (mm/day): PET with interception correction; accounts for rainfall interception by the canopy and its daily drying, combining interception and transpiration components.

## Calculation methodology
- Base equation: Penman-Monteith (EP) using meteorological inputs (Ta, qa, downward radiation, surface pressure) with fixed stomatal resistance (70 s m⁻¹) and grass surface assumptions.
- PET (PET): standard Penman-Monteith computation for well-watered grass.
- PETI: uses the same EP calculation but includes interception effects:
  - Interception store dynamics modeled with initial store S0 and total capacity Stot.
  - On wet days, interception evaporation is computed by making stomatal resistance effectively zero for the interception component.
  - PETI combines interception and transpiration with an exponential dry-down of interception.

## Input data
- CHESS-met meteorological variables:
  - Air temperature (Ta)
  - Specific humidity (qa)
  - Downward longwave and shortwave radiation (Ld, Sd)
  - Surface air pressure (p*)
- Precipitation input for PETI:
  - CHESS-met precipitation, scaled appropriately (CEH-GEAR data: Tanguy et al., 2014; Keller et al., 2015).

## File format and data standards
- Data format: netCDF, CF-compliant, CEH gridded dataset conventions.
- Data organization: monthly files per variable.
- Variable names inside files: pet (PET) and peti (PETI).

## Practical notes for GIS specialists
- Suitable for map-based analyses of atmospheric evaporative demand and hydrological modelling.
- The 1 km resolution enables detailed spatial analysis across varied GB landscapes.
- Daily PET and PETI provide opportunities to assess interception effects and water demand under different rainfall regimes.
- Data can be integrated into GIS workflows via standard netCDF readers; references provide detailed methodological context.

## References and sources
- Allen, R. G., Pereira, L. S., Raes, D., and Smith, M. (1998) FAO guidelines for computing crop water requirements.
- Keller, V. D. J., et al. (2015) CEH-GEAR: gridded rainfall estimates for the UK.
- Monteith, J. L. (1965) Evaporation and environment.
- Robinson, E. L., et al. (2015) CHESS-met dataset for Great Britain (1961–2012).
- Tanguy, M., et al. (2014) CEH-GEAR rainfall dataset.
- Additional Robinson et al. (in preparation) on trends in evaporative demand.