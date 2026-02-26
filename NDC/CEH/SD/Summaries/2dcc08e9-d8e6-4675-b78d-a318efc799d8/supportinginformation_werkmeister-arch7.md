# Temperature and humidity data supporting use of an in situ passive heating method, and associated whole tree responses, Cerrado, Brazil, 2020

## Overview
- In situ passive heating method (Whole-Tree Heating Structures, WTHS) to evaluate daytime warming responses in Cerrado vegetation.
- Heating aims to raise tree-scale temperatures by ~3°C for whole individuals up to 2.5 m tall.
- Study integrates microclimate data with plant physiological responses (photosynthesis and respiration) to understand warming effects.

## Location and target organisms
- Location: Cerrado, Bacaba Park, Nova Xavantina, Mato Grosso, Brazil.
- Target organisms: Davilla elliptica (2.4 m tree; prototype WTHS) and Erythroxylum suberosum (shrubs ~2 m tall).

## Experimental design
- Prototype WTHS: six-sided frame around a Davilla elliptica individual (prototype).
- Additional field warming: three four-sided WTHSs (S1–S3) around E. suberosum individuals (T1–T3 heated; C1–C3 controls).
- Measurements conducted over a short-term warming period (July 27 – August 23, 2020); some measurements excluded due to wind damage or open-warming conditions.
- Measurements repeated across days to capture heating onset and short-term acclimation.

## Data collected
- Microclimate data
  - Temperature and relative humidity (RH) recorded at 1-minute intervals inside WTHS and at ambient/control locations.
  - Ambient weather data collected every 15 minutes: temperature, RH, solar irradiance.
  - Sensor placements: above crown inside WTHS and above a nearby control tree; calibration against known temperatures and sensor-to-sensor comparison.
- Physiological measurements (leaf-level)
  - Photosynthesis and respiration rate measurements across leaf temperatures (20–50°C) using LI-6400XT systems (with and without fluorometer).
  - Leaf selection: healthy, fully expanded leaves; respiration measured in darkness after dawn; photosynthesis measured under controlled light.
  - Measurement window: 08:00–11:30 each day.
  - Environmental controls during measurements: CO2 400 ppm, RH 50%, photosynthetic light ~1100 µmol m-2 s-1 for photosynthesis; respiration measurements conducted with light off.
- Data collection timeline and replication
  - Prototype: continuous microclimate data collection in June 9–27, 2020.
  - S1–S3: August 4–25, 2020; repeated measurements for T1–T3 and C1–C3 across weeks; one leaf/rating per measurement event.

## Data structure and files
- WeatherStationClimateData.csv
  - Contains: DateTime, SolarR (W/m^2), RH (%), AirTemp (°C)
  - Period: 01/06/2020–01/09/2020
- StructuresTempRH.csv
  - Contains: DateTime, Temp_T (°C inside WTHS), Temp_C (°C ambient/control), RH_T (% inside), RH_C (% ambient), Structure (Prototype, S1, S2, S3)
  - Period: 09/06/2020–25/08/2020
- PhotosynthesisMeasurements.csv
  - Contains: Week, Treatment (T/C), Individual, LogNumber, AirTemp (°C), LeafTemp (°C), PhotosynthRate (µmol m^-2 s^-1)
- RespirationMeasurements.csv
  - Contains: Week, Treatment (T/C), Individual, LogNumber, AirTemp (°C), LeafTemp (°C), RespRate (µmol m^-2 s^-1)

## Quality control and data integrity
- Sensor calibration against known steady temperatures and inter-sensor comparisons.
- Preanalysis data cleaning to remove anomalous readings.
- Careful execution of measurements; leaves photographed and health assessed before and after analysis.
- Data filtered to exclude periods when WTHS was open or environmental conditions invalid (e.g., wind damage).

## Units and variable definitions
- DateTime: dd/mm/yyyy hh:mm
- SolarR: Watts/m^2
- RH: %
- AirTemp, Temp_T, Temp_C: °C
- LeafTemp: °C
- Structure: categorical (Prototype, S1, S2, S3)
- Week: ordinal (1, 2, 3, …)
- Treatment: categorical (Treatment, Control)
- Individual: identifier (e.g., T1–T3, C1–C3)
- LogNumber: 1–10
- PhotosynthRate, RespRate: µmol m^-2 s^-1

## GIS relevance and potential applications
- Enables spatially explicit analysis of microclimate effects around WTHS structures and adjacent controls.
- Facilitates creation of map-based data products linking microclimate (temperature, RH, solar radiation) to physiological responses (photosynthesis, respiration) across multiple individuals and structures.
- Supports integration with GIS layers (species distribution, canopy structure, topography, land cover) to model warming effects on Cerrado vegetation at fine scales.
- Provides a structured metadata framework (per-structure and per-leaf measurements) suitable for overlay, temporal analyses, and reproducibility in spatial analyses.