# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Meteorological Data for Cartmel Sands, Morecambe

## Purpose and scope
- Provides meteorological measurements at the Cartmel Sands site in Morecambe for CBESS monitoring of coastal environmental conditions.
- Data intended to support assessment of environmental health and policy-relevant trends over time.
- Observation period: half-hourly values from 31/05/2013 to 26/01/2015.
- Sites described include Morecambe (Cartmel Sands CS, plus Warton Sands WS and West Plain WP) and Essex sites (Abbotts Hall AH, Fingringhoe Wick FW, Tillingham Marshes TM) to represent contrasting habitats and sediment/soil types.

## Data collection and instrumentation
- Staff responsible: Timothy Hill.
- Observing locations: Cartmel Sands (CS) at Morecambe; additional Essex and Morecambe Bay sites provide habitat contrasts.
- Measurement framework:
  - Half-hourly mean values (with time reference at the middle of the half-hour).
  - Wind measurements at 10 Hz using a CSAT3 anemometer on a 4.3 m lattice tower.
  - Other meteorological variables recorded every 15 minutes.
- Key instruments:
  - Campbell Scientific CR5000 datalogger.
  - Vaisala MP103A for air temperature/humidity (converted to VPD).
  - EML ARG100 tipping bucket rain gauge for precipitation.
  - Kipp and Zonen NR Lite for net radiation.
  - Skye Instruments SKP215 for PAR.
  - Type T thermocouples for soil temperatures (5 cm and 10 cm).

## Variables and data handling
- Measured variables (with typical units):
  - Air temperature (T_air, °C)
  - Soil temperature at 5 cm (T_soil_5cm, °C)
  - Soil temperature at 10 cm (T_soil_10cm, °C)
  - Relative humidity (RH, %)
  - Net radiation (Net_rad, W/m²)
  - Photosynthetically active radiation (PAR, μmol m⁻² s⁻¹)
  - Precipitation (Precip, mm per 30 min)
  - Wind speed (Wind_Spd, m/s)
  - Wind direction (Wind_Dir, degrees)
  - Vapour Pressure deficit (VPD, kPa)
- Data processing:
  - Mean half-hour values calculated in Matlab; time reference is the half-hour midpoint.
  - 10 Hz wind data filtered for wind shadowing and quality flags; then averaged to half-hourly means.
  - Remaining meteorological measurements averaged to half-hourly means.
- Data quality and checks:
  - Wind data quality flags used to filter measurements; wind shadowing considerations applied.
  - Data checked via CSATA flags and wind-shadowing considerations.
- Data format:
  - Primary file format: CSV.
  - Gaps explained by sensor malfunction or power loss; NA values indicate measurements not performed.

## Dataset structure and field descriptions
- Core fields include:
  - Seasonal indicator (Winter W, Summer S)
  - Location (Morecambe M, Essex E)
  - Site (CS Cartmel Sands, WS Warton Sands, WP West Plain; AH Abbotts Hall, FW Fingringhoe Wick, TM Tillingham Marshes)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A: 1 m; B: 1–10 m; C: 10–100 m; D: 100 m and above)
  - Year, Month, Day, Hour, Minute
  - Parameters: T_air, T_soil_5cm, T_soil_10cm, RH, Net_rad, PAR, Precip, Wind_Spd, Wind_Dir, VPD
- The field descriptions indicate data types (numeric or text) and scale details for each variable.

## Context and accessibility
- The dataset is part of a broader effort to monitor coastal biodiversity and ecosystem service sustainability, enabling cross-site comparisons across contrasting habitats and sediment types.
- The design emphasises standardized methods, data verification, and preparation for publication or portal storage to support downstream analyses and policy evaluation.
- Acknowledges gaps and data quality considerations, with emphasis on making underlying data accessible to others and enabling dataset integration with related environmental data.