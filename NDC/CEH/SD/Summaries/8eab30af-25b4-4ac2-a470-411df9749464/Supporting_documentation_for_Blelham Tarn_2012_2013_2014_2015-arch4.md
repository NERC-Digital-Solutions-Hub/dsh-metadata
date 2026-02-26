# Data from automatic water monitoring buoy from Blelham Tarn 2012, 2013, 2014 and 2015

## Overview
- Dataset from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Variables captured: air temperature, solar radiation flux, wind speed, and lake water temperatures at multiple depths.
- Timeframe: measurements from 2012, 2013, 2014, and 2015; all times in GMT.
- Data are used in multiple current scientific studies (including PhD projects).

## Sampling regime and collection methods
- Instrumentation: buoy equipped with meteorological instruments and in-lake temperature sensors.
- Measured variables:
  - Air temperature (°C)
  - Solar radiation flux (W/m²) via pyranometer
  - Wind speed (m/s)
  - Lake water temperature at depths: 0.5 m, 1 m, 2 m, 3 m, 4 m, 5 m, 6 m, 7 m, 8 m, 9 m, 10 m, and 12 m
- Cadence: data recorded every 4 minutes.
- Data processing:
  - Hourly averages calculated from the 4-minute data.
  - Window definition: the value for a given hour is the average of data from the previous hour, including data from the end of that hour (e.g., 2 p.m. equals the average of 1–2 p.m., including 2 p.m. data and excluding 1 p.m. data).
  - Data handling platform change: hourly averages computed by a Campbell Scientific datalogger up to 19 July 2012, and by an Oracle database from 19 July 2012 onwards.

## Quality control
- The dataset is raw and has not been calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Gaps in data arise from buoy maintenance or sensor/logger problems.

## Data structure (columns)
- Data provided as comma separated values (CSV).
- Columns include:
  - Date_GMT (Date and time in GMT of measurement)
  - Water_temperature at depths: 0.5 m, 1 m, 2 m, 3 m, 4 m, 5 m, 6 m, 7 m, 8 m, 9 m, 10 m, 12 m
  - Air_Temperature (°C)
  - Pyranometer (Solar radiation flux in W/m²)
  - Wind Speed (m/s)

## Usage notes and considerations for data leadership
- Status: raw data not yet calibrated or quality controlled; suitable for downstream QA/QC workflows before use.
- Timeframe and coverage: 2012–2015 with multi-depth temperature profiles and meteorological context.
- Metadata and discoverability: data described with explicit depth-specific temperature columns and measurement times; potential gaps should be documented and accounted for in analyses.
- Applicability: useful as a multi-parameter, time-synchronized lake-monitoring dataset; valuable for studies requiring continuous temporal and vertical temperature profiles and surface meteorology, with caveats about calibration and data gaps.