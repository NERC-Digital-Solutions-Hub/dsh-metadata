# Data from automatic water monitoring buoy from Blelham Tarn 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

## Overview
- Data from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Measures meteorological variables and in-lake temperature profiles to support studies of lake ecology and physical processes.
- Timeframe: 2012–2015; all data in Greenwich Mean Time (GMT).

## Sampling regime and collection methods
- Instruments record: air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and lake temperatures at depths of 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 m.
- Data cadence: every 4 minutes; hourly averages are produced by a Campbell Scientific datalogger (until 19 Jul 2012) and an Oracle database (from 19 Jul 2012 onwards).
- Hourly average definition: average of the data between the previous hour and the current hour, excluding the measurement at the start of the hour and including the measurement at the end of the hour.

## Quality control
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware malfunctions removed.
- Gaps occur due to buoy maintenance or sensor/logger problems.

## Data structure and fields
- File format: CSV with the following columns:
  - Date_GMT: date and time of measurement (GMT)
  - 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m: water temperature in °C at each depth
  - Air_Temperature: air temperature in °C
  - Pyranometer: solar radiation flux in W/m²
  - Wind Speed: wind speed in m/s

## Practical notes for analysts
- Data are used in ongoing scientific studies, including by PhD students; may require calibration/quality control before rigorous analysis.
- Be mindful of missing data due to maintenance or sensor issues; verify time alignment and ensure GMT timing when merging with other datasets.
- Consider exploring vertical temperature gradients across depths and coupling with meteorological drivers (air temperature, solar radiation, wind) for ecosystem and physical-process analyses.