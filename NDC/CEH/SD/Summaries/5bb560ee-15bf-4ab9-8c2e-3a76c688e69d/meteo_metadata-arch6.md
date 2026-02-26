# Daily climate data combines data from several different sources for the Siksik catchment

## Overview
- Dataset describing meteorological data for the Siksik catchment, North West Territories, Canada
- Location details: Longitude 133°26'26" W, Latitude 68°44'17" N, Elevation 85 m
- Catchment size: ~1 km2; Time zone: Mountain Standard Time
- Data are daily climate measurements, assembled from multiple sources and packaged as meteo_data.csv with explanations
- Purpose: to enable analysis and self-service exploration of climate data and derived variables for the catchment

## Data sources and processing
- Primary data source for core meteorological variables: http://climate.weather.gc.ca
- Variables obtained from source: mean daily air temperature (Tair), Tmin, Tmax, minimum and maximum relative humidity (RHmin, RHmax), wind speed at 10 m (u2), dew point temperature (Tdew), and precipitation (P)
- Derived variables and methods:
  - Estimated actual vapour pressure (ea) using FAO methods
  - Estimated surface resistance (Rs) using FAO methods
  - Potential evapotranspiration (PET) estimated using the Penman-Monteith method
- Thaw-related calculations:
  - Thaw depth and thaw volume estimated using a day-degree method
  - Thaw depth measurements referenced to observed data (noted to be measured by Lorna Street)

## Variables and units (as described in the sheet)
- date: Date of record (dd/mm/yy)
- Tair: Mean daily air temperature (degrees Celsius)
- Tmin: Minimum daily air temperature (degrees Celsius)
- Tmax: Maximum daily air temperature (degrees Celsius)
- RHmin: Minimum daily relative humidity (%)
- RHmax: Maximum daily relative humidity (%)
- u2: Wind speed at 10 m height (kilometres per second)
- Tdew: Dew point temperature (degrees Celsius)
- ea: Estimated actual vapour pressure (kPa)
- P: Precipitation (mm)
- Rs: Estimated surface resistance (sm⁻¹)
- albedo: Estimated albedo (dimensionless)
- PET: Estimated potential evapotranspiration (mm per day)
- ddt: Degree-day temperature (mean daily temperature above 0°C; units: degree-days or °C·d)
- thaw_depth: Mean catchment thaw depth (metres)
- thaw_volume: Estimated thaw volume (millimetres)
- flow_m3s: Measured stream discharge (m³/s)
- flow_mm: Calculated stream runoff (mm)
- stream_temp: Stream water temperature (degrees Celsius)

Notes:
- NA indicates missing/not applicable data
- Data sheet includes explanations of column headings, units, and methodology

## Derived metrics and methodology
- PET and Rs derived from FAO methods and climate data
- Thaw-related estimates based on day-degree approach, with observed thaw depth referenced from measured data
- The dataset integrates multiple sources to support planning and analysis for the catchment

## Data quality, usage, and purpose
- Intended to support data discovery and self-service analysis for end users
- Highlights potential challenges typical of data support work:
  - Patchy data across formats and systems
  - Need to understand the ask and determine the best approach to meet data needs
  - Communication of complex data and outputs to non-specialists
- NA/missing data are noted, informing users to account for gaps during analysis

## Materials and methods (summary)
- Meteorological data compiled for the Siksik catchment, North West Territories, Canada
- Source data for temperature, humidity, wind, and precipitation obtained from climate.weather.gc.ca
- Derived values computed using FAO methods (ea, Rs) and Penman-Monteith method (PET)
- Thaw depth and thaw volume calculated via day-degree method, with reference measurements for validation