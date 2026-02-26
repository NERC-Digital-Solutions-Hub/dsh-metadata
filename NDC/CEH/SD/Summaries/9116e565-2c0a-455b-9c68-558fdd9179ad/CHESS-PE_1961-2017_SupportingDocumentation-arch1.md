# Supporting information

## Overview
- Documents the Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2017) [CHESS-PE], which provides two daily PET estimates on a 1 km resolution grid over Great Britain.
- Two variables: PET (Penman-Monteith PET for a well-watered grass surface) and PETI (PET with interception correction).

## Data and variables
- PET: Evapotranspiration demand calculated via Penman-Monteith assuming a well-watered grass surface (FAO standard).
- PETI: PET with interception correction, incorporating rainfall interception storage and its drying, adding a transpiration component as the interception store dries.

## Input data and methodology
- PET inputs: air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), surface air pressure (p*), all from CHESS-met.
- PETI inputs: all CHESS-met inputs plus CHESS-met precipitation (CEH-GEAR).
- Calculation: Penman-Monteith equation (E_P) with a fixed stomatal resistance (rs) of 70 s m-1 for grass; constants and framework follow Robinson et al. (2017) and FAO guidance (Allen et al., 1998).
- PETI calculation includes interception on wet days with an interception store S0 and total capacity; total PETI combines interception and transpiration with a dry-down exponential component.

## Data updates and improvements
- This release extends the dataset to 2016-2017 and updates all netCDF metadata relative to earlier versions.
- Bug fixes:
  - Humidity deficit (qs - qa) is constrained to a minimum of zero; ~4% of data affected; mean PET slightly increased (~0.001 mm/day, 0.1%).
  - PETI calculation corrected for overestimation of interception; affects ~63% of data; winter differences up to -4%, summer around -1%; overall PETI decreases by ~0.02 mm/day (about 1.5% of total).
- Some small numerical differences due to updated Python libraries; timestep- and location-specific variations may be larger.

## File format and data availability
- NetCDF format, CF-compliant, following CEH gridded dataset conventions.
- Data organized as monthly files, with separate files for each variable.
- Hosted by the Environmental Information Data Centre; downloadable via the provided CEH catalogue link.

## Known issues
- Reading CF-compliant files with projected coordinate systems in ArcGIS can misplace layers due to the datum assumption (WGS84). Adjust layers with ArcGIS tools; offset typically 10–100 m. Refer to ArcGIS documentation for guidance.

## References and context
- FAO Guidelines for computing crop evapotranspiration (Allen et al., 1998).
- CEH-GEAR precipitation dataset (Keller et al., 2015; Tanguy et al., 2019).
- Penman-Monteith framework and related methodological details (Monteith, 1965; Robinson et al., 2017; Robinson et al., 2020).
- CHESS-PE and CHESS-met data lineage and prior releases (Robinson et al., 2016; 2017; 2020).