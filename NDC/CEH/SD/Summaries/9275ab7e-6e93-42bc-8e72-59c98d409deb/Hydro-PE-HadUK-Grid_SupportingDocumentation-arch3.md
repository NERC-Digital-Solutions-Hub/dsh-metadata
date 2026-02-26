# Potential evapotranspiration derived from HadUK-Grid 1km gridded climate observations 1969-2021 (Hydro-PE HadUK-Grid) Supporting information

## Overview
- Gridded daily potential evapotranspiration (PET) and PET with interception correction (PETI) on 1 km UK grid for 1969–2021.
- PET and PETI derived from the HadUK-Grid meteorological dataset using the Penman-Monteith approach parameterised for well-watered grass.
- PET uses daily mean values; PETI adds interception correction on days with precipitation.
- Two input HadUK-Grid versions: v1.0.3.0 (1969–2020) and v1.1.0.0 (2021); no differences between versions for the variables used in 1969–2020.
- Units: kg m^-2 d^-1, equivalent to mm d^-1.

## Data and variables
- PET (kg m^-2 d^-1) and PETI (kg m^-2 d^-1).
- Input data (HadUK-Grid) for 1969–2021 on a 1 km grid:
  - Monthly mean water vapour pressure (pv, hPa)
  - Monthly mean sea level pressure (psl, hPa)
  - Monthly total sunshine hours (sun, hours)
  - Monthly mean wind speed at 10 m (sfcWind, m s^-1)
  - Daily max temperature (tasmax, °C)
  - Daily min temperature (tasmin, °C)
  - Daily precipitation (P, mm d^-1) for PETI
- Ancillary data: surface altitude (m) and Ångström coefficients a, b, c.
- Time coverage: HadUK-Grid inputs span 1862–2021; calculations use data available from 1969 onwards.
- Interpolation to daily time-step uses quadratic interpolation; monthly values are treated as the 15th of the month.

## Calculation approach (Penman-Monteith)
- PET calculated via Penman-Monteith for a well-watered short grass surface.
- Key inputs derived from HadUK-Grid data:
  - Daily mean temperature from tasmax and tasmin (with a specific pairing rule across days for consistency with rainfall timespan).
  - Specific humidity at saturation, air density, and humidity gradients derived from temperature and pressure.
  - Net radiation as the sum of net shortwave and net longwave, computed from sunshine hours, temperature, and water vapour pressure following MORECS v2.0 conventions.
  - Aerodynamic resistance as a function of wind speed; canopy resistance based on leaf area index; stomatal resistance components included.
  - Ground heat flux treated as a monthly mean.
- Parameterisation aligned with MORECS v2.0 documentation; constants and relations chosen for a well-watered grass surface.
- PETI corrections based on interception by a canopy, using a function of precipitation and leaf area index; interception rate adjusted during spring–autumn for multiple daily precipitation events.

## Interception correction
- PETI on days with no precipitation equals PET.
- On days with precipitation, PETI accounts for canopy interception:
  - Interception water CI depends on precipitation and leaf area index.
  - Evaporation from intercepted water EI is calculated with r_s set to zero (open water potential evaporation) and continued until the canopy is dry, then PET is resumed.
  - Formula for PETI combines PET, CI, EI, and E_P with a conditional structure to reflect whether interception capacity is exceeded.

## Interpolation and data handling
- Quadratic interpolation of monthly variables to daily resolution; monthly values treated as representing the 15th of each month.
- Extrapolation at ends can occur; negative pv or sun values are reset to zero.
- To avoid inconsistencies when new years are added, the last year of already-interpolated daily data is joined with new monthly data and interpolated on that combined series, preserving end-of-old-timespan data but creating continuity with new data. The end-of-timespan data may still be based on extrapolation.

## File format, spatial and time information
- Data distributed as NetCDF files, CF Metadata Conventions v1.8 and ACDD v1-3.
- Time: daily mean values from 1969-01-01 to 2021-12-31; interpolation assumes mid-month timestamps.
- Spatial: 1 km resolution, British National Grid (EPSG:27700); WGS84 coordinates (EPSG:4326) provided as well.
- Known data-compatibility note: ArcGIS may offset projected-datum layers because it assumes WGS84; adjustments may be needed for correct positioning.

## Use, governance, and caveats for monitoring frameworks
- Purpose: supports hydrological modelling and environmental health monitoring; PETI aligns with established MORECS v2.0 methodologies.
- Data provenance and structure enable traceability (netCDF CF-compliant, documentation of input sources and processing steps).
- Potential data governance considerations:
  - Data quality and metadata completeness are addressed through detailed input descriptions and processing steps; however, some metadata gaps can create verification barriers.
  - Public sharing of underlying data is supported by the CF-compliant NetCDF format, but users should be aware of the ArcGIS datum issue and interpolation-induced changes over time as new data are added.
  - Data updates (new years) may alter daily values in the old time span due to the quadratic interpolation over the updated full series; the chosen interpolation strategy mitigates major discontinuities while preserving continuity at the old endpoint.

## Acknowledgements and references
- Supported by Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme.
- Key references: MORECS v2.0; HadUK-Grid data development; EU-DEM; Brutsaert (long-wave radiation), Linacre (net radiation), and related foundational works used to derive radiation and evapotranspiration components.