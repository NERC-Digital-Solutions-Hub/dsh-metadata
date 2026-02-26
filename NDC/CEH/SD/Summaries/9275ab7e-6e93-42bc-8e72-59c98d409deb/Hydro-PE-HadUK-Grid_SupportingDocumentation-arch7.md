# Potential evapotranspiration derived from HadUK-Grid 1km gridded climate observations 1969-2021 (Hydro-PE HadUK-Grid) Supporting information

## Overview
- Gridded daily potential evapotranspiration (PET) and PET with interception correction (PETI) on a 1 km UK grid for 1969–2021.
- PET calculated with Penman-Monteith for a well-watered grass surface; PETI includes canopy interception corrections on days with precipitation.
- Data are derived from HadUK-Grid meteorological datasets (v1.0.3.0 for 1969–2020 and v1.1.0.0 for 2021; no differences between versions for overlapping period).
- PET and PETI units: kg m^-2 d^-1 (equivalent to mm d^-1).

## Data and input variables
- Input dataset: HadUK-Grid v1.0.3.0 (1969–2020) and v1.1.0.0 (2021) on a 1 km UK grid.
- Required variables (monthly): 
  - pv (mean water vapour pressure), psl (mean sea level pressure), sun (monthly sunshine hours), sfcWind (wind speed at 10 m), tasmax (daily max temp, 1.5 m), tasmin (daily min temp, 1.5 m).
- Additional inputs for PETI: daily precipitation (P, rainfall in mm d^-1).
- Ancillary data: surface altitude (EU-DEM v1.1), Ångström coefficients a, b, c.
- Monthly data are interpolated to daily using quadratic interpolation; timeseries are kept contiguous when new years are added.

## Calculation methods
- PET (kg m^-2 d^-1) computed via Penman-Monteith, parameterised for well-watered grass; uses daily mean temperature and interpolated daily values for other variables.
- Key derivations from HadUK-Grid inputs: daily mean temperature (average of tasmax and tasmin with specific handling around day boundaries), specific humidity at saturation, air density, total net radiation (from net shortwave and net longwave radiation via MORECS v2.0 relationships), aerodynamic and canopy resistances.
- Alignment with MORECS v2.0: parameter choices and formulations used to ensure compatibility with historical methods.
- Interception correction (PETI): on days with P > 0, canopy interception water (CI) is calculated from rainfall and leaf area index (LAI); PETI is PET adjusted by interception dynamics, with enhanced interception in spring–autumn to account for multiple events per day. If CI >= EI, PETI = EI; if CI < EI, PETI = PET + CI(1 - PET/EI); if no rain, PETI = PET.

## Interpolation and temporal consistency
- Quadratic interpolation to daily resolution assumes the 15th of each month as representative; extrapolation at ends may occur.
- To avoid updates causing shifts in already interpolated data, the last year of existing daily data is kept with new monthly data, and interpolation is performed on the combined series to maintain continuity.

## File format and spatial/time information
- Format: netCDF files following CF Metadata Conventions v1.8 and ACDD v1-3; one monthly file per variable (PET or PETI) and per year.
- File naming: structured as {VARN}_{YEAR}.nc (e.g., pet_1969.nc, peti_1999.nc).
- Spatial grid: 1 km resolution, aligned to the British National Grid (BNG), EPSG:27700; coordinates in metres (eastings/northings). WGS84 lat/lon (EPSG:4326) provided as well.
- Time coverage: daily mean values from 1969-01-01 to 2021-12-31; monthly inputs are represented by mid-month timestamps during interpolation.

## Practical notes for use in GIS
- PET and PETI are suitable for hydrological modelling and climate analyses where daily areal evapotranspiration estimates are required at high spatial resolution.
- File format and projection details facilitate integration into GIS workflows; be aware of a known ArcGIS offset issue with CF-projected files and the need to adjust datum alignment if using ArcGIS.
- PETI provides an interception-corrected ET signal, aligning with MORECS v2.0 methodologies for canopy interception.

## Acknowledgements and references
- Supported by Natural Environment Research Council (NE/S017380/1) as part of the Hydro-JULES programme.
- References include MORECS v2.0 documentation and HadUK-Grid data series, among others.