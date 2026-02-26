# Ozone and Meteorology 2019

- Overview
  - Rural site in North Wales, UK, part of Bangor University farm; near the sea.
  - Eight solardomes used for the experiment in 2019; ozone added with computer control (LabView).
  - Three domes were heated above ambient temperature by 7°C to mimic tropical/subtropical conditions.
  - Plant biomass and physiology data available only for the three heated domes.
  - Ozone exposure followed a weekly profile (night and day), with irrigation as needed; exposure ended at different times for different species.

- Experimental Design
  - Four replicate pots per species/cultivar.
  - Ozone and meteorological conditions logged hourly throughout exposure.
  - Ad-hoc measurements of stomatal conductance, soil moisture, and chlorophyll content index collected during exposure.
  - End-of-experiment biomass/yield measured for all species/cultivars.
  - Start/end dates per cultivar provided (e.g., sweet potato and several bean cultivars from June to October 2019).

- Treatments
  - Low ozone, heated: target peak 35 ppb, ambient temp + 7°C.
  - Medium ozone, heated: target peak 80 ppb, ambient temp + 7°C.
  - High ozone, heated: target peak 115 ppb, ambient temp + 7°C.

- Data Collected and Collection Methods
  - Ozone and meteorology data collected automatically by PC with hourly timestamps; QA performed to check ranges and plausibility; gap-filling as needed.
  - Plant physiology data collected ad-hoc during exposure with QA checks.
  - Biomass and yield data measured at the end of the experiment.
  - Instruments: LabView-controlled solardome ozone system, AP4 porometer for stomatal conductance, Delta-T theta probe for soil moisture, CCM-200 for chlorophyll content index.

- Data Files and Structure
  - Plant_Physiology_2019.csv: 12 columns, 692 rows; data available for sweet potato only; blank cells indicate missing readings.
  - Ozone_and_meteorology_2019.csv: 11 columns, 10,008 rows; hourly data; gaps logged and filled; constant air pressure and wind speed assumed; dummy 1 mm/hour precipitation to support DO3SE model.
  - Biomass_and_Yield_2019.csv: 11 columns, 63 rows; bean yields per plant; tuber yield for sweet potato; blanks indicate missing readings.
  - Notes: All three are CSV files; blank cells denote unavailable readings.

- Data Processing, Calibration, and Quality Control
  - Ozone instruments calibrated by an external company; ozone data QA for plausibility and ranges; meteorological QA likewise; plant physiology QA for plausibility.
  - Calibration specifics: AP4 porometer calibrated daily; ozone analysers externally calibrated; CCM-200 autocalibrates during startup.
  - DO3SE model inputs used for ozone flux calculations; constant wind speed and modeled wind/pressure values incorporated.

- Gap Filling Protocol
  - Documented process to fill gaps and preserve original data (amended copies saved separately).
  - Gap identification ensures a row for every hour of every day.
  - Gaps ≤ five consecutive hours: fill with average of surrounding values.
  - Longer gaps: consult lab book; fill using previous and next day values (time-matched); adjust if needed to reflect patterns.
  - If system not running and data missing: fill with a dummy value (e.g., 5 ppb) for ozone data to maintain model continuity.
  - Anomalous values identified and replaced using adjacent legitimate values; data validation rules applied.

- Additional Information
  - Facility website for the experimental setup: https://www.ceh.ac.uk/our-science/research-facilities/solardomes-and-ozone-fieldrelease-system
  - Gap-filling protocol described in Appendix 1; emphasis on maintaining original data alongside amended copies.