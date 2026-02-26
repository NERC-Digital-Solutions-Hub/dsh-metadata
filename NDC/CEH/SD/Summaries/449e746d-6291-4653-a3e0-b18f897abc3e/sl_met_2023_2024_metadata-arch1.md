# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (20232024)

## Overview
- Meteorological dataset collected adjacent to the ammonia enhancement manifold at Queensberry Estate, Sri Lanka (coordinates: 6.9693°, 80.5911°; altitude 1645 m).
- Time period: 1 January 2023 to 31 December 2024 (Sri Lanka Standard Time, SLST).
- Measurement mast height: 12 m, with sensors extending up to 5 m above the forest canopy.
- Data frequency: measurements every 20 seconds; 15-minute averages computed for analysis.
- Dataset size: 70,176 measurements across 37 parameters, provided as a CSV file.
- This dataset extends a 2022 dataset from the same site.

## Data collection and site setup
- Instrumentation arranged to capture microclimate and environmental conditions across vertical forest strata:
  - Air temperature and relative humidity at multiple heights (near forest floor, ground flora layer, tree canopy, above canopy).
  - Leaf wetness sensors at four heights (0.3, 2.0, 3.6, 5.6 m).
  - Wind speed and direction at below-canopy and upper canopy layers.
  - Barometric pressure measurements below the canopy.
  - Photosynthetically active radiation (PAR) and total solar radiation at below- and above-canopy positions.
  - Rain and below-canopy throughfall measurements.
  - Soil volumetric water content (VWC), soil electrical conductivity (EC), and soil temperature at shallow depths (near surface) and at 10–15 cm depths.
- Instrument manufacturers and specific sensors are listed for each parameter in the data structure.

## Measurements and data structure
- 37 parameters captured, each with metadata including:
  - Height (m) and position (below/above canopy, forest floor, ground flora layer, etc.)
  - Unit (e.g., °C for air temperature, % for RH, mm for rainfall, mV for leaf wetness sensors, etc.)
  - Instrument and description (e.g., Leaf Wetness Sensor near forest floor, above-canopy rainfall, below-canopy PAR)
- Sample fields include:
  - Timestamp (15-minute intervals), Rain, Throughfall, LWS1–LWS4 (leaf wetness sensors at various heights)
  - AirT1–AirT4 and RH1–RH4 (air temperature and relative humidity at multiple heights)
  - Soil_VWC1–VWC3, Soil_EC1–EC3, Soil_T1–T3 (soil moisture, conductivity, and temperature at near-surface, 10 cm, and 15 cm depths)
  - WS_Cup1–WS_Cup3 (wind speeds at different canopy layers)
  - PAR1–PAR2 and Total_Solar1–Total_Solar2 (below- and above-canopy radiation)
  - WXT_WS1–WXT_WS2, WXT_WD1–WXT_WD2, WXT_BP1–WXT_BP2 (wind, wind direction, and barometric pressure at below- and above-canopy levels)
- Data are provided in a CSV file with structured columns and detailed descriptions for each record.

## Quality control and data processing
- Visual quality checks performed; obvious instrument malfunctions, erroneous datalogger settings, and power cut issues removed.
- Some gaps exist due to sensor replacements and instrument downtime.
- Step changes in leaf wetness measurements attributed to baseline shifts after sensor replacement.
- Metadata notes emphasize the field-based nature and potential minor non-steady-state periods due to maintenance.

## Temporal and spatial coverage
- Spatial coverage limited to the Queensberry site near the ammonia enhancement manifold; multi-height vertical profiling from near the forest floor to above the canopy.
- Time-resolved data enabling analysis of diurnal and seasonal patterns in meteorology and related microclimate processes in the context of ammonia enhancement experiments.

## Usage and applicability
- Suitable for studying:
  - Microclimate responses to ammonia enhancement campaigns.
  - Wind-controlled dispersion and deposition scenarios in forested environments.
  - Relationships between meteorological variables (temperature, humidity, radiation, wind) and soil–leaf–canopy processes.
- Important considerations:
  - Align analyses with SLST time standard.
  - Account for gaps due to sensor maintenance and known step changes in leaf wetness baselines.
  - Data complements the 2022 dataset from the same site for longitudinal analyses.

## Access, provenance, and references
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1) supported establishing the facility.
- Related publications and data records:
  - Deshpande et al. (2024a): Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments.
  - Deshpande et al. (2024b): Meteorological data and ammonia concentration and deposition rates from Queensberry, Sri Lanka, 2022.
- Data provenance: metadata and full methodology are described in the cited works; complete site-specific details, methodology, and analysis are available through the NERC Environmental Information Data Centre (EDS) and linked DOIs.