# BioMech Sensor Data on Barro Colorado Island, Panama, 2022

## Overview
- Data collection on Barro Colorado Island (Panama) in 2022 using purpose-built BioMech sensors to measure bending strains on 108 trees.
- Two sensors per tree, mounted on perpendicular axes, to capture two independent directions of motion.
- Raw data sampled at 4 Hz and converted from millivolts to bending strain; includes hourly maxima and ERA5 wind data for analysis of wind–tree bending relationships.

## Data collection and sensors
- 108 trees across five common species (Jacaranda copaia, Anacardium excelsa, Virola spp, Dipteryx odorata, Handroanthus guyacan); additional species sampled if nearby.
- Two sensors per tree, mounted perpendicularly on the trunk; both sensors report independently to a base station.
- Missing data can occur for individual sensors within a pair, complicating interpretation of some observations.

## Data recording and units
- Raw measurements: millivolts (mV) at 4 Hz, converted to bending strain using a calibration constant.
- Calibration constant: 0.0001104799, derived by calibrating against a commercial extensometer.

## Data quality and limitations
- Quality checks show smoothly varying data with higher variation during windy periods.
- Major data gaps due to: (1) lossy, low-power data transmission; (2) humidity and battery-related sensor/ hardware failures over time.
- Completeness declines as the data collection period progresses.

## Raw data structure
- Each hour is stored as a file with 14,400 rows (4 Hz × 3600 s) and 216 strain columns (two sensors per 108 trees).
- File names encode the end time of the hour; times are in Panama local time.
- First row provides the datetime (to the nearest second); subsequent entries include milliseconds and strain values for each sensor.
- Tree mapping: TreeID corresponds to the lower of each sensor pair; an example mapping is TreeID 54 uses sensors S54 and S55, TreeID 56 uses S56 and S57.
- Data may include NA values when data were unavailable (e.g., battery issues).

## Sampling regime and fieldwork instrumentation
- Sampling aimed to maximize wind exposure variation to test sheltering effects.
- Trees chosen to span different sizes and topographic positions.
- Two sensors per trunk, oriented at right angles; data from each sensor transmitted separately to a base station.

## Calibration
- Raw sensor outputs (mV) are converted to bending strain using the calibration factor 0.0001104799.
- Calibration validated against a commercially available extensometer.

## Calculating hourly maximum strain
- Steps per hour per sensor pair:
  - Remove offset by detrending to address slow-varying offsets due to temperature, growth, and manufacturing errors.
  - Combine the two axis signals per tree using the Pythagorean theorem to yield a single bending signal per tree.
  - Compute the hourly maximum bending strain and the hourly 99th percentile (q99) for each tree.
- Offsets are slow-varying (hours) while bending varies on the scale of seconds.

## Hourly maxima file format
- Available as BCI_strain_hourly_maxima.csv (long format: one row per tree per hour).
- Columns:
  - Datetime: Hourly timestamp in Panama local time for the preceding hour.
  - Wind_speed_mean_era5_ms: Mean wind speed (m/s) for the hour from ERA5 data.
  - gust_speed_era5_ms: Gust wind speed (m/s) for the hour from ERA5 data.
  - Wind_direction_era5: Mean wind direction (degrees from North) for the hour from ERA5 data.
  - Tree_id: Identifier for the tree.
  - Bending_strain_max: Hourly maximum bending strain for the tree in that hour.
  - Bending_strain_q99: Hourly 99th percentile bending strain for the tree in that hour.
  - Completeness: Proportion of non-NA values in the file (data completeness indicator).

## How to use for analysis
- Link bending strain (max and q99) with ERA5 wind metrics to assess wind-induced bending and sheltering effects.
- Explore species- and size-specific bending responses; examine spatial/topographic variation via Tree_id groupings.
- Account for data quality by using Completeness and addressing missing sensor data within hours.
- The dataset enables correlation analyses, predictive modeling of bending under wind conditions, and assessments of data gaps and reliability.