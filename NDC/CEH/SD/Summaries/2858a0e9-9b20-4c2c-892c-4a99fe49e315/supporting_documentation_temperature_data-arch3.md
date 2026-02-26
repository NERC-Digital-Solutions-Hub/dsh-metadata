# Hourly water temperature of 28 experimental mesocosms and air temperature from July to September 2022

- Purpose and scope
  - Provides hourly water temperature data for an experimental mesocosm facility and corresponding air temperatures from July 6 to September 30, 2022.
  - Mesocosms are 1 m deep, 2 m diameter, about 2800 L of reservoir water; water temperature measured with two platinum resistance thermometers (PRTs) shielded by a plastic cover at mid-depth (~40 cm) and logged by a Campbell Scientific Data Logger.
  - Mesocosms labeled 1–32, with 1, 16, 17, and 32 not used in this experiment.
  - Nutrient treatment variations applied (inorganic/organic phosphorus and ammonium).
  - Air temperature measured at a weather station within the mesocosm compound (~2.7 m height).

- Temporal and spatial coverage
  - Dates: 6 July – 30 September 2022 (GMT).
  - Spatial: 28 active mesocosms (data available for individual mesocosm temperature columns: T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T18, T19, T20, T21, T22, T23, T24, T25, T26, T27, T28, T29, T30, T31) and AirT.

- Data collection and instrumentation details
  - Temperature recorded every 5 minutes; hourly averages computed by aggregating 5-minute data (an hour value equals the average of 60 5-minute readings).
  - Sensor deployment: two PRTs per mesocosm; data logged and later reconciled if sensor readings diverged.
  - Temperature data are raw at the time of reporting; some data gaps due to sensor or logger problems.
  - Data quality checks include comparison between the two sensors; if their difference < 0.2 °C, the average is used; if > 0.2 °C, data are checked against the overall average and a drifting sensor may be discarded in favor of the other sensor.

- Data processing and quality control
  - Quality control status: raw data, not yet calibrated or fully quality assured; visual checks performed and obvious hardware errors removed.
  - Data gaps are attributed to sensor or logger issues.
  - Specific processing rules applied:
    - If hourly difference between the two sensors is ≤ 0.2 °C, use the average.
    - If > 0.2 °C difference, investigate; if drift is detected, discard the drifting sensor’s data for those occasions (use single-sensor data when appropriate).
  - Recorded instances:
    - 158 occasions where only one sensor’s data were used (for some hours).
    - 391 occasions (and additional counts in later lines) of single-sensor usage due to sensor drift or malfunction.
    - 1) 158; 6) 391; 11) 1614; 20) 8; 22) 7; 24) 14; 25) 7; 31) 17 (specifics refer to single-sensor data occurrences).

- Data structure and format
  - Files: Comma-separated values (CSV).
  - Columns include:
    - Date (dd/mm/yyyy)
    - Hour (0-23)
    - T2–T31 (temperatures in °C for mesocosms 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31)
    - AirT (air temperature in °C)
  - Note: Some mesocosms (1, 16, 17, 32) are not used and therefore have no temperature columns.

- Data issues, gaps, and caveats
  - Hardware problems caused data loss:
    - Mesocosms 18, 19, 20, 29, 30, 31: overheating events on three occasions; these 5-minute data were deleted, and hourly data were calculated excluding those periods.
    - Mesocosms 5–12: logger failure from 1 Sep 11:00 to 7 Sep 14:00; no data recorded during this interval.
  - Data are not yet calibrated or fully quality controlled; gaps are due to equipment malfunctions.
  - When calibrating or validating datasets for policy monitoring, these caveats should be considered, particularly gaps, sensor drift handling, and the need for metadata to support data provenance and reproducibility.

- Data provenance, governance, and reuse
  - Data collection conducted at the UKCEH mesocosms facility.
  - Project supported by the European Union Horizon 2020 programme (AQUACOSM-plus), grant agreement No 871081.
  - Reference dataset linked to Feuchtmayr et al. (2019) for background on mesocosm trials and related methodologies.
  - Data sharing status: the dataset is provided with detailed structure and processing notes; raw data are shared with transparency about quality checks and sensor issues, aiding data governance and reproducibility.

- Relevance for monitoring frameworks
  - Demonstrates practical challenges in environmental monitoring data management:
    - Data gaps due to equipment failures and overheating.
    - Handling sensor disagreement and drift to produce a usable hourly dataset.
    - Need for clear data structure, metadata, and governance to enable downstream analysis and policy evaluation.
  - Provides a template for archiving high-frequency environmental data (5-minute to hourly) with explicit QC decisions and documentation of limitations, aiding decision-makers in interpreting results and planning future monitoring.