# Summary

- Overview
  - Description of an ozone exposure experiment conducted at a rural site in North Wales, UK, part of Bangor University farm.
  - Eight solardomes used in 2018; near the sea; coordinates: 53°14'N, 4°01'W; elevation 15 m.
  - Experimental setup included four replicate pots per species/cultivar, with four species/cultivars tested under varying ozone and temperature treatments (heated vs unheated; different ambient temperature profiles).

- Site and Experimental Setup
  - Ozone was injected according to a set weekly profile and controlled by LabView software; ozone added both at night and during the day.
  - Three heated solardomes simulated tropical/subtropical conditions (+7°C) for the experiment.
  - Measurements included continuous hourly ozone and meteorological data; plant physiology was measured ad-hoc; biomass/ yield assessed at harvest.
  - Watering was provided as needed; exposure times varied by species/cultivar due to growing-season differences.

- Treatments and Sampling Regime
  - Treatments described by abbreviations (e.g., Medium/Low/High ozone with heated or unheated conditions; target peak ozone levels around 35 ppb, with higher ambient targets up to 115 ppb in some treatments).
  - Species/cultivar list includes Bean, Cowpea, Amaranth, and Sorghum with multiple cultivar entries and sampling date ranges (start vs end of exposure).

- Data Collected and File Structure
  - Ozone_and_meteorology_2018.csv: hourly records of ozone, meteorology, and derived model inputs (DOY, Date, HOD, Light, VPD, pressure, windspeed, precipitation).
  - Plant_Physiology_2018.csv: measurements of stomatal conductance, relative humidity, light, temperature, soil moisture, Chlorophyll Content Index, and other plant-state readings; includes date, time, pot number, leaf side, etc.
  - Biomass_and_Yield_2018.csv: end-of-experiment biomass and yield metrics by species/cultivar, including pod/bean counts and weights, seed heads, and notes on yield per plant.
  - Data gaps and missing values are annotated; blank cells indicate unavailable readings.
  - Appendix 1 documents a gap-filling procedure for ozone and canopy monitoring data.

- Instrumentation and Calibration
  - Solardome ozone exposure system controlled by LabView (NI, version 2012).
  - Stomatal conductance measured with AP4 porometer; soil moisture with a theta probe; Chlorophyll Content Index with CCM-200.
  - Calibration: AP4 porometer calibrated daily; ozone analyzers calibrated by external supplier; CCM-200 autocalibration upon startup.

- Data Quality Control
  - Automated QA for ozone and meteorology data (range checks, plausibility of outliers, gap-filling when necessary).
  - Plant physiology data QA checks (range validity, outlier plausibility).
  - Biomass/yield data QA for data range and plausibility.

- Gap Filling and Data Processing (Appendix 1)
  - Gaps identified for each day-hour; rows ensured for all 24 hours per day.
  - Gaps ≤ 5 consecutive hours: fill with average of preceding and following values.
  - Larger gaps: consult lab notebook; fill using previous/next day values; adjust to preserve data patterns; when the ozone system was off, fill with a dummy value of 5 ppb.
  - Anomalous values (e.g., negative ozone) corrected using neighboring values; changes are logged in separate amended copies.

- Miscellaneous and Access
  - External facility description: link to CEH solardomes and ozone field release system.
  - No analytical methods were applied to the data within this description (Analytical Methods section states: No analysis performed).

- GIS-Relevant Highlights
  - Precise geospatial context provided (latitude, longitude, elevation) enabling spatial joins with other GIS layers.
  - Time-series data at hourly resolution across multiple treatments and species allows mapping of ozone exposure patterns, temperature regimes, and plant responses by space and time.
  - Three key CSV files offer structured, graph-ready datasets for spatial analyses, modelling (e.g., DO3SE-related flux calculations requiring wind, pressure, and other inputs), and integration with other environmental geodata.

- Reference and Data Availability
  - Data are organized into three CSV files with clearly labeled variables and documentation in the Appendix.
  - Dataset supports GIS-led analyses of environmental exposure, plant response, and yield outcomes across a controlled field facility.