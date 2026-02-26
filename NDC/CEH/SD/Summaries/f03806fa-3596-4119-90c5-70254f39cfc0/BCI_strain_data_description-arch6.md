# 1. Collection methods

- Meta-data describes data collected on Barro Colorado Island, Panama, in 2022.
- BioMech sensors measured bending strains on 108 trees; two sensors per tree mounted on the trunk perpendicular to capture two axes.
- Data collected at 4 Hz and recorded as mV, later converted to strain.

# 2. Nature and Units of recorded values

- Raw measurements are in millivolts (mV) at 4 Hz.
- Values are converted to bending strain using a calibration coefficient (see section 7).

# 3. Quality control

- Random samples of time-series inspected; data show smoothly varying patterns with higher variation during windy periods, indicating measurement validity.
- Missing data are common due to two main issues: lossy, low-power data transmission; and humidity/battery-related sensor failures over time.
- Completeness of data varies over time and by sensor.

# 4. Details of data structure - raw data

- Raw data files contain one hour of data each, at 4 Hz (14400 rows per file).
- File names end with the hour timestamp; times are in Panama local time.
- First row provides the datetime to the second; second column is milliseconds.
- Remaining columns: 216 strain values (two sensors per each of 108 trees).
- Columns follow a fixed naming scheme; TreeID maps to sensor pairs (e.g., TreeID 54 uses sensors s54 and s55).
- Some entries are NA when data were unavailable (often due to battery issues).

# 5. Sampling regime

- 108 trees sampled, focusing on five species: Jacaranda copaia, Anacardium excelsa, Virola spp, Dipteryx odorata, Handroanthus guyacan.
- Additional species sampled when primary ones were not nearby.
- Selection aimed to maximize wind exposure variation to test sheltering effects.
- Trees sampled across different sizes and topographic positions.

# 6. Fieldwork instrumentation

- Two sensors attached per tree, perpendicular to each other to measure two axes of motion.
- Sensors screwed into the wood; each sensor reports separately to a base station.
- Missing data often occur for a single sensor within a pair, complicating interpretation.

# 7. Calibration steps and values

- BioMech sensors output in mV; conversion to bending strain uses a calibration coefficient of 0.0001104799.
- Coefficient derived by calibrating BioMech sensors against a commercial extensometer.

# 8. Calculating hourly maximum strain

- Steps per hour per tree:
  1) Remove offset by computing and subtracting a linear trend for each hour/channel.
  2) Combine the two perpendicular sensors per tree using the Pythagorean theorem.
  3) Compute hourly maxima and the 99th percentile.
- Offsets arise from sensor manufacturing/installation and environmental factors; offsets vary slowly (hours) while bending varies quickly (seconds).

# 9. Hourly maxima file format

- Output file: BCI_strain_hourly_maxima.csv (long format) with per-tree hourly summaries.
- Columns:
  - Datetime: hour end timestamp in Panama local time (preceding hour data).
  - Wind_speed_mean_era5_ms: mean wind speed for the hour (ERA5).
  - gust_speed_era5_ms: gust wind speed for the hour (ERA5).
  - Wind_direction_era5: mean wind direction for the hour (degrees from North, ERA5).
  - Tree_id: identifier for the tree.
  - Bending_strain_max: maximum bending strain in the preceding hour.
  - Bending_strain_q99: 99th percentile bending strain in the preceding hour.
  - Completeness: proportion of non-NA values in the file.