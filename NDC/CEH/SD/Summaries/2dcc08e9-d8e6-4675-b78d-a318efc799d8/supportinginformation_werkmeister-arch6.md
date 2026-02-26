# Temperature and humidity data supporting use of an in situ passive heating method, and associated whole tree responses, Cerrado, Brazil, 2020

## Overview
- Describes a dataset supporting a novel in situ passive heating method (whole-tree heating structures, WTHS) to evaluate daytime warming responses in Cerrado trees and shrubs.
- Includes microclimate measurements inside and outside the structures, plus leaf-level photosynthesis and respiration responses across a range of temperatures.
- Serves as a resource for analyzing how whole-tree heating influences physiological processes and microclimate in remote environments.

## Experimental design and setup
- Objective: Test the functioning of WTHS to heat entire individuals by ~3°C during daytime.
- Structures:
  - Prototype six-sided WTHS around a ~2.4 m Davilla elliptica (Dilleniaceae).
  - Three four-sided WTHSs (S1-S3) around Cerrado shrubs Erythroxylum suberosum.
- Subjects:
  - Davilla elliptica (prototype) for baseline microclimate testing.
  - Erythroxylum suberosum: six individuals selected; three heated (T1-T3) and three controls (C1-C3).
- Experimental timeline:
  - Day 1: Measure photosynthesis and respiration for T1 before constructing S1 (heating not yet started).
  - Day 2 onward: Repeat measurements for C1 (control) before heating; continue for the remaining trees with S2 and S3 in sequence.
  - Week 1–3: Re-measure each individual at 7, 14, and 21 days after first measurements.
  - Note: The final respiration measurement for C3 (day 21) was removed due to wind-induced leaf damage.
- Data focus: Compare physiological responses under heated vs control conditions over a multi-week period.

## Microclimate data
- Temperature and relative humidity (RH) recorded continuously using:
  - DTH22 sensors inside WTHS shields, controlled by Arduino UNO; accuracy ±0.5°C, ±2% RH.
  - One sensor above the crown inside each WTHS (structure center) and one ambient sensor above a nearby control individual.
  - Ambient climate data also captured by a nearby WatchDog weather station (air temperature, RH, solar irradiance every 15 minutes).
- Timeframes:
  - Prototype (D. elliptica): 09–27 June 2020.
  - S1–S3 (E. suberosum): 04 August–25 August 2020 (data paired with corresponding control trees).
- Data handling: Climate data from open-walled testing periods were removed from analyses.

## Photosynthesis and respiration measurements
- Instrumentation: Two LI-6400XT portable systems (one with fluorometer chamber head and one with LED chamber head) used to measure:
  - Photosynthesis and dark respiration at leaf level.
- Protocol:
  - Leaves: healthy, fully expanded, similarly mature; two leaves analyzed per individual per day.
  - Respiration leaves: dark-adapted (sunlight blocked since dawn, at least 40 minutes in darkness before testing).
  - Photosynthesis leaves: exposed to full light (~1100 µmol m^-2 s^-1) for at least 40 minutes prior to testing.
  - Temperature steps: 20–50°C in 10 incremental steps with full equilibration at each step.
  - CO2: maintained at 400 ppm; RH: 50% for all measurements.
- Measurements:
  - For photosynthesis: leaf temperatures across the temperature range to derive temperature response curves.
  - For respiration: similar temperature response curves under dark conditions.
- Timing: Measurements conducted between 08:00 and 11:30 each day.
- Note: One final C3 respiration measurement was excluded due to wind damage.

## Data structure and contents
- WeatherStationClimateData.csv
  - Content: Temperature, relative humidity, and solar radiation from WatchDog weather station.
  - Period: 01/06/2020–01/09/2020.
  - Columns: DateTime, SolarR (W/m^2), RH (%), AirTemp (°C).
- StructuresTempRH.csv
  - Content: Temperature and RH data from sensors inside treatment WTHS and outside (control) across prototype and S1–S3.
  - Period: 09/06/2020–25/08/2020.
  - Columns: DateTime, Temp_T (inside WTHS, °C), Temp_C (outside WTHS, °C), RH_T (%), RH_C (%), Structure (Prototype, S1, S2, S3).
- PhotosynthesisMeasurements.csv
  - Content: Photosynthesis rates across leaf temperatures for leaves inside (T) and outside (C) WTHS during the 4-week heating period.
  - Week 1 measurements taken on heating onset.
  - Columns: Week, Treatment (Treatment/Control), Individual, LogNumber, AirTemp (°C), LeafTemp (°C), PhotosynthRate (µmol m^-2 s^-1).
- RespirationMeasurements.csv
  - Content: Respiration rates across leaf temperatures for leaves inside (T) and outside (C) WTHS during the 4-week heating period.
  - Columns: Week, Treatment (Treatment/Control), Individual, LogNumber, AirTemp (°C), LeafTemp (°C), RespRate (µmol m^-2 s^-1).
- Units (summary):
  - DateTime: dd/mm/yyyy hh:mm
  - SolarR: Watts/m^2
  - RH: %
  - AirTemp, Temp_T, Temp_C: °C
  - Structure: categorical (Prototype, S1, S2, S3)
  - Week: integer
  - Treatment: categorical (Treatment, Control)
  - Individual: label (T1–T3, C1–C3)
  - LogNumber: integer
  - LeafTemp: °C
  - PhotosynthRate: µmol m^-2 s^-1
  - RespRate: µmol m^-2 s^-1

## Quality control and data integrity
- Sensor calibration performed against known temperatures and against each other prior to measurements.
- Anomalous readings removed pre-analysis.
- Leaves visually assessed for health before and after measurements.
- Wind-induced damage excluded from final respiration dataset (C3, day 21).

## Practical considerations for data reuse
- This dataset enables analysis of:
  - Microclimate alterations inside vs. outside WTHS and their relation to ambient conditions.
  - Temperature response curves for photosynthesis and respiration under controlled heating.
  - Short-term physiological acclimation to daytime warming over multiple weeks.
- Potential analyses:
  - Compare WTHS-induced temperature increases with changes in leaf photosynthesis and respiration.
  - Model acclimation dynamics over 2–3 weeks under elevated daytime temperatures.
  - Integrate microclimate data with physiological responses to quantify warming effects at the whole-tree level.
- Limitations:
  - Data are from specific species (D. elliptica and E. suberosum) in a Cerrado setting; generalization to other ecosystems should be done cautiously.
  - One respiration measurement was omitted due to wind damage, which may affect completeness of that time point.