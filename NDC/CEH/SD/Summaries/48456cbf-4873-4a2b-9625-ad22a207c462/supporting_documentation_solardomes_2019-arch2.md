# Ozone exposure experiment in solardomes at Bangor University farm, North Wales (2019)

- Overview
  - Rural site in North Wales, UK, part of Bangor University farm, near the sea, at 15 m above sea level.
  - Eight hemi-spherical solardomes used in 2019 to study ozone effects; ozone added to charcoal-filtered air in controlled profiles.
  - Three heated solardomes raised by 7°C above ambient to mimic tropical/subtropical conditions; plant biomass and physiology data available only for these heated domes.
  - Ozone exposure followed a weekly, computer-controlled profile (LabView); ozone added at night and day.
  - Plants watered as needed; exposure ended at different times per species.

- Experimental Design
  - Four replicate pots per species/cultivar grown from seed and exposed to ozone.
  - Continuous hourly logging of ozone and meteorological conditions; ad-hoc plant physiology measurements (stomatal conductance, soil moisture, chlorophyll content index).
  - End-of-experiment biomass/yield measured for all species/cultivars.
  - Species included: Sweet potato (Erato orange) and beans (Orca, Pinto, Rajama, Turtle); exposure dates span 13/06/2019 to 1/10/2019 for most, with variations by species.

- Treatments
  - Low ozone, heated: target peak 35 ppb, ambient temperature +7°C.
  - Medium ozone, heated: target peak 80 ppb, ambient temperature +7°C.
  - High ozone, heated: target peak 115 ppb, ambient temperature +7°C.

- Data Collection and Instrumentation
  - Ozone and meteorology data logged automatically by PC; QA performed to ensure valid ranges and plausible outliers; gap-filling as needed.
  - Plant physiology data collected ad-hoc; QA for range and plausibility.
  - Biomass and yield measured at experiment end.
  - Instrumentation:
    - LabView-controlled solardomes ozone exposure system.
    - AP4 porometer for stomatal conductance.
    - Theta probe for soil moisture.
    - CCM-200 chlorophyll content index device (autocalibration in turn-on).

- Calibration
  - AP4 porometer calibrated daily per manufacturer instructions.
  - Ozone analyzers calibrated by external vendor (Air Monitors Ltd).
  - CCM-200 autocalibrates during startup.

- Data Resources and Structure
  - Biomass_and_Yield_2019.csv: 63 rows; fields include species, treatment, pot and pod metrics, bean counts/weights, tuber weight for sweet potato.
  - Ozone_and_meteorology_2019.csv: 10008 rows; fields cover treatment, date/time, hourly ozone, light, temperature, humidity-related variables, wind speed (constant in domes), air pressure (constant proxy), precipitation (dummy value).
  - Plant_Physiology_2019.csv: 692 rows; 12 columns; data available only for sweet potato; blanks indicate missing readings.
  - Data quality notes: three CSV files total; blanks indicate unavailable readings; some short logging gaps and data adjusted via gap-filling protocol.

- Data Quality Control and Gap Filling
  - Automated QA for ozone and meteorology, with plausibility checks and gap-filling.
  - Plant physiology QA for reasonable ranges and plausibility.
  - Biomass/yield QA for range and plausibility.
  - Gap filling protocol:
    - Ensure 24 hourly data rows per day.
    - Gaps ≤ 5 consecutive hours filled with average of surrounding values.
    - Larger gaps checked against lab notes; fill using previous/next day values when appropriate.
    - If system not running, fill with a 5 ppb dummy value for ozone.
    - Anomalous values identified and corrected using adjacent values; maintained with an amended copy and kept as separate “filled and corrected” data.

- Miscellaneous
  - Facility description available at: https://www.ceh.ac.uk/our-science/research-facilities/solardomes-and-ozone-fieldrelease-system
  - Note: Data are prepared for standardized environmental health monitoring analyses, enabling cross-study comparison and model-facing inputs (e.g., DO3SE model prerequisites).