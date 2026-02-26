# Temperature and humidity data supporting use of an in situ passive heating method, and associated whole tree responses, Cerrado, Brazil, 2020

## Overview
- Study to evaluate whole-tree responses to daytime warming using a novel in situ passive heating method (WTHS) in Cerrado, Brazil.
- Heat entire individuals up to 2.5 m tall by approximately 3°C during the day to assess photosynthesis and respiration responses over time.
- Includes microclimate measurements and leaf-level gas exchange (photosynthesis and respiration) across treated and control individuals.

## Experimental design and sampling regime
- WTHS setup
  - Six-sided prototype WTHS tested on a ~2.4 m Davilla elliptica tree.
  - Three additional four-sided WTHSs (S1–S3) built around Cerrado shrub Erythroxylum suberosum to assess responses in smaller plants.
  - Treatment trees (T1–T3) and controls (C1–C3) were randomly assigned for short-term heating.
- Species and replication
  - Davilla elliptica used to test the heating structure in a tree form.
  - Erythroxylum suberosum used for replicate shrub-level experiments around S1–S3.
  - Each of T1–T3 and C1–C3 measured repeatedly across weeks.
- Measurement timeline
  - Week 1: baseline photosynthesis and respiration measurements for each treated and control individual, before heating began for that set.
  - Weeks 2–4: repeated measurements at 7, 14, and 21 days after the first measurements, coinciding with heating.
  - Note: the final respiration measurement for C3 (day 21) was removed due to wind damage to the leaf.
- Data modalities
  - Microclimate inside and outside WTHSs to quantify the heating effect.
  - Leaf gas exchange to capture temperature response curves during heating.

## Microclimate data collection
- Sensors and setup
  - Temperature and relative humidity recorded every minute with DTH22 sensors in solar radiation shields; controlled by Arduino UNO.
  - One sensor placed above the crown inside each WTHS, and a corresponding sensor above a nearby control individual of the same species.
  - Ambient conditions also recorded every 15 minutes by a nearby WatchDog weather station.
- Calibration and quality
  - Sensors calibrated against known temperatures and against each other before measurements.
  - Data flagged and removed if readings were anomalous.
- Timeframe
  - Prototype WTHS: June 9–27, 2020 for Davilla elliptica.
  - S1–S3 WTHSs: August 4–25, 2020 for Erythroxylum suberosum.

## Photosynthesis and respiration rate measurements
- Instruments and setup
  - LI-COR LI-6400XT portable photosynthesis systems (two units): one with a fluorometer chamber head for photosynthesis, and one with an LED chamber head for respiration.
  - Leaf selection: healthy, fully expanded leaves; two leaves per individual per day.
  - Measurements conducted 08:00–11:30 each day.
- Experimental conditions
  - CO2 concentration: 400 ppm; relative humidity (RH): 50%.
  - Light levels for photosynthesis: ~1100 μmol m⁻² s⁻¹; for respiration: 0 μmol m⁻² s⁻¹.
  - Temperature steps: leaf temperature measured and water-jacket temperatures adjusted to achieve 20–50°C in 10 incremental steps after equilibration.
  - For leaf temperature inside WTHS vs ambient: in-wths temperature T_T (inside) vs control temperature T_C (outside).
- Data capture
  - Each leaf yields a partial temperature response curve (up to 10 measurements per leaf at different leaf temperatures).
  - Measurements use consistent CO2 and RH settings throughout.
- Data quality
  - Leaves photographed and health status assessed before and after analysis.
  - Measurements conducted with established, functioning equipment to ensure comparability across treatment and control groups.

## Data structure and formats
- WeatherStationClimateData.csv
  - Content: Temperature, relative humidity, and solar radiation from the WatchDog weather station.
  - Columns: DateTime, SolarR, RH, AirTemp.
- StructuresTempRH.csv
  - Content: Temperature and relative humidity data from sensors inside treatment WTHSs and outside controls.
  - Columns: DateTime, Temp_T, Temp_C, RH_T, RH_C, Structure.
- PhotosynthesisMeasurements.csv
  - Content: Photosynthetic rates across leaf temperatures for leaves inside (treatment) and outside (control) the WTHSs.
  - Columns: Week, Treatment, Individual, LogNumber, AirTemp, LeafTemp, PhotosynthRate.
- RespirationMeasurements.csv
  - Content: Respiration rates across leaf temperatures for leaves inside (treatment) and outside (control) the WTHSs.
  - Columns: Week, Treatment, Individual, LogNumber, AirTemp, LeafTemp, RespRate.

## Units and value points
- DateTime: dd/mm/yyyy hh:mm
- SolarR: Watts per square meter (W/m²)
- RH: Relative humidity (%)
- AirTemp, Temp_T, Temp_C: Degrees Celsius (°C)
- LeafTemp: Degrees Celsius (°C)
- PhotosynthRate: μmol m⁻² s⁻¹
- RespRate: μmol m⁻² s⁻¹

## Notable considerations and limitations
- A measurement (C3 day 21 respiration) was removed due to wind-induced leaf damage.
- Field-based, in situ heating provides a realistic proxy for daytime warming in remote environments, with careful calibration and QA to ensure data reliability.

## Relevance for environmental monitoring and policy analysis
- Provides standardized, high-resolution microclimate data paired with physiological responses to warming.
- Enables consistent, comparable datasets across individuals, species, and growth forms (tree vs shrub).
- Data organization supports integration into monitoring portals and downstream analyses of environmental health and climate-response performance over time.