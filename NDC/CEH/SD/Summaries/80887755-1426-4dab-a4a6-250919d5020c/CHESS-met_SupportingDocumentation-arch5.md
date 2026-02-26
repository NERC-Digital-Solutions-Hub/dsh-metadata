# Climate hydrology and ecology research support system meteorology dataset (1961-2012) [CHESS-met] provides daily meteorological variables on a 1km grid over Great Britain

## Overview
- Provides daily meteorological variables on a 1km grid over Great Britain for 1961–2012 to support the Joint UK Land Environment Simulator (JULES) with daily disaggregation.

## Data sources and inputs
- Met Office MORECS dataset: daily mean air temperature, vapour pressure, hours of bright sunshine, wind speed.
- CRU TS 3.21: daily temperature range.
- WATCH Forcing Data: air pressure.
- IHDTM: 50 m resolution elevation data.
- UK Energy Technology Support Unit (ETSU): 1 km mean wind speeds.

## Variables and units
- tas: air temperature (Kelvin)
- huss: specific humidity (kg kg⁻¹)
- sfcWind: wind speed (m s⁻¹)
- rlds: downward longwave radiation (W m⁻²)
- rsds: downward shortwave radiation (W m⁻²)
- precip: precipitation (kg m⁻² s⁻¹)
- psurf: surface air pressure (Pa)
- dtr: daily temperature range (K)

Notes:
- All variables (except daily temperature range) are daily means from 09:00 GMT to 09:00 GMT the next day.
- Temperature and humidity are referenced at 1.2 m height; wind at 10 m; pressure adjusted for 1 km elevation.

## Data processing and methods
- Precipitation scaled from CEH-GEAR daily totals (mm/day) to kg m⁻² s⁻¹.
- Ta created by bicubic-spline interpolation of MORECS temperature, then elevation adjustment using IHDTM (1 km grid). qa derived from interpolated vapour pressure; elevation-adjusted.
- MoreCS sunshine hours used to derive cloud cover factor; used to compute Sd and Ld, with Sd corrected for slope and aspect.
- Wind speed 10 m interpolated from MORECS, then adjusted using long-term ETSU wind speed means.
- Psess (psurf) produced as a mean-monthly WFD climatology, adjusted for 1 km elevation.
- DTR reprojected from CRU TS 3.21 (0.5°) monthly data with no spatial interpolation.

## File formats and naming
- Distributed as netCDF files, CF-compliant, following CEH gridded dataset conventions.
- Variables named: tas, huss, sfcWind, rlds, rsds, precip, psurf, dtr.
- Original download format: monthly files per variable.
- Accessible via Order Manager; subsets contain all variables and the required temporal/spatial aggregation.

## Temporal and spatial resolution
- 1 km grid covering Great Britain.
- Daily data for 1961–2012 (09:00 GMT to 09:00 GMT the next day).

## Data governance, provenance, and usability
- Compilation from multiple established data sources with documented processing steps.
- Detailed methodology described (Robinson et al., in prep) with full references provided.
- Emphasis on standard formats, metadata, and subset delivery to enhance discoverability, reuse, and governance of the dataset.