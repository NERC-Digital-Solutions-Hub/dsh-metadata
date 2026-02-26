# Supporting information

## Overview
- CHESS-PE: Climate hydrology and ecology research support system potential evapotranspiration dataset for Great Britain (1961-2017), providing two daily PET estimates on a 1 km grid.
- PET: Penman-Monteith potential evapotranspiration assuming a well-watered grass surface.
- PETI: PET with interception correction, accounting for canopy interception after rainfall and its daily drying; total daily PETI is the sum of interception and transpiration components.
- This release supersedes the 2016 version by extending years (to 2016-17), updating metadata, and applying bug fixes.

## Data products
- Variables: PET (mm/day) and PETI (mm/day).
- Spatial resolution: 1 km; temporal resolution: daily (reported via monthly netCDF files).
- Time coverage: 1961-2017 (with 2016-17 added in this release).
- PETI specifics: uses precipitation data to model interception store dynamics.

## Input data and sources
- PET inputs (CHESS-met): air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), surface air pressure (p*).
- PETI inputs: all PET inputs plus CHESS-met precipitation (CEH-GEAR) scaled to appropriate units.
- Data provenance: CHESS-met and CEH-GEAR datasets; metadata and references provided.

## Calculation methods and variables
- PET calculation: Penman-Monteith equation for a well-watered grass surface; assumes stomatal resistance of 70 s m^-1.
- PETI calculation: same core equation with interception corrections; includes an interception store (S0) and a total interception capacity (Stot); on wet days, E_I is computed with zero stomatal resistance; PETI combines interception and transpiration with dry-down dynamics.
- Documentation and full equations are described in Robinson et al. (2017, 2016) and related references.

## File format, data availability, and access
- Format: netCDF, CF-compliant, CEH gridded dataset conventions.
- Organization: monthly files, one file per variable.
- Availability: Environmental Information Data Centre; download via the CEH catalogue page.

## Data updates and release notes
- This release supersedes CHESS-PE (2016) with:
  - Extension to 2016-17.
  - Updated netCDF metadata for all years.
  - PET bug fix: humidity deficit limited to a minimum of zero (affects ~4% of data; mean PET up by ~0.001 mm/day).
  - PETI bug fix: interception correction overestimation corrected (affects ~63% of data; PETI decreased by ~0.02 mm/day overall; winter differences up to -4%, summer ~-1%).
- Changes may yield larger differences at specific timesteps/locations.

## Known issues and data quality considerations
- ArcGIS reading CF-compliant files with projected coordinate systems can offset layers by 10–100 m due to datum assumptions (WGS84); adjust layers using ArcGIS tools as needed.

## References
- Key references include FAO evapotranspiration guidelines, CEH-GEAR and CHESS metadata papers, and methodological foundational works (Monteith 1965; Allen et al. 1998; Robinson et al. 2017, 2016, 2020; Tanguy et al. 2019).