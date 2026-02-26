# Potential evapotranspiration derived from HadUK-Grid 1km gridded climate observations 1969-2021 (Hydro-PE HadUK-Grid) Supporting information

## Overview
- Gridded potential evapotranspiration (PET) calculated from the HadUK-Grid 1km UK climate dataset for 1969–2021.
- Two PET variables: daily total PET (kg m-2 d-1) and daily total PET with interception correction (PETI; kg m-2 d-1).
- PET uses the Penman-Monteith equation parameterised for a well-watered grass surface; PETI adds interception correction on days with precipitation.
- PET and PETI align with MORECS v2.0 parameterisations to ensure historical consistency.
- Data derived from HadUK-Grid v1.0.3.0 (1969–2020) and v1.1.0.0 (2021); no differences between versions for the variables used in 1969–2020.

## Input data (2.1)
- HadUK-Grid on a 1 km UK grid (v1.0.3.0 for 1969–2020 and v1.1.0.0 for 2021), interpolated from station observations to grid points.
- Timespan overall: 1862–2021 (start depends on variable); PET-related variables required from 1969 onward.
- Variables used for PET and PETI:
  - Monthly means: water vapour pressure (pv), sea level pressure (psl), sunshine hours (sun), wind speed at 10 m (u10)
  - Daily: daily max/min air temperature at 1.5 m (tasmax, tasmin)
  - Daily precipitation (P) for PETI
- Ancillary data: surface altitude (EU-DEM v1.1), Ångström coefficients (a, b, c)
- Temporal processing: monthly values interpolated to daily with quadratic interpolation to produce a contiguous daily timeseries.

## Penman-Monteith calculation (2.2)
- PET is computed with the Penman-Monteith equation, using a well-watered short grass parameterisation and adjustments to net longwave radiation to match surface temperature.
- Inputs derived from HadUK-Grid:
  - Daily mean temperature from tasmax and tasmin (with day-boundary handling)
  - Specific humidity, air density
  - Net radiation (sum of net shortwave and net longwave; derived via MORECS v2.0 approaches)
  - Aerodynamic resistance as a function of wind speed; canopy/stomatal resistance via leaf area index
- Consistency with MORECS v2.0 is maintained for parameters and formulations.
- Intermediates include: surface altitude adjustments for pressure, net radiation components, and derived humidity/air properties.

## Interception correction (2.3)
- PETI differs from PET on days with precipitation (P > 0) due to canopy interception.
- Interception water CI and evaporation EI are computed; EI is treated as open-water evaporation (r_s = 0) and scaled until the canopy is dry.
- Interception correction logic:
  - If P > 0 and CI ≥ EI: EI replaces PETI
  - If P > 0 and CI < EI: PETI = PET + CI (1 - PET/EI)
  - If P = 0: PETI = PET
- Spring/summer/autumn enhancements to CI account for multiple precipitation events per day.

## Interpolation details (2.4)
- Monthly variables are interpolated to daily using quadratic interpolation, treating the 15th of each month as the timestamp.
- Extrapolation can occur at ends; negative pv or sun from interpolation are set to zero.
- To avoid inconsistencies when new yearly data are added, the last year of already-interpolated daily data is combined with new monthly data, and interpolation is performed on this extended series, preserving continuity at the end of the old timeseries.

## File format (3)
- Data stored as netCDF files, CF v1.8 conventions and ACDD v1-3.
- Daily mean values; monthly files for each variable.
- Typical file naming structure referenced, with variable name and year (e.g., pet or peti, year).

### Spatial information (3.1)
- 1 km resolution, aligned to the British National Grid (BNG), EPSG:27700.
- Longitude/latitude provided in WGS84 (EPSG:4326).
- Note: ArcGIS may offset layers due to datum handling; adjust if necessary.

## Time information (3.2)
- Daily mean values from 1969-01-01 to 2021-12-31.
- Monthly variables interpolated with a mid-month timestamp.

## Acknowledgements (4)
- Funded by the Natural Environment Research Council (grant NE/S017380/1) as part of the Hydro-JULES programme.

## References (5)
- MORECS v2.0 methodology and documentation (Hough et al., 1995; related materials)
- HadUK-Grid dataset description (Hollis et al., 2018/2019)
- EU-DEM elevation data
- Supporting methodological references for net radiation and related PET components (Brutsaert 1975; Linacre 1968; Richards 1971; and other related works)