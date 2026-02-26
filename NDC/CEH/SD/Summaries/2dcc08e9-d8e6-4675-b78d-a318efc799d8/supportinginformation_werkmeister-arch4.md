# SUPPORTING INFORMATION Temperature and humidity data supporting use of an in situ passive heating method, and associated whole tree responses, Cerrado, Brazil, 2020

## Overview
- Study develops and tests a passive in situ whole-tree heating method (WTHS) to elevate daytime temperatures by ~3°C for trees up to 2.5 m tall, in a Cerrado environment.
- Field setup includes:
  - Six-sided prototype WTHS around a 2.4 m Davilla elliptica tree (prototype structure).
  - Three four-sided WTHSs (S1–S3) around Erythroxylum suberosum shrubs (~2 m tall).
- Primary goal: evaluate whole-tree daytime warming responses and acclimation of photosynthesis and respiration in situ.
- Measurements span a short-term 4-week heating experiment with repeated leaf-level gas exchange assessments.

## Experimental Design
- Species and individuals:
  - Davilla elliptica (prototype WTHS) and Erythroxylum suberosum (S1–S3, with T1–T3 treatment and C1–C3 controls).
- Treatment assignment:
  - Treatment (T1–T3) vs. Control (C1–C3) for E. suberosum.
- Measurement schedule:
  - Baseline measurements for each treated individual before any heating.
  - Heating initiated with WTHS; repeated measurements at 7, 14, and 21 days after first measurements.
  - One respiration measurement (week 3, day 21) removed due to wind-induced leaf damage.
- Data collection window:
  - June–August 2020 for microclimate data; specific measurement periods described for each WTHS setup.

## Data Collected and Measurements
- Microclimate data:
  - Temperature and relative humidity measured continuously inside WTHS and at nearby control trees.
  - Ambient values recorded with a WatchDog weather station; sensors calibrated and cross-validated.
  - Sensors: DTH22 (±0.5°C, ±2% RH), solar radiation shields, Arduino UNO controller.
  - Timeframe: 09/06/2020 to 27/08/2020 (with testing periods excluded from ambient data).
- Gas exchange measurements:
  - Photosynthesis and respiration rate measurements using LI-COR LI-6400XT systems (with a fluorometer for photosynthesis and an LED chamber for respiration).
  - Measurement window: 08:00–11:30 daily.
  - Leaf selection: healthy, fully expanded leaves; one leaf per instrument per individual (two leaves per individual per day).
  - Temperature response: 10 incremental leaf temperature steps from 20°C to 50°C.
  - Environmental controls: CO2 at 400 ppm, RH at 50%, light at 1100 µmol m−2 s−1 for photosynthesis; dark for respiration (0 µmol m−2 s−1).
  - Temperature manipulation: internal leaf temperature tracked with water jackets to achieve target temperatures.
- Data integrity:
  - Regular calibration of temperature and humidity sensors; anomalous readings removed pre-analysis.
  - Leaves photographed and health status assessed before and after measurements.

## Data Structure and Variables
- WeatherStationClimateData.csv
  - Description: Temperature, relative humidity, and solar radiation from the WatchDog weather station (Bacaba Park, Nova Xavantina).
  - Columns: DateTime, SolarR, RH, AirTemp.
  - Units: DateTime (dd/mm/yyyy hh:mm); SolarR (W/m²); RH (%); AirTemp (°C).
- StructuresTempRH.csv
  - Description: Temperature and RH data inside treatment WTHS and outside control, across prototype and S1–S3 structures.
  - Columns: DateTime, Temp_T, Temp_C, RH_T, RH_C, Structure.
  - Units: Temp_T/Temp_C (°C); RH_T/RH_C (%); Structure (category).
- PhotosynthesisMeasurements.csv
  - Description: Photosynthesis rates across leaf temperatures for E. suberosum inside (T) and outside (C) WTHSs.
  - Columns: Week, Treatment, Individual, LogNumber, AirTemp, LeafTemp, PhotosynthRate.
  - Units: Week (int); Treatment (C/T); Individual (identifier); LogNumber (int); AirTemp (°C); LeafTemp (°C); PhotosynthRate (µmol m−2 s−1).
- RespirationMeasurements.csv
  - Description: Respiration rates across leaf temperatures for E. suberosum inside (T) and outside (C) WTHSs.
  - Columns: Week, Treatment, Individual, LogNumber, AirTemp, LeafTemp, RespRate.
  - Units: Week (int); Treatment (C/T); Individual (identifier); LogNumber (int); AirTemp (°C); LeafTemp (°C); RespRate (µmol m−2 s−1).

## Quality Control and Data Integrity
- Sensor calibration against known steady temperatures and inter-sensor comparisons.
- Data flagged and removed if readings were clearly anomalous.
- Measurement procedures standardized; leaf health assessed before and after experiments to ensure data quality.

## Potential Uses for Data Leaders
- Data governance and interoperability:
  - A well-documented, multi-structure dataset linking microclimate, structural environment, and leaf-level gas exchange in a field warming experiment.
  - Clear metadata and column definitions support discoverability and re-use for cross-site warming studies or meta-analyses of WTHS methodologies.
- Data strategy and stewardship lessons:
  - Demonstrates end-to-end data lifecycle: instrument setup, calibration, data capture, alignment across devices, and post-processing notes on data exclusions.
  - Highlights importance of linking treatment, time, and physiological responses to support user-centered, iterative data products.
- Analytical use cases:
  - Develop temperature-response curves for photosynthesis and respiration under controlled, in situ warming.
  - Assess how microclimate changes inside WTHS relate to whole-tree and leaf-level physiological responses across weeks.
  - Examine data gaps and barriers to access or standardization in field-collected ecological data, informing data standardization practices.

## Notes and Considerations
- One respiration data point (week 3, day 21) excluded due to wind damage; dataset may reflect occasional field disruptions.
- Some structural parameter tables show incomplete side-length entries; interpret structural scope with accompanying documentation.
- Data available in clearly labeled CSVs with explicit units and headers to facilitate reuse and integration with broader data ecosystems.