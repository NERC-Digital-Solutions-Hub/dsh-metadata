# The Climate hydrology and ecology research support system potential evapotranspiration dataset for Great Britain (1961-2019) [CHESS-PE]

## Overview
- CHESS-PE provides two daily potential evapotranspiration estimates on a 1 km grid over Great Britain for 1961–2019, with an extended coverage to 2018–2019 and updated metadata.
- Data are distributed as monthly netCDF files, with a separate file for each variable.
- The dataset is CF-compliant and follows CEH gridded dataset conventions.
- Aims to support GIS-based analysis and map-based data products for hydrology, ecology, and climate applications.

## Data and variables
- POTENTIAL EVAPOTRANSPIRATION (PET): Penman-Monteith PET for a well-watered grass surface (mm/day).
- PET with interception correction (PETI): PET adjusted for rainfall interception by canopy; includes interception storage dynamics.
- Spatial resolution: 1 km grid across Great Britain.
- Time coverage: 1961–2019 (with 2018–19 extension and updated metadata).
- Input data: derived from CHESS-met meteorological variables (air temperature Ta, specific humidity qa, downward longwave and shortwave radiation Ld and Sd, surface air pressure p*, etc.) and CHESS-met precipitation from CEH-GEAR (scaled to appropriate units).

## Calculation methods
- PET (EP): calculated using the Penman-Monteith equation for a well-watered grass surface; follows established standard assumptions (stomatal resistance around 70 s/m).
- PETI (EPI): uses the same PET calculation plus an interception component on wet days, with an exponential dry-down of interception storage; outputs daily PETI values.
- Full methodological details and references are provided (e.g., Monteith 1965; Allen et al. 1998; Robinson et al. 2017).

## Data format and structure
- File format: netCDF, CF-compliant, CEH gridded conventions.
- Data organization: monthly files; separate netCDF file for each variable (PET and PETI).

## Data availability and access
- Hosted by the Environmental Information Data Centre (EIDC).
- Downloadable from the CEH data catalogue (link provided in the dataset documentation).

## Known issues and considerations for GIS users
- ArcGIS reading issue: when using CF-compliant files with projected coordinate systems, ArcGIS assumes the WGS 1984 datum, which can cause a positional offset (approximately 10–100 m) for CHESS-PE data with a different datum. Layers can be adjusted with ArcGIS tools to align correctly; refer to ArcGIS documentation for details.

## Practical relevance for GIS specialists
- Enables high-resolution mapping and spatial analysis of atmospheric evaporative demand (PET, PETI) across GB for hydrological and ecological modelling.
- Facilitates integration with CEH-GEAR precipitation and other CHESS datasets for composite hydrological models.
- Supports creation of map-based decisions and policy visuals requiring consistent, gridded evapotranspiration estimates.
- The 1 km resolution and CF-netCDF format streamline integration into standard GIS workflows and data pipelines.