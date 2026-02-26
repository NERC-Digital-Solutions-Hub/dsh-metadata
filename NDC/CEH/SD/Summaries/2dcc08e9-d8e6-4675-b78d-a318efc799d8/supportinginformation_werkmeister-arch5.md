# SUPPORTING INFORMATION Temperature and humidity data supporting use of an in situ passive heating method, and associated whole tree responses, Cerrado, Brazil, 2020

## Purpose and scope
- Documents microclimate and physiological data collected to evaluate a novel in situ passive heating method (whole-tree heating structures, WTHS) in the Cerrado.
- Focuses on daytime warming effects on whole trees and associated leaf-level photosynthesis and respiration responses.
- Includes data from a prototype WTHS around Davilla elliptica and three four-sided WTHS around Erythroxylum suberosum, plus short-term heating experiment.

## Experimental design and sampling regime
- WTHS deployment:
  - Prototype around a ~2.4 m Davilla elliptica (Dilleniaceae).
  - Three four-sided WTHSs (S1–S3) around Erythroxylum suberosum shrubs (~2 m tall).
- Treatment scheme:
  - Treatment individuals: T1–T3 (heated).
  - Control individuals: C1–C3 (not heated).
- Measurements:
  - Photosynthesis and respiration temperature response curves measured daily 08:00–11:30.
  - Two leaves per individual analyzed with LI-COLOR XT systems (one leaf per instrument; one leaf for photosynthesis, one for respiration).
  - Temperature range: 20–50°C in 10 incremental steps; leaf temperature controlled via heating; CO2 at 400 ppm; RH at 50%; light levels at 1100 µmol m⁻² s⁻¹ for photosynthesis measurements and 0 for respiration.
- Temporal design:
  - Repeated measurements: week 1 (baseline), then 7, 14, 21 days after heating began for treated individuals.
  - Last respiration measurement (C3, day 21) excluded due to leaf wind damage.
- Timeline:
  - Prototype measurements: 09–27 June 2020.
  - S1–S3 measurements: 04 August–25 August 2020.

## Microclimate data collection
- Temperature and relative humidity recorded every minute with DTH22 sensors inside solar shields, controlled by Arduino UNO.
- Sensor placement:
  - Inside WTHS, near crown center (treatment).
  - Above a nearby control individual (ambient comparison).
  - Ambient conditions also captured every 15 minutes by a WatchDog weather station.
- Calibration and quality checks:
  - Sensors calibrated against known temperatures and each other.
  - Anomalous readings removed pre-analysis; leaves photographed to assess health pre/post measurements.

## Data structure and content (files and variables)
- WeatherStationClimateData.csv
  - Purpose: Temperature, relative humidity, and solar radiation from the WatchDog weather station.
  - Columns: DateTime, SolarR, RH, AirTemp.
  - Period: 01/06/2020–01/09/2020.
- StructuresTempRH.csv
  - Purpose: Temperature and relative humidity inside WTHS (treatment) vs outside (control) for prototype and S1–S3.
  - Columns: DateTime, Temp_T, Temp_C, RH_T, RH_C, Structure.
  - Period: 09/06/2020–25/08/2020.
- PhotosynthesisMeasurements.csv
  - Purpose: Leaf-level photosynthesis rates across a range of leaf temperatures.
  - Columns: Week, Treatment, Individual, LogNumber, AirTemp, LeafTemp, PhotosynthRate.
- RespirationMeasurements.csv
  - Purpose: Leaf-level dark respiration across a range of leaf temperatures.
  - Columns: Week, Treatment, Individual, LogNumber, AirTemp, LeafTemp, RespRate.
- Units and details:
  - DateTime: dd/mm/yyyy hh:mm.
  - SolarR: Watts/m².
  - RH: %.
  - AirTemp, Temp_T, Temp_C: °C.
  - LeafTemp: °C.
  - PhotosynthRate: µmol m⁻² s⁻¹.
  - RespRate: µmol m⁻² s⁻¹.

## Methods and quality assurance
- Instrumentation:
  - DTH22 temperature/humidity sensors with Arduino control for microclimate data.
  - LI-COR LI-6400XT systems for photosynthesis and respiration measurements (with fluorometer and LED chambers).
- Experimental rigor:
  - Leaves selected based on health, full expansion, and uniform maturity; respiration leaves kept in darkness pre-measurement.
  - Calibration of sensors prior to data collection; data screened for anomalies.
  - Documentation includes detailed protocol steps, including measurement timing, environmental controls (CO2, RH, light), and leaf handling.

## Data governance, sharing, and stewardship considerations
- Rich, structured metadata with explicit explanations of each dataset file and each column to enable reuse and reproducibility.
- Clear documentation of experimental conditions, device settings, and measurement schedules to support data integrity and provenance.
- Notable data limitation: one late respiration measurement removed due to wind damage; some datasets reflect the 4-week heating period with open/closed-wedging conditions as noted.
- Potential for data reuse in validating in situ heating methods, microclimate characterization, and leaf-level physiological responses under warming.
- Recommend including licensing, repository location, and DOI in future sharing to facilitate discoverability and long-term preservation.