# Ozone Exposure Experiment in Solardomes (2017) - Rural North Wales, UK

- Location and facility
  - Rural site in North Wales, UK, part of Bangor University farm, near the sea.
  - Eight hemi-spherical solardomes used for experiments in 2017; three heated +7°C above ambient to mimic tropical/subtropical conditions.
  - Ozone addition controlled by LabView software; profiles follow a weekly ozone episode, applied day and night.
  - Plants watered as needed; ozone exposure ended at different times for different species.

- Experimental design
  - Four replicate pots per species/cultivar.
  - Ozone and meteorological conditions continuously logged hourly.
  - Ad-hoc measurements of stomatal conductance; accompanying soil moisture and chlorophyll content index measurements.
  - Yield determined at the end of the experiment for all species/cultivars.
  - Start/end dates for species groups vary; e.g., multiple wheat cultivars span 18 May–25 July 2017; various millets, beans, cowpeas, and others have corresponding end dates.

- Treatments and conditions
  - Treatments include:
    - Low ozone, unheated: target peak 35 ppb, ambient temperature.
    - Medium ozone, unheated: target peak 80 ppb, ambient temperature.
    - High ozone, unheated: target peak 115 ppb, ambient temperature.
    - Low ozone, heated: 35 ppb, ambient temperature +7°C.
    - Medium ozone, heated: 80 ppb, ambient temperature +7°C.
    - High ozone, heated: 115 ppb, ambient temperature +7°C.
  - Ozone exposure follows a predefined weekly pattern; measurements include hourly ozone and meteorology data.

- Data collected and structure
  - Ozone and meteorology data (Ozone_and_meteorology_2017.csv): 11 columns, 18,534 rows.
    - Variables include: Treatment, Day_of_Year, Date, Hour_of_Day, Ozone_ppb, Light_in_dome, temperature, Vapour Pressure Deficit, Air_pressure, Windspeed, precipitation.
    - Model inputs (DO3SE) require fixed values for air pressure, wind speed, and precipitation; wind is constant due to dome fans, and precipitation set to 1 mm/hour as a dummy value.
  - Plant physiology data (Plant_Physiology_2017.csv): 11 columns, 3,112 rows.
    - Variables include: Treatment, Plant_Species, Pot_Number, Date, Time, Leaf_side, stomatal_conductance, Light_PAR, Leaf_Temperature, Soil_Moisture, Chlorophyll_Content_Index.
  - Biomass and yield data (Biomass_and_Yield_2017.csv): 17 columns.
    - Variables include: Plant_Species_and_variety, Treatment, Pot_Number, Pod_Number, Pod_weight_grams, Bean_number, Bean_weight_grams, Seed_head_total_weight_grams, Average_pod_weight_grams, Average_bean_weight_milligrams, Average_beans_per_pod_number, total_weight_of_all_grains_grams, 100_grain_weight_grams, Number_of_Ears, Calculated_number_of_grains_per_ear, Calculated_total_number_of_grains.
  - Data notes: Some blanks indicate readings were not taken or unavailable; a small number of measurements missing due to QA issues.

- Data quality control and calibration
  - Ozone and meteorology data logged automatically with QA checks for range and plausibility; gaps filled as needed (see gap-filling protocol).
  - Plant physiology data collected ad-hoc with QA checks for plausibility.
  - Biomass and yield data QA-checks for appropriate range and plausibility.
  - Instrument calibration:
    - Stomatal conductance: AP4 porometer calibrated daily.
    - Ozone analysers: calibrated by external provider (Air Monitors Ltd).
    - Chlorophyll Content Index: CCM-200 autocalibrates during startup.

- Gap filling and data processing
  - Gaps identified to ensure at least one data row per hour for every day.
  - Gaps ≤ 5 hours filled by averaging surrounding values.
  - Larger gaps: reference lab book; fill using values from same time on previous and following day, adjusted to maintain patterns; when the system was not running, missing values set to a dummy 5 ppb.
  - Data amendments are documented by creating a separate 'filled and corrected' dataset to preserve the original data.

- Documentation and access
  - Gap filling protocol documented in Appendix 1.
  - Miscellaneous: facility described on CEH website (link provided in original document).

- Considerations for data users (Data Leaders perspective)
  - Clear linkage between treatments, species, and measurement outputs enables evaluation of ozone–plant response across diverse taxa and conditions.
  - Comprehensive metadata (treatment names, dates, hourly measurements, instrument calibrations) supports reproducibility and cross-study comparisons.
  - Gaps and data corrections are transparently tracked via separate filled datasets, aiding data governance and auditability.
  - DO3SE model compatibility is supported by standardized hourly fields and surrogate constants where site measurements are unavailable.