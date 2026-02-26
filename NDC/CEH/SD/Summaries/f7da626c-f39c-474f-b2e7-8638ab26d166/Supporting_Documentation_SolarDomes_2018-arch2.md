# Summary

- Location and facility
  - Rural site in North Wales, UK, part of Bangor University farm; near the sea.
  - Eight solardomes used in 2018 to study ozone effects; three domes were heated by 7°C to simulate tropical/subtropical conditions.
  - Ozone added via a computer-controlled LabView system; exposure follows a weekly repetitive ozone episode, including night-time additions.
  - Plants watered as needed; ozone exposure ended at different times for different species.

- Experimental design
  - Four replicate pots per species/cultivar.
  - Continuous hourly sampling of ozone and meteorological conditions.
  - Varying exposure lengths by species/cultivar; ad-hoc stomatal conductance measurements with soil moisture and chlorophyll content index tracking.
  - End-of-experiment biomass and yield measurements for all species/cultivars.

- Treatments
  - Treatments combine ozone level and temperature regime:
    - Medium ozone, unheated: target peaks at 35 ppb; ambient temperature ~.
    - Medium ozone, unheated with higher peak: 80 ppb.
    - High ozone, unheated: 35 ppb with 115 ppb peak.
    - Low ozone, heated: 35 ppb with ambient temperature +7°C.
    - Medium ozone, heated: 35 ppb at 80 ppb peak with ambient +7°C.
    - High ozone, heated: 35 ppb at 115 ppb peak with ambient +7°C.

- Crop species and varieties
  - Beans: Mbombo, Rajama, Tiger.
  - Cowpeas: Blue Goose, Hog brains, Old Timer, Razorback, Whippoorwill.
  - Amaranth: Pygmy Torch, Juana's Orange.
  - Sorghum: IS1004, IS27557.

- Data collection and instrumentation
  - Ozone and meteorology logged automatically; QA checks for plausibility and gap-filling as needed.
  - Plant physiology data collected ad-hoc (stomatal conductance via AP4 porometer, soil moisture via theta probe, Chlorophyll Content Index via CCM-200).
  - Calibration: AP4 porometer calibrated daily; ozone analyzers calibrated externally; CCM-200 autocalibration step on startup.

- Data products and metadata
  - Biomass_and_Yield_2018.csv: growth metrics by species, treatment, replicate; includes pod/bean counts and weights, seed head data for amaranth; notes on yield.
  - Ozone_and_meteorology_2018.csv: hourly ozone, meteorology with columns for DOY, date, hour, ozone (ppb), light, temperature, VPD, pressure, wind speed, precipitation (dummy value).
  - Plant_Physiology_2018.csv: plant-level physiology measurements (abbreviated treatment, species, replicate, date/time, RH, stomatal conductance, light, temperature, soil moisture, CCI).
  - Three CSV files total; some fields blank where readings were not obtained.
  - Data quality and QA documented; gaps and missing values described.

- Data quality control and gap filling
  - Automated logging with range checks and plausibility tests; gaps filled per Appendix 1:
    - Ensure 24 hourly values per day; gaps ≤5 hours filled by averaging adjacent values.
    - Larger gaps reconciled using patterns from the lab book; day-to-day values used to fill when appropriate.
    - Periods when the ozone system was off filled with a 5 ppb dummy value.
  - Outliers identified and adjusted using neighboring data; negative ozone values set to zero; higher-than-expected values checked for plausibility.

- Appendix 1: gap filling methodology
  - Detailed protocol for handling gaps, including logic for small vs. large gaps and when to use previous/next day values.
  - Maintains an original amended copy of data; all changes recorded as separate “filled and corrected” datasets.

- Miscellaneous and access
  - Facility and methodology described publicly at CEH research facilities page.
  - Data resources organized to support standardized monitoring outputs and potential data reuse beyond a single study.