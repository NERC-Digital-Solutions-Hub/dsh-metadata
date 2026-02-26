# Data from automatic water monitoring buoy from Blelham Tarn 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

## Overview
- Dataset collected from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Instruments measure air temperature, solar radiation (pyranometer), wind speed, and in-lake temperatures at multiple depths.
- Time coverage: 2012–2015; all timestamps in Greenwich Mean Time (GMT).
- Data sampling: measurements every 4 minutes; hourly averages provided.

## What is measured
- Air temperature (°C)
- Solar radiation flux (Pyranometer) (W/m^2)
- Wind speed (m/s)
- Lake water temperature (°C) at depths: 0.5 m, 1 m, 2 m, 3 m, 4 m, 5 m, 6 m, 7 m, 8 m, 9 m, 10 m, and 12 m
- Temperature sensors: platinum resistance thermometers

## Sampling regime and calculation details
- Data collection systems: Campbell Scientific datalogger (until 19 July 2012) and Oracle database (from 19 July 2012 onwards).
- Hourly averages are calculated over the previous hour, e.g., the 2 p.m. value is the average from 1–2 p.m. (excluding 1 p.m. data, including 2 p.m. data).
- All data are recorded in GMT.

## Quality control and data quality
- Data are raw and not yet calibrated or quality controlled.
- Visual checks performed; obvious hardware malfunctions removed.
- Gaps occur due to buoy maintenance or sensor/logger problems.

## Data structure and contents
- Data provided as CSV with:
  - Date_GMT: date and time of measurement (GMT)
  - Water_temperature at depths: 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m
  - Air_Temperature (°C)
  - Pyranometer (Solar radiation) (W/m^2)
  - Wind Speed (m/s)

## Usage notes and applications
- Used in multiple current scientific studies, including work by PhD students.
- Suitable as a data source for time-series analyses of lake thermal structure and meteorological conditions.
- Users should perform calibration and additional quality control before formal analyses or public dissemination.