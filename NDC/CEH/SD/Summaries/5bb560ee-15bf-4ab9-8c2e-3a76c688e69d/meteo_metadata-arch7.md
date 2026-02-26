# Daily climate data combines data from several different sources for the Siksik catchment. Explanation of data sheet - meteo_data.csv

## Overview
- Daily climate dataset for the Siksik catchment in the North West Territories, Canada.
- Location details: Longitude 133°26'26" W, Latitude 68°44'17" N, Elevation 85 m.
- Catchment area approximately 1 km2; time zone: Mountain Standard Time.
- Data integrates multiple sources and includes both observed and derived variables.

## Data content and variables
- Date of record (dd/mm/yy).
- Tair: Mean daily air temperature (°C).
- Tmin / Tmax: Minimum and maximum daily air temperature (°C).
- RHmin / RHmax: Minimum and maximum daily relative humidity (%).
- u2: Wind speed at 10 m height (km/s).
- Tdew: Dew point temperature (°C).
- ea: Estimated actual vapour pressure (kPa) via FAO methods.
- P: Precipitation (mm).
- Rs: Estimated surface resistance (sm-1) via FAO method.
- albedo: Estimated albedo (dimensionless).
- PET: Potential evapotranspiration (mm/day) via Penman method.
- ddt: Degree-day temperature metric (mean daily temperature above 0°C) (°C).
- thaw_depth: Mean catchment thaw depth (m), estimated from observations and day-degree method.
- thaw_volume: Estimated thaw volume (mm) based on thaw depth.
- flow_m3s: Measured stream discharge at S2 (m3/s).
- flow_mm: Calculated stream runoff using contributing area (mm).
- stream_temp: Stream water temperature (°C).

Notes:
- NA indicates not applicable or missing data.
- Column headings may be presented in multiple variants (1/2/3) in the data sheet; the summary above captures the core variables.

## Data sources and methodology
- Meteorological data (temperature, humidity, wind, precipitation) sourced from http://climate.weather.gc.ca.
- Vapour pressure (ea) and surface resistance (Rs) estimated using FAO methods.
- PET estimated with Penman-Monteith method.
- Thaw depth and thaw volume derived from day-degree calculations; measured thaw depth referenced to measurements by Lorna Street.

## Data structure and preparation
- Data sheet referenced: meteo_data.csv.
- Clear explanations accompany column headings, units, and methodology for each variable.
- Data integrates observed measurements with standard meteorological calculations to produce GIS-ready climate variables.

## Data quality and considerations for GIS use
- Data combines multiple sources; expect potential gaps (marked as NA) and require careful data validation when integrating with other layers.
- Spatial applicability is focused on the Siksik catchment; temporal resolution is daily.
- Units are specified for each variable, ensuring consistency when creating map layers or time series in GIS.

## How to use in GIS
- Use coordinates and elevation to align with base maps and other spatial datasets.
- Create time-series rasters or vector-derived attributes for Tair, precipitation, PET, thaw parameters, and stream metrics.
- Utilize derived thaw depth/volume and PET for hydrological and permafrost analyses within the catchment.
- Validate and cross-check data against source metadata (climate.gc.ca, FAO methods, Penman-Monteith) during integration.

## Provenance and caveats
- Data provenance includes primary meteorological sources and established estimation methods (FAO, Penman-Monteith).
- Documentation notes and methodology are provided to support reproducibility and transparency in GIS analyses.