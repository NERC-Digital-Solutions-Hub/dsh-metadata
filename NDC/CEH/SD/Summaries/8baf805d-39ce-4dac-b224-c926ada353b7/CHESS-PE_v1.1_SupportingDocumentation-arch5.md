# The Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2015) [CHESS-PE]

## Overview
- CHESS-PE provides two estimates of daily potential evapotranspiration on a 1 km grid over Great Britain for 1961–2015.
- Based on CHESS-met meteorological data and CEH-GEAR precipitation; two variables cover identical time and space extents.
- Full methodological details are available in Robinson et al. (in review).

## Data products (PET and PETI)
- PET (mm/day): Penman-Monteith potential evapotranspiration for a well-watered grass surface (FAO standard).
- PETI (mm/day): PET with interception correction, accounting for rainfall interception by canopy; on wet days, interception store is considered and dries through the day, affecting transpiration.

## Inputs and data provenance
- PET inputs: air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), and surface air pressure (p*), from CHESS-met.
- PETI inputs: all PET inputs plus CHESS-met precipitation (CEH-GEAR, scaled to appropriate units).
- Assumes well-watered grass surface with a constant stomatal resistance (rs) of 70 s m^-1 for the calculation basis.

## Calculation and methodological notes
- PET is calculated with the Penman-Monteith equation.
- PETI uses the same equation to compute potential transpiration, plus:
  - E_I (interception) computed on wet days by setting rs to zero.
  - Total PETI is an exponential dry-down model of interception with parameters S0 (initial interception store) and Stot (total interception store capacity).
- Key constants in the calculation include t_d, latent heat of vaporization, psychrometric constant, specific heat, air density, and other thermodynamic terms.
- The approach follows the well-established standard by FAO, with explicit assumptions:
  - Surface: vegetation is grass with reference conductance.
  - Interception dynamics modelled via EPI formulation.
- Full derivations and parameter choices are detailed in Robinson et al. (in review).

## File format and data access
- Data are distributed as CF-compliant netCDF files following CEH gridded dataset conventions.
- Data are stored as monthly files; there is one file per variable (PET and PETI).

## Data governance and usage considerations for Data Stewards
- Provenance: dataset links to CHESS-met and CEH-GEAR sources; clearly cite Robinson et al. and FAO guidelines.
- Standards and interoperability: CF-compliant netCDF with CEH conventions facilitates integration with other UK hydrology datasets.
- Metadata and documentation: ensure metadata captures variables, units (mm/day), spatial resolution (1 km), temporal coverage (1961–2015), input sources, and calculation assumptions (grass reference, rs=70 s/m for baseline).
- Data volume and management: high-resolution, long-term data; plan for storage, transfer, and access (monthly files per variable).
- Versioning and updates: note that full calculation details and potentially future updates are described in Robinson et al. (in review); track dataset version and any changes to input sources or parameters.
- Usage guidance: suitable for hydrological modelling, atmospheric evaporative demand analyses, and climate impact studies; PETI is particularly relevant where interception and canopy processes are important.

## References
- Allen, R. G., Pereira, L. S., Raes, D., and Smith, M. FAO guidelines for computing crop water requirements (FAO Irrigation and Drainage Paper, 1998).
- Keller, V. D. J., et al. CEH-GEAR precipitation dataset (Earth System Data, 2015).
- Monteith, J. L. Evaporation and environment (1965).
- Robinson, E. L., et al. CHESS-met meteorology dataset for Great Britain (2015).
- Robinson, E. L., et al. Trends in atmospheric evaporative demand in Great Britain (2016, in review).
- Tanguy, M., et al. Gridded UK rainfall estimates CEH-GEAR (2016).