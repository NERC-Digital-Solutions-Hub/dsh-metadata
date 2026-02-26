# Meteo_data.csv – Daily climate data for the Siksik catchment, North West Territories, Canada

## Overview
- Provides daily climate data for the Siksik catchment, combining information from several sources.
- Includes derived metrics (thaw depth, thaw volume, stream discharge/runoff) and water temperature.
- Data are intended to support assessment of environmental conditions and policy/research performance over time.
- Methods rely on established FAO and Penman-Monteith approaches; thaw metrics use a day-degree method.
- Notes indicate missing data with NA.

## Location and data scope
- Site: Siksik catchment
- Country: Canada
- State/Region: North West Territories
- Coordinates: Long 133°26'26" W, Lat 68°44'17" N
- Elevation: 85 m
- Watershed area: ~1 km²
- Time zone: Mountain Standard Time
- Data sheet: meteorological data for Siksik catchment; daily climate data from multiple sources
- Daily data are organized around the meteo_data.csv sheet and accompany an explanation document

## Data content and variables (columns, units, methodology)
- date: Date of record (dd/mm/yy)
- Tair: Mean daily air temperature (°C)
- Tmin: Minimum daily air temperature (°C)
- Tmax: Maximum daily air temperature (°C)
- RHmin: Minimum daily relative humidity (%)
- RHmax: Maximum daily relative humidity (%)
- u2: Wind speed at 10 m height (km/s)
- Tdew: Dew point temperature (°C)
- ea: Estimated actual vapour pressure (kPa) using FAO methods
- P: Precipitation (mm)
- Rs: Estimated surface resistance (sm⁻¹) using FAO method
- albedo: Estimated albedo (based on HOBO shortwave sensor; sometimes not available)
- PET: Estimated potential evapotranspiration (mm/day) using Penman method
- ddt (degree day temperature): Cumulative daily temperature above 0°C (°C)
- Mean catchment thaw depth: Estimated using observations and sqrt of ddt (m)
- thaw_depth: Thaw depth (m)
- thaw_volume: Estimated thaw volume (mm)
- flow_m3s: Measured stream discharge at S2 (m³/s)
- flow_mm: Calculated stream runoff using contributing area of S2 (mm)
- stream_temp: Stream water temperature (°C)

## Data sources and methods
- Meteorological inputs (temperature, humidity, wind, precipitation) sourced from http://climate.weather.gc.ca.
- ea and Rs estimated using FAO methods.
- PET estimated using the Penman-Monteith method.
- Thaw depth and thaw volume calculated via a day-degree (ddt) approach; measured thaw depth referenced to Lorna Street.
- NA indicates missing/not applicable data.

## Data quality and interpretation
- Data are quality-assured and transformed for standardized outputs.
- Columns include units and methodological notes to ensure consistent interpretation across analyses.
- Missing data are indicated as NA.

## Relevance to environmental monitoring objectives
- Enables consistent, time-series evaluation of environmental health indicators (temperature, moisture, evapotranspiration, thaw dynamics, and stream conditions).
- Supports cross-dataset integration by standardizing data sources, methods, and derived variables.
- Facilitates dissemination and accessibility by design, aligning with the aim to enable broader data use and portal storage.

## Practical implications for analysts
- Follow standardized data verification, cleaning, and transformation steps before analysis.
- Use the included methodologies (FAO, Penman-Monteith, day-degree thaw estimation) to reproduce or extend outputs.
- Present findings in clear formats (charts, maps, reports) and ensure datasets are uploaded to appropriate data portals for accessibility.