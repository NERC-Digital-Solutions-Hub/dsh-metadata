# Temperature and humidity data supporting use of an in situ passive heating method, and associated whole tree responses, Cerrado, Brazil, 2020

- Objective and scope
  - Presents data supporting a novel in situ passive heating method (whole-tree heating structures, WTHS) to evaluate daytime warming responses in remote environments.
  - Demonstrates a heating approach for whole individuals up to 2.5 m tall, approximately +3°C during daytime.
  - Includes field testing on Davilla elliptica (a dominant Cerrado tree) and Erythroxylum suberosum shrubs, with short-term acclimation measurements.

- Experimental design and treatments
  - Prototype WTHS: six-sided enclosure built around a ~2.4 m Davilla elliptica; tested in a Cerrado site near Nova Xavantina, Brazil.
  - Additional four-sided WTHSs (S1–S3) constructed around Erythroxylum suberosum individuals (~2 m tall) to assess heating effects.
  - Short-term warming experiment for E. suberosum conducted from July 27 to August 23, 2020.
  - Experimental layout: three treatment individuals (T1–T3) and three controls (C1–C3); initial measurements taken before heating; subsequent measurements at 7, 14, and 21 days after heating began.
  - Outcome note: last respiration measurement (C3, day 21) excluded due to wind-induced leaf damage.

- WTHS specifications
  - Prototype: side length 140 cm per side, total perimeter 840 cm, height 270 cm, base area 5.09 m2, internal volume 13.74 m3.
  - S1: side lengths ~160–165 cm, perimeter 650 cm, height 210 cm, base area 2.58 m2, volume 5.41 m3.
  - S2: side lengths ~130–255 cm, perimeter 720 cm, height 280 cm, base area 2.93 m2, volume 8.19 m3.
  - S3: side lengths ~210–260–175–185 cm, perimeter 830 cm, height 310 cm, base area 4.19 m2, volume 12.99 m3.

- Microclimate data collection
  - Temperature and relative humidity recorded every minute with DTH22 sensors in solar shields; one sensor inside the WTHS above the plant crown and a control sensor above a nearby similarly sized individual.
  - Ambient climate monitored every 15 minutes with a nearby WatchDog weather station (ambient temperature, RH, solar irradiance).
  - Data collection window for prototype WTHS: June 9–27, 2020; for S1–S3: Aug 4–25, 2020.
  - Data aligned to a paired design (treatment vs. control) with sensors rotated across WTHSs and controls. Climate data during WTHS open/ testing periods were excluded.

- Photosynthesis and respiration measurements
  - Instruments: two LI-6400XT portable photosynthesis systems (one with fluorometer, one with LED chamberHead) for photosynthesis and respiration measurements.
  - Leaf selection: two healthy, fully expanded leaves per individual; one leaf per LI-6400XT per day.
  - Measurement timing: 08:00–11:30 daily.
  - Procedure: leaves tested at 10 leaf-temperature steps from 20°C to 50°C; full equilibration at each step.
  - Environmental conditions during measurements: CO2 400 ppm, RH 50% for both photosynthesis and respiration; photosynthesis leaf measurements used ~1100 µmol m-2 s-1 light, respiration measurements used 0 µmol m-2 s-1.
  - Temperature control: temperature expansion water jackets allowed attainment of higher leaf temperatures (>40°C).

- Data quality assurance and handling
  - Sensor calibration performed before measurements; cross-checks against known steady temperatures; anomalous readings removed pre-analysis.
  - Leaves photographed and health assessed before and after analysis to ensure data integrity.
  - Data cleaning included removal of non-representative data (e.g., wind-disturbed respiration measurement).

- Data structure and content
  - WeatherStationClimateData.csv: contains ambient temperature, relative humidity, and solar radiation (DateTime, SolarR, RH, AirTemp) for 01/06/2020–01/09/2020.
  - StructuresTempRH.csv: contains temperature and RH data inside treatment structures and outside controls (DateTime, Temp_T, Temp_C, RH_T, RH_C, Structure) across the prototype and S1–S3 (09/06/2020–25/08/2020).
  - PhotosynthesisMeasurements.csv: photosynthesis rates across leaf temperatures for E. suberosum inside/outside WTHSs (Week, Treatment, Individual, LogNumber, AirTemp, LeafTemp, PhotosynthRate).
  - RespirationMeasurements.csv: respiration rates across leaf temperatures for E. suberosum inside/outside WTHSs (Week, Treatment, Individual, LogNumber, AirTemp, LeafTemp, RespRate).

- Units and data definitions
  - Date and time in dd/mm/yyyy hh:mm.
  - Solar radiation in Watts per square meter (W/m2).
  - Relative humidity in percent (%).
  - Air temperature and leaf temperatures in degrees Celsius (°C).
  - Structure identifiers: Prototype, S1, S2, S3.
  - Week index (1, 2, 3, ...); Treatment labeled as Control or Treatment.
  - Leaf-level measurements include LogNumber (1–10) indicating repeated measurements at different leaf temperatures.
  - Photosynthesis rates in µmol m-2 s-1; respiration rates in µmol m-2 s-1.

- Potential uses for analysts
  - Correlate microclimate within WTHS to whole-tree physiological responses (photosynthesis and respiration) under daytime warming.
  - Compare heated vs. ambient conditions to quantify acclimation over 3+ weeks.
  - Integrate multi-sensor microclimate data with leaf-level gas exchange to develop predictive models of plant response to daytime warming in tropical savanna ecosystems.
  - Use provided metadata and structured CSVs to ensure data provenance and reproducibility in subsequent analyses.