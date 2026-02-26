# Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2021-2022)

## Overview
- Meteorological dataset collected to support the Glencorse ammonia enhancement experiment near Edinburgh.
- Site features a 16 m mast (2 m above canopy) in the Glencorse woodland; data used to understand wind-controlled NH3 enhancement effects on forest ecosystems.
- Data period: 28 May 2021 to 5 January 2023; all times in GMT.
- Comprehensive documentation and results referenced in Deshpande et al. (2024).

## Data collection
- Measurements from a multi-sensor setup at multiple heights:
  - Air temperature, relative humidity, leaf wetness, wind speed (four heights)
  - Rainfall, wind direction, barometric pressure, photosynthetically active radiation (PAR), total solar radiation (above and below canopy)
  - Soil volumetric water content (VWC), electrical conductivity (EC), and temperature at three depths
- Data collection cadence: every 20 seconds, with 15-minute averages computed
- Complete methodology and experimental design detailed in Deshpande et al. (2024)

## Quality control
- Visual checks performed; obvious instrument/ logger issues and power outages removed
- Gaps occur due to sensor replacement and related maintenance

## Data structure
- Dataset comprises 56,154 measurements across 41 parameters
- Format: CSV with descriptive columns (e.g., Timestamp, Height, Manufacturer, Instrument, Description) plus a wide set of sensor readings
- Variables include:
  - Rain and Throughfall (locations: above/below canopy)
  - Leaf Wetness Sensors (LWS1–LWS4)
  - Air temperature and relative humidity at multiple heights (AirT1–AirT4, RH1–RH4)
  - Soil VWC, EC, and Temperature at multiple depths (Soil_VWC1–3, Soil_EC1–3, Soil_T1–3 with corresponding depth annotations)
  - Wind speed and related measurements near the forest floor, ground flora, tree canopy, and top canopy (WS_Cup1–4)
  - PAR and Total Solar radiation (PAR1, Total_Solar1–2)
  - Wind, temperature, humidity, and barometric pressure readings for below- and above-canopy contexts (WXT_WS1–2, WXT_WD1–2, WXT_AirT1–2, WXT_RH1–2, WXT_BP1–2)

## Temporal and location details
- Location coordinates: Glencorse woodland site (approximate 55.8539° N, -3.2151° W), altitude ~200 m
- Timeframe spans late May 2021 to early January 2023; measurements are GMT timestamps

## Data quality and limitations
- Data quality controlled through visual checks; some gaps due to sensor maintenance
- Metadata and instrument details enable clear interpretation and reuse, with explicit height, unit, and instrument/source information to support downstream analyses

## Data usage and accessibility
- Data provided as a CSV with extensive sensor metadata to facilitate reuse, integration, and cross-comparison
- Used to estimate ammonia deposition to forest ecosystems; methods and findings published in Atmosphere Environment (Deshpande et al., 2024)

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub
- Reference: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325