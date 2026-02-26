Daily climate data combines data from several different sources for the Siksik catchment. Explanation of data sheet - meteo_data.csv.

## Overview
- Describes meteorological data for the Siksik catchment in the North West Territories, Canada.
- Site details: Siksik site(s) with coordinates around 133°26'26"W, 68°44'17"N; elevation ~85 m; watershed area ~1 km²; time zone: Mountain Standard Time.
- Daily climate data collated from multiple sources; includes explanations for column headings, units, and methods.

## Dataset structure
- Data sheet presents a structured table with:
  - date: day, month, year (dd/mm/yy)
  - Variables related to temperature, humidity, wind, precipitation, radiation, and hydrology
  - Units and methodology provided for each variable
- Notes indicate that NA means not applicable or missing data.

## Variables and units
- Temperature and humidity
  - Tair: mean daily air temperature (°C)
  - Tmin: minimum daily air temperature (°C)
  - Tmax: maximum daily air temperature (°C)
  - RHmin: minimum daily relative humidity (%)
  - RHmax: maximum daily relative humidity (%)
  - Tdew: dew point temperature (°C)
- Wind and radiation
  - u2: wind speed at 10 m (unit listed as km/s)
  - ea: estimated actual vapour pressure (kPa) using FAO methods
  - Rs: estimated surface resistance (sm⁻¹) using FAO methods
  - albedo: estimated albedo (dimensionless; data may be absent)
- Precipitation and evapotranspiration
  - P: precipitation (mm)
  - PET: potential evapotranspiration (mm or mm/day; method noted)
- Derived temperatures and thaw
  - ddT or ddt: degree days above 0°C (°C)
  - thaw_depth: mean catchment thaw depth (m)
  - thaw_volume: estimated thaw volume (mm)
- Hydrology and stream conditions
  - flow_m3s: measured stream discharge (m³/s)
  - flow_mm: calculated stream runoff (mm)
  - stream_temp: stream water temperature (°C)

## Derived variables and methods
- PET calculated using Penman-Monteith method
- Ea and Rs estimated using FAO methods
- Thaw depth and thaw volume derived from a day-degree (degree-day) method
- Data sources and methodologies are documented in the notes and methods sections

## Data sources and provenance
- Meteorological inputs (Tair, Tmin, Tmax, RHmin, RHmax, u2, P, etc.) sourced from http://climate.weather.gc.ca
- FAO methods used for vapour pressure and surface resistance
- Penman-Monteith method used for PET
- Thaw metrics based on day-degree calculations; thaw depth measured by Lorna Street
- Data sheet provides explicit methodology and references for replication

## Notes on data quality and structure
- NA indicates not applicable or missing data
- Dataset integrates multiple sources and derived calculations; users should consider potential inconsistencies or gaps, especially at small local scales

## Practical use for analysts
- Suitable for exploring correlations and modeling in catchment processes:
  - Relationships between climate variables (temperature, humidity, precipitation) and evapotranspiration (PET)
  - Thaw dynamics (thaw depth and thaw volume) in relation to daily climate
  - Runoff and stream temperature in connection with meteorological drivers
- Provides explicit provenance and methods to enable reproducibility and metadata-rich analysis

## Considerations and caveats
- Small watershed (~1 km²); findings may not generalize to larger scales without adjustment
- Data completeness may vary by date; some fields may be missing (NA)
- Units and measurement details (e.g., u2 in km/s) should be verified if used in cross-dataset analyses to ensure consistency