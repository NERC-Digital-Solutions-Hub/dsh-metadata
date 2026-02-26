# BioMech Tree Strain Data on Barro Colorado Island, Panama, 2022

- Objective and scope
  - Metadata and data collected on Barro Colorado Island, Panama, in 2022.
  - Use BioMech sensors to measure bending strains on the trunks of 108 trees as they sway in wind.
  - Each tree monitored with two sensors to capture two independent axes of motion.

- Data collection and measurement
  - Sensors: BioMech load-cell-based strain sensors screwed into the tree trunks.
  - Sampling rate: 4 Hz (four measurements per second).
  - Data type: raw millivolt (mV) readings converted to bending strain using a calibration constant.

- Data quality and issues
  - Quality checks: random time-series inspection showed smoothly varying data with higher variation during windy periods.
  - Missing data: substantial gaps due to two main causes:
    - Low-power, lossy data transmission.
    - Humidity and battery-related sensor degradation over time.

- Raw data structure
  - Each raw data file covers one hour of measurements at 4 Hz (14400 rows).
  - Naming: file names end with the hour timestamp in Panama local time, matching ERA5 conventions.
  - Columns: 216 columns representing two sensors for each of 108 trees (S54–S55 for TreeID 54, S56–S57 for TreeID 56, etc.).
  - Data representation: values or NA (missing) for sensors with issues (e.g., battery problems).
  - Tree and sensor mapping: tree ID inferred from the lower of the consecutive sensor IDs (even/odd pairing).
  - Temporal format: each row includes a datetime with second precision and a separate milliseconds field.

- Sampling regime and site selection
  - Species focus: Jacaranda copaia, Anacardium excelsa, Virola spp, Dipteryx odorata, Handroanthus guyacan; other species sampled when these were unavailable.
  - Experimental design: maximize wind exposure variation to test sheltering effects.
  - Tree selection: varied sizes and topographic positions to capture sheltering and exposure differences.

- Field instrumentation details
  - Two sensors per tree, oriented perpendicularly to measure two axes of motion.
  - Attachment: sensors screwed into trunk; each sensor transmits data independently to a base station.
  - Data gaps: isolated missing data often arise for a single sensor within a pair.

- Calibration
  - Raw measurements (mV) are converted to bending strain using a calibration coefficient: 0.0001104799.
  - Calibration method: coefficient derived by calibrating BioMech sensors against a commercial extensometer.

- Processing: hourly maximum strain
  - Objective: enable comparison with wind data (ERA5) by summarizing bending strain per hour.
  - Steps:
    - Offset removal: detrend each hour per channel to remove slow-varying offsets caused by temperature, sensor offsets, and growth.
    - Axis combination: combine the two perpendicular sensors for each tree via the Pythagorean theorem to obtain a single per-tree signal.
    - Hourly maxima: extract the maximum strain and the 99th percentile for each tree within the hour.

- Hourly maxima data file
  - Summary file: BCi_strain_hourly_maxima.csv (hourly maxima per tree).
  - Key columns:
    - Datetime: hour-end timestamp in Panama local time (e.g., hour from 1pm to 2pm).
    - Wind_speed_mean_era5_ms: mean wind speed for the hour from ERA5 (m/s).
    - gust_speed_era5_ms: gust wind speed for the hour from ERA5 (m/s).
    - Wind_direction_era5: mean wind direction for the hour from ERA5 (degrees from North).
    - Tree_id: identifier for the tree corresponding to the strain maxima.
    - Bending_strain_max: maximum bending strain in the preceding hour.
    - Bending_strain_q99: 99th percentile of bending strain in the preceding hour.
    - Completeness: proportion of non-NA values in the hourly file.
  - Format: long format in the summary file (one row per tree per hour), while the raw data are in a wide format (one column per sensor).

- Overall note on data usability
  - The dataset supports monitoring environmental health and wind-related tree bending over time.
  - Completeness varies by hour and sensor; users should consult the Completeness column to assess data coverage per hourly record.