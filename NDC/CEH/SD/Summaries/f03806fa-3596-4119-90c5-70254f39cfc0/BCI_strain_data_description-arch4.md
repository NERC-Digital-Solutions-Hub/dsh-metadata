# BioMech Tree Strain Data on Barro Colorado Island, Panama, 2022

## Overview
- Dataset collected on Barro Colorado Island, Panama, in 2022.
- Purpose-built BioMech sensors measured bending strains on 108 trees (two sensors per tree, recording two axes of motion).
- Data collected at 4 Hz; used to analyze wind effects and tree responses.

## Collection methods
- BioMech sensors based on load cells, mounted on tree trunks with screws.
- Two sensors per tree attached perpendicularly to capture two axes of motion.
- Each sensor reports data independently to a base station.

## Nature and units of recorded values
- Raw data recorded as millivolts (mV), converted to bending strain values.
- Sampling rate: 4 Hz.
- Hourly data format (14400 rows per hour) with 216 strain data columns (two sensors per tree across 108 trees).

## Quality control
- Random time-series checks show smoothly varying data; higher variation during windy periods.
- Missing data are frequent due to:
  - Low-power, lossy data transmission.
  - Humidity and battery-related equipment failures over time.

## Details of data structure - raw data
- Each file contains one hour of data; file names end with the hour timestamp (Panama local time) to align with ERA5 conventions.
- First row contains the timestamp; subsequent rows include millisecond markers and per-sensor strain values.
- Columns are organized as pairs per sensor; for each tree, the lower sensor ID defines the TreeID (e.g., TreeID 54 uses sensors S54 and S55).
- Example shows values interleaved with NA where data were unavailable.

## Sampling regime
- Monitored 108 trees, focusing on five common species (Jacaranda copaia, Anacardium excelsa, Virola spp, Dipteryx odorata, Handroanthus guyacan).
- Selection aimed to maximize wind exposure variation (sheltering effects) by tree size and topography.

## Fieldwork instrumentation
- Two sensors per tree attached at right angles to the trunk; data transmitted separately.
- Issues with missing data often affect only a single sensor within a pair, complicating interpretation.

## Calibration steps and values
- Raw mV values converted to bending strain using calibration coefficient: 0.0001104799.
- Calibration performed by comparing BioMech sensors to a commercial extensometer.

## Calculating hourly maximum strain
- Processing steps per hour and per sensor:
  1. Remove offset by detrending (linear) to isolate bending.
  2. Combine the two perpendicular sensors for each tree using the Pythagorean theorem.
  3. Compute hourly maxima and 99th percentile.
- Offsets arise from manufacturing and environmental factors (temperature, growth) and vary slowly; removal is essential.

## Hourly maxima file format
- File: BCI_strain_hourly_maxima.csv (summary in long format per hour per tree)
- Columns:
  - Datetime (Panama local time) for the preceding hour
  - Wind_speed_mean_era5_ms (mean wind speed for the hour, ERA5)
  - gust_speed_era5_ms (gust wind speed for the hour, ERA5)
  - Wind_direction_era5 (mean wind direction for the hour, ERA5)
  - Tree_id (identifier for the tree)
  - Bending_strain_max (hourly maximum bending strain)
  - Bending_strain_q99 (hourly 99th percentile bending strain)
  - Completeness (proportion of non-NA values in the file)