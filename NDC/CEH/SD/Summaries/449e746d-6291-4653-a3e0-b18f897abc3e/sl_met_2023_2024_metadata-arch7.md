# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (20232024)

## Overview
- Meteorological dataset collected at a 12 m mast near the ammonia enhancement manifold at Queensberry Estate, Sri Lanka (coordinates: 6.9693°, 80.5911°, altitude 1645 m).
- Time period: 1 January 2023 – 31 December 2024 (Sri Lanka Standard Time, SLST).
- 70,176 measurements across 37 parameters, provided as a CSV with 15-minute averaging.
- Extends the 2022 dataset from the same site; linked to Ammonia enhancement experiments where wind conditions below the canopy drive the process.

## Data collection site and instrumentation
- Site supports multi-height measurements near and above/within the forest canopy.
- Measured variables include:
  - Air temperature and relative humidity at four heights; leaf wetness at four leaf-wetness sensors.
  - Wind speed and direction, barometric pressure, photosynthetically active radiation (PAR) and total solar radiation above and below the canopy.
  - Soil volumetric water content (VWC), soil electrical conductivity (EC), and soil temperature at three depths.
  - Rainfall and below-canopy throughfall; wind measurements near the forest floor and in the canopy.
- Data cadence: instrument readings every 20 seconds with 15-minute averages.

## Data structure (schema)
- Format: CSV with 37 parameters, each row representing a 15-minute interval.
- Example fields (high level): 
  - Timestamp (15-minute intervals)
  - Height, Manufacturer, Instrument, Description (metadata per measurement)
  - Rain, Throughfall
  - LWS1–LWS4 (Leaf Wetness Sensor readings at multiple heights)
  - AirT1–AirT4; RH2, RH3, RH4 (air temperature and relative humidity at multiple heights)
  - Soil_VWC1–3, Soil_EC1–3, Soil_T1–3 (soil moisture, electrical conductivity, temperature at various depths)
  - WS_Cup1–3 (wind speed near the forest floor and in the canopy)
  - PAR1–2; Total_Solar1–2 (PAR and total solar radiation near/below/above canopy)
  - WXT_WS1–2, WXT_WD1–2, WXT_BP1–2 (wind speed, wind direction, barometric pressure at below/canopy and above canopy levels)

## Quality control and data integrity
- Visual QC performed; obvious instrument errors, datalogger issues, and power outages corrected or removed.
- Small data gaps due to sensor replacement; step changes in leaf wetness reflect differing sensor baselines.
- Data are provided with clear documentation of measured parameters and units; time zone specified (SLST).

## Temporal coverage and usage notes for GIS
- Time span covers two full calendar years with 15-minute temporal resolution, suitable for time-series mapping and spatiotemporal analyses in GIS when integrated with ancillary spatial layers.
- Coordinate reference context is site-based; no explicit horizontal spatial grid beyond the coordinates provided. Users may need to assign a CRS when integrating with GIS datasets.
- For map-based visualization, consider aggregating to hourly/daily layers or creating feature layers per sensor height/variable for thematic mapping.

## Accessibility and references
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).
- Related data and methods reported in:
  - Deshpande et al. 2024a (Atmospheric Environment) – ammonia deposition estimation using wind-controlled NH3 enhancement.
  - Deshpande et al. 2024b (NERC EDS Data Centre) – meteorological data and ammonia concentrations/deposition rates at Queensberry, Sri Lanka.
- Data is available through the referenced publications and data centre entries.