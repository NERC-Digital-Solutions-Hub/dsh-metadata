# Overview of data

- What it is
  - A dataset compiling results from the stream metabolism component of the NERC Macronutrients consortium project titled "The role of lateral exchange in the seaward flux of C, N and P."
  - Field-generated atmospheric data collected during four campaigns in rivers within the Hampshire Avon catchment; associated with the broader study of lateral exchange impacts on nutrient flux.

- Data composition
  - 23 accompanying data files (Geos11_AP_autumn.CSV, Geos11_AP_spring.CSV, Geos11_AP_summer.CSV, Geos11_AP_winter.CSV, Geos11_AS_autumn.CSV, Geos11_AS_spring.CSV, Geos11_AS_summer.CSV, Geos11_AS_winter.CSV, Geos11_CE1_autumn.CSV, Geos11_CE1_spring.CSV, Geos11_CE1_summer.CSV, Geos11_CW2_autumn.CSV, Geos11_CW2_spring.CSV, Geos11_CW2_summer.CSV, Geos11_CW2_winter.CSV, Geos11_GA2_autumn.CSV, Geos11_GA2_spring.CSV, Geos11_GA2_summer.CSV, Geos11_GA2_winter.CSV, Geos11_GN1_autumn.CSV, Geos11_GN1_spring.CSV, Geos11_GN1_summer.CSV, Geos11_GN1_winter.CSV).
  - Four field campaigns measuring in situ atmospheric data with a SKYWATCH GEOS 11 weather station.

- Field campaign and site details
  - Locations span rivers with varying land-river connectivity in the Hampshire Avon catchment.
  - Sites include CE1 (River Ebble), GA2 (River Avon), GN1 (River Nadder), CW2 (River Wylye), AS1 (tributary of River Sem, AP), AS2 (River Sem).
  - Campaign periods: spring 2013, summer 2013, autumn 2013, winter 2014.
  - CE1 data not collected in winter 2014 due to flooding.

- Instrumentation and data collection
  - Equipment: SKYWATCH GEOS 11 high-precision weather station (factory-calibrated March 2013).
  - Deployment: 1–4 m above stream surface; exposed to stream morphology and access constraints.
  - Sampling frequency: 15–30 seconds (limited by battery life).

- Data quality and formatting notes
  - NaN values indicate missing data (e.g., battery changes, data download gaps) or data flagged as contaminated (e.g., insufficient wind for stable wind direction).
  - File naming convention: GEOS11_'SiteCode'_'Season'.CSV, encoding site and campaign season.
  - Column headers and data types
    - DateTime: combined date and time (MM/DD/YYYY hh:mm:ss)
    - Date: MM/DD/YYYY
    - Time: hh:mm:ss
    - Wind: wind speed (m/s); resolution 0.1 m/s; accuracy ±2% or measured value
    - Temperature: air temperature (°C); resolution 0.1 °C; accuracy ±2% (or 0.5 °C at 25 °C)
    - Humidity: relative humidity (%); resolution 0.1%; accuracy ±2% at 50% RH
    - Pressure: atmospheric pressure (hPa); resolution 0.1 hPa; accuracy ±0.5% (or 1.5 hPa at 25°C)
    - Direction: wind direction (°N); resolution 1°; accuracy ±3%; compass calibrated in the field

- Data usage considerations for data support
  - Suitable for analyses linking atmospheric conditions to stream metabolism across seasons and sites.
  - Expect some gaps due to NaN entries and winter flood-related omissions at CE1.
  - Ensure alignment of site codes with geographic coordinates when integrating with other datasets. 
  - Refer to GEOS11 documentation for instrument specifics and calibration context.