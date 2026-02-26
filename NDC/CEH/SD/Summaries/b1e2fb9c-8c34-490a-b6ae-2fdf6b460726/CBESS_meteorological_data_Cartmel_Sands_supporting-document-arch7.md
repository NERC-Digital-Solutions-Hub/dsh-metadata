# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Meteorological Data for Cartmel Sands, Morecambe.

## Overview
- Meteorological measurements collected at the Cartmel Sands site in Morecambe as part of the CBESS project.
- Data consist of half-hourly mean values collected from 31/05/2013 to 26/01/2015.
- Designed to support GIS-based analyses of coastal biodiversity, habitat conditions, and ecosystem services.

## Location and Scope
- Observation location: Morecambe, Cartmel Sands (CS) with coordinates 54°10'40"N, 3°00'05"W.
- Dataset focuses on Cartmel Sands but notes Essex and Morecambe Bay saltmarsh regions as contrasting habitat contexts in the broader CBESS framework (habitat differences include sediment type, inundation frequency, creek structure, and vegetation).

## Data Collection and Timing
- Instrumentation:
  - Campbell Scientific CR5000 datalogger for measurements.
  - Wind: CSAT3 anemometer at 4.3 m on a lattice tower operating at 10 Hz.
  - Other variables measured with Vaisala MP103A (air temperature and humidity) and converted to Vapour Pressure Deficit (VPD).
  - Precipitation: Environmental Measurements Limited ARG100 tipping bucket rain gauge.
  - Net radiation: Kipp and Zonen NR Lite.
  - Photosynthetically active radiation (PAR): Skye Instruments SKP215.
  - Soil temperatures: T thermocouples (depths 5 cm and 10 cm).
- Sampling and processing:
  - Half-hourly mean values; time reference is the middle of the half-hour period (e.g., 00:15 represents 00:00–00:30).
  - Matlab used to calculate mean half-hour values.
- Data quality and calibration:
  - 10 Hz wind data filtered for wind shadowing and data quality flags; averaged to half-hour.
  - Other meteorological measurements averaged to half-hour.
  - Quality control relies on data quality flags and calibration procedures.

## Measured Variables and Instruments
- Variables observed:
  - Air temperature (T_air)
  - Soil temperature at 5 cm (T_soil_5cm)
  - Soil temperature at 10 cm (T_soil_10cm)
  - Relative humidity (RH)
  - Net radiation (Net_rad)
  - Photosynthetically active radiation (PAR)
  - Precipitation (Precip)
  - Wind speed (Wind_Spd)
  - Wind direction (Wind_Dir)
  - Vapour pressure deficit (VPD)
- Data collection details:
  - Wind: 10 Hz measurements, wind direction/velocity via CSAT3; rest of variables at various sampling rates (with half-hourly aggregation).
  - T_air and RH measured with Vaisala MP103A; conversions performed to derive VPD.
  - Net radiation, PAR, and soil temperatures measured with specified instruments; mean half-hour values computed.

## Data Formats and Metadata
- File format: CSV.
- Data gaps: Gaps indicate sensor malfunctions or power loss; NA values indicate measurements not performed.
- Dataset field structure (examples of fields and coding):
  - Row Number (sorting order)
  - Season (Winter W, Summer S)
  - Location (Morecambe M, Essex E)
  - Site (CS: Cartmel Sands, WS: Warton Sands, WP: West Plain, AH: Abbotts Hall, FW: Fingringhoe Wick, TM: Tillingham Marshes)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A: 1 m, B: 1–10 m, C: 10–100 m, D: 100–upper limit)
  - Year, Month, Day
  - Hour, Minute
  - T_air, T_soil_5cm, T_soil_10cm
  - RH
  - Net_rad
  - PAR
  - Precip
  - Wind_Spd
  - Wind_Dir
  - VPD
- Units and coding conventions are described for each field (e.g., T_air in degrees Celsius, PAR in μmol m^-2 s^-1, etc.).

## Data Structure and Accessibility
- The dataset is organized to support spatial-temporal analyses within GIS, enabling mapping of meteorological conditions across habitat types and scales.
- Codes for site, habitat, and scale facilitate filtering and integration with spatial layers (habitat maps, soil types, grid systems).

## Gaps, Limitations, and Data Quality
- Data gaps due to sensor malfunction or power loss; some NA values where measurements were not performed.
- The dataset covers a specific timeframe and a single site, with broader CBESS comparisons to Essex and Morecambe Bay habitats in related materials.

## GIS Applications and Use in Mapping
- Suitable for creating time-series maps of meteorological variables across coastal habitats.
- Integrates with habitat and soil data to analyze spatially variable climate conditions and their potential impacts on coastal biodiversity and ecosystem services.
- Supports quality-controlled, half-hourly climate rasters or vector overlays for policy, research, and public-facing GIS visuals.