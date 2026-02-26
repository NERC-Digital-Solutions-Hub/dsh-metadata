# The Climate hydrology and ecology research support system potential evapotranspiration dataset for Great Britain (1961-2019) [CHESS-PE]

## Overview
- Provides two daily potential evapotranspiration estimates on a 1 km grid for Great Britain, covering 1961–2019.
- Supersedes CHESS-PE (2020) by extending years to 2018–2019 and updating netCDF metadata.
- PET and PETI are derived from CHESS-met meteorology and CEH-GEAR precipitation data.

## Data and variables
- PET (mm/day): Penman–Monteith potential evapotranspiration for a well-watered grass surface (FAO standard).
- PETI (mm/day): PET with interception correction; accounts for rainfall interception by the canopy on wet days.
  - On wet days, interception store reduces transpiration; daily evaporation combines interception and transpiration with appropriate weighting.
- Inputs:
  - PET: from CHESS-met variables — air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), surface air pressure (p*).
  - PETI: same inputs plus CHESS-met precipitation (CEH-GEAR).
- Interception correction:
  - Uses an initial interception store S0 and total interception capacity Stot.
  - PETI calculation follows an exponential dry-down model for interception plus remaining PET.

## Calculation details
- PET calculation employs the Penman–Monteith equation (referencing Allen et al., 1998) with a fixed stomatal resistance of 70 s m⁻¹.
- PETI uses the same equation for E_P and adds E_I for interception on wet days, with E_I computed using zero stomatal resistance, and the total PETI combines interception dynamics with the residual PET.

## File format and data structure
- NetCDF format, CF-compliant, following CEH gridded data conventions.
- Monthly files; data are stored with one file per variable.

## Data availability
- Hosted by the Environmental Information Data Centre.
- Download at: https://catalogue.ceh.ac.uk/documents/8651771d-aa6d-4d0f-8bcd-b3be1f733852

## Known issues and caveats
- ArcGIS reading CF-compliant files with projected coordinate systems may offset layers by about 10–100 m due to the datum assumption being WGS 1984.
- Layers can be adjusted using ArcGIS tools to correct positioning; refer to ArcGIS documentation.

## Release context and references
- References include FAO guidelines (Allen et al., 1998), CEH-GEAR precipitation work (Keller et al., 2015; Tanguy et al., 2021), and Robinson et al. (2017, 2019, 2023) on CHESS datasets.