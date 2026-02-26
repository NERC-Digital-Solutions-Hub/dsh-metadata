# BioMech Sensor Strain Data (Barro Colorado Island, Panama, 2022)

## Overview
- Metadata describe data collected on Barro Colorado Island (BCI), Panama, in 2022 using purpose-built BioMech sensors to measure bending strains on 108 trees as they moved in wind.
- Each tree has two sensors mounted perpendicularly to capture two axes of motion; sensors are screwed into the trunk and report separately to a base station.
- Data collection aims to enable analysis of tree bending under wind, with attention to data quality and provenance.

## What is recorded and in what units
- Raw data are recorded as millivolts (mV) at 4 Hz and converted to bending strain using a calibration constant.
- Calibration constant: 0.0001104799 (derived by calibration against a commercial extensometer).
- Each raw file represents one hour of data (4 Hz → 14,400 rows) with 216 columns (two sensors per tree × 108 trees).

## Data structure and file formats
- Raw data files:
  - Filename timing follows ERA5 conventions; timestamps are in Panama local time.
  - Each row starts with a datetime (nearest second) and milliseconds, followed by strain values for each sensor.
  - Columns: 216 strain columns (two per tree). If a sensor did not report data, the value is NA; columns exist for all sensors to keep format consistent.
  - Tree-to-sensor mapping: TreeID 54 uses sensors S54 and S55; TreeID 56 uses S56 and S57, and so on.
- Hourly maxima file:
  - BCi_strain_hourly_maxima.csv includes hourly maxima and related fields for each tree.
  - Columns include:
    - Datetime (Panama local time) for the preceding hour
    - Wind_speed_mean_era5_ms (mean wind speed, m/s)
    - gust_speed_era5_ms (gust wind speed, m/s)
    - Wind_direction_era5 (direction in degrees from North)
    - Tree_id
    - Bending_strain_max (hourly maximum strain per tree)
    - Bending_strain_q99 (hourly 99th percentile strain per tree)
    - Completeness (proportion of non-NA values in the hour)

## Data processing and quality control
- Pre-processing steps:
  - Offset removal: remove slowly varying offset in each channel (value x) by detrending within each hour.
  - Per-tree synthesis: two orthogonal sensor signals per tree are combined using Pythagoras to yield a single bending signal per tree.
  - Hourly metrics: compute the hourly maximum and the 99th percentile of bending strain.
- Quality observations:
  - Random samples show smoothly varying data; higher variability during windy periods.
  - Missing data are common due to: lossy, low-power transmission, humidity-related sensor degradation, and battery issues leading to partial coverage.
  - Offsets are acknowledged as sensor/installation-related and are corrected before downstream analyses.

## Sampling regime and fieldwork
- Monitored 108 trees across five common species (Jacaranda copaia, Anacardium excelsa, Virola spp, Dipteryx odorata, Handroanthus guyacana); other species sampled when these were not nearby.
- Trees chosen to maximize wind exposure variation (sheltering effects) and covered a range of sizes and topographic positions.
- Field setup included two sensors per tree mounted perpendicular to each other; data reported to a base station, with occasional single-sensor data gaps within a pair.

## Data governance and considerations for data stewards
- Clear linkage between raw and derived data:
  - Raw data provide per-sensor time series; hourly maxima file provides a consolidated per-tree view aligned with ERA5 wind data.
- Provenance and traceability:
  - Timestamping in Panama local time; hourly alignment with ERA5 data for wind context.
  - Explicit mapping between TreeID and sensor IDs; consistent file naming and formatting to facilitate discovery and reuse.
- Data quality and transparency:
  - Documentation of calibration (constant and method) and offset removal strategy.
  - Documentation of missing data causes and their impact on analyses.
  - Completeness metric included in hourly maxima file to aid filtering and quality assessment.
- Practical governance notes:
  - Data are split into raw (high-resolution) and derived (hourly summaries) formats to support diverse analyses.
  - Users should account for potential non-interoperability issues due to sensor-based formats and missing data in late-stage processing.
  - The structure supports reproducibility: calibration parameters, processing steps, and wind data alignment are all documented.