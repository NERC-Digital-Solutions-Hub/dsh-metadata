# BioMech Tree Strain Data on Barro Colorado Island, Panama, 2022

- Overview
  - Purpose: measure bending strains on 108 trees using purpose-built BioMech sensors to study wind effects.
  - Data capture: two sensors per tree, orthogonal axes, recording at 4 Hz; data stored in raw files and summarized in an hourly maxima file.
  - Time reference: timestamps are in Panama local time.

- Data Collection and Instrumentation
  - Trees and sampling: 108 trees focused on five common species (Jacaranda copaia, Anacardium excelsa, Virola spp, Dipteryx odorata, Handroanthus guyacan) with variation in wind exposure, size, sheltering by neighbors, and topography.
  - Sensor setup: two perpendicular strain sensors per tree, screws mounted into the trunk, each reporting separately to a base station; data gaps can occur if individual sensors fail.

- Sensor Details and Calibration
  - Raw measurements: millivolt (mV) readings converted to bending strain via calibration coefficient 0.0001104799.
  - Calibration basis: coefficient calibrated against a commercial extensometer.

- Data Structure and File Formats
  - Raw data (hourly files): each file covers one hour, 4 Hz, totaling 14,400 rows; 216 strain columns (two sensors per tree for 108 trees); always include columns for all sensors with NA where data are missing.
  - Naming convention: columns named by sensor IDs; tree ID is the lower of each sensor pair (e.g., TreeID 54 uses sensors S54 and S55; TreeID 56 uses S56 and S57).
  - Example structure: alternating time, milliseconds, followed by sequential sensor readings; NA entries appear when data are unavailable.
  - Time format: datetimes align with ERA5 conventions for comparability.

- Data Quality and Gaps
  - Quality checks: random time-series inspections show smoothly varying data, with greater variation during windy periods.
  - Gaps: significant missing data due to lossy, low-power transmission and humidity/battery-related sensor failures; missing data can occur at the sensor level within a tree.

- Processing and Calculation of Hourly Maxima
  - Steps per hour per sensor/axis:
    - Remove offset by detrending (linear trend) for that hour and channel.
    - Combine the two perpendicular sensors per tree using the Pythagorean theorem to get a single per-tree signal.
    - Determine hourly maxima and the 99th percentile (q99) for bending strain.
  - Offset considerations: raw strains have a slowly varying offset due to sensor manufacturing and installation; offset removal preserves fast bending variation.

- Hourly Maxima Dataset
  - File: BCI_strain_hourly_maxima.csv (hourly maxima summary).
  - Columns:
    - Datetime: hour-end timestamp (Panama local time); maxima calculated for the preceding hour (e.g., 14:00:00 covers 13:00–14:00).
    - Wind_speed_mean_era5_ms: mean wind speed for the hour from ERA5.
    - gust_speed_era5_ms: hourly gust wind speed from ERA5.
    - Wind_direction_era5: mean wind direction (degrees from North) for the hour from ERA5.
    - Tree_id: identifier for the structure (per tree) to which the bending strain maxima pertain.
    - Bending_strain_max: maximum bending strain in the preceding hour.
    - Bending_strain_q99: 99th percentile bending strain in the preceding hour.
    - Completeness: proportion of non-NA values in the file.
  - Format difference: the hourly maxima file is in long format (per-tree per-hour records) whereas the raw data is wide (one column per sensor).

- Fieldwork and Data Context
  - Fieldwork setup: two sensors per tree, individually reporting data; data integrity can vary by sensor within a pair.
  - Purpose for GIS: enables map-based visualization of wind-induced tree bending across the study area, aligned with ERA5 wind fields for spatial-temporal analyses.

- Limitations and Considerations for GIS Use
  - Data gaps due to power/battery and environmental conditions; need to account for missingness in spatial analyses.
  - Local time stamps require consistent time zone handling when integrating with other datasets (e.g., ERA5).
  - Some species and site variations are embedded in the sampling design, useful for exploring sheltering effects and wind exposure across a landscape.