# BioMech Sensor Strain Data from Barro Colorado Island, Panama (2022)

- Purpose and scope
  - Collect environmental health measures by recording wind-induced bending strains in tree trunks to understand wind exposure, sheltering effects, and related ecological responses.
  - Data intended to inform monitoring frameworks, policy decisions, and future analyses of environmental health risks.

- Study site and sampling design
  - Barro Colorado Island (BCI), Panama, 2022.
  - Monitored 108 trees across five common species: Jacaranda copaia, Anacardium excelsum, Virola spp, Dipteryx odorata, Handroanthus guyacan (with other species sampled if these were not available nearby).
  - Sampling aimed to maximize variation in wind exposure (sheltering effects) by selecting trees of different sizes and topographic positions.

- Field instrumentation and collection
  - Two BioMech strain sensors per tree, mounted perpendicularly on the trunk to capture two axes of motion.
  - Sensors screwed into the wood, with data transmitted to a base station; single-sensor data losses contribute to missing values in pairs.
  - Sampling rate: 4 Hz (data recorded as mV and later converted to strain).
  - Calibration: mV values converted to bending strain using a calibration coefficient of 0.0001104799 (calibrated against a commercial extensometer).

- Data structure (raw data)
  - Raw data files contain hourly records (one hour per file) with 14400 rows (4 Hz).
  - 216 strain columns: two sensors for each of 108 trees (S54–S55 for TreeID 54, S56–S57 for TreeID 56, etc.).
  - File names encode the end-of-hour time; times are in Panama local time.
  - Each row includes a timestamp, sensor-specific readings, and NA values where data were unavailable (often due to battery issues).

- Data processing and quality control
  - Quality check conducted by inspecting time-series; data exhibited smooth variation with higher variability during windy periods, consistent with bending measurements.
  - Noted data gaps from:
    - Lossy, low-power data transmission.
    - Humidity-related equipment degradation and battery issues over time.
  - Offset present in raw strain data (due to sensor manufacturing/installation and environmental factors); offset removal required before analysis.

- Processing steps to derive hourly maxima
  - For each hour and sensor channel:
    - Remove offsets by subtracting a linear hourly trend.
  - For each tree (two perpendicular sensors):
    - Combine the two corrected signals using the Pythagorean theorem to obtain a single bending signal per tree per time point.
  - For each tree and hour:
    - Compute the hourly maximum bending strain.
    - Compute the 99th percentile (q99) of bending strain for the hour.
  - Result: hourly maxima reflecting the strongest bending within each tree during each hour.

- Derived data product: hourly maxima file
  - File: BCI_strain_hourly_maxima.csv
  - Columns include:
    - Datetime (Panama local time): end of the preceding hour (e.g., 14:00:00 covers 13:00–14:00)
    - Wind_speed_mean_era5_ms: mean wind speed for the hour (ERA5 data)
    - gust_speed_era5_ms: gust wind speed for the hour (ERA5 data)
    - Wind_direction_era5: mean wind direction for the hour (ERA5 data)
    - Tree_id: identifier for the tree
    - Bending_strain_max: hourly maximum bending strain
    - Bending_strain_q99: hourly 99th percentile bending strain
    - Completeness: proportion of non-NA values in the hourly file
  - Format: long (hourly maxima per tree) vs. raw data format (wide, one column per sensor)

- Interpretation and usage notes
  - The hourly maxima enable linkage with ERA5 wind data to study wind exposure and bending responses across trees and species.
  - The per-tree bending metrics (max and q99) support analyses of extreme wind loading and variability due to sheltering and topology.
  - Data artifacts to consider in analyses:
    - Missing data due to sensor failures and transmission losses; consider Completeness when including hours/trees in analyses.
    - Removal of slow-varying offsets is essential to avoid conflating sensor/environmental drift with actual bending.
  - Metadata and data governance considerations:
    - Metadata gaps can hinder reuse; documenting sensor IDs, tree IDs, and data processing steps is critical.
    - Public sharing of underlying data requires careful attention to data provenance, quality assurance, and openness at the data source.
    - Data should be accompanied by clear processing steps (offset removal, axis combination) and alignment with ERA5 time stamps for reproducibility.

- Key takeaways for monitoring framework authors
  - This dataset exemplifies a structured approach to capturing fine-scale physiological responses (tree bending) linked to atmospheric drivers (ERA5 wind data).
  - The two-sensor-per-tree, perpendicular configuration provides robust two-axis measurements that are then integrated for a single per-tree metric.
  - A transparent processing pipeline (offset removal, axis combination, and computation of max/q99) is essential for producing comparable, policy-relevant indicators.
  - The documented data gaps and transmission challenges highlight the importance of robust data governance, metadata richness, and strategies to maximize data completeness for monitoring frameworks.