# Data from automatic water monitoring buoy from Esthwaite Water 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly S.C. (2017)

## Overview
- Location: Esthwaite Water, Cumbria, England
- Instrumentation: automatic lake monitoring buoy with meteorological sensors and in-lake temperature sensors
- Measured variables: air temperature (°C), solar radiation flux (W/m^2), wind speed (m/s), lake water temperatures at depths 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 and 12 m
- Cadence and processing: data collected every 4 minutes; hourly averages computed by Campbell Scientific datalogger (hour defined as the interval from the previous hour to the current hour, excluding the start of the hour)
- Timeframe: data from 2012, 2013, 2014, and 2015, all in GMT
- Usage: used in multiple current scientific studies, including PhD research

## Quality control and caveats
- Data are raw and not yet calibrated or quality controlled
- Visual checks conducted; obvious hardware-related errors removed
- Gaps attributed to buoy maintenance or sensor/logger issues
- Temperature chain updated in August 2015

## Data structure and format
- Format: comma separated values (CSV)
- Columns:
  - Date_GMT: date and time in GMT
  - 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m: water temperature at specified depths (°C)
  - Air_Temperature: air temperature (°C)
  - Pyranometer: solar radiation flux (W/m^2)
  - Wind_Speed: wind speed (m/s)

## Practical notes for analysts
- Data are raw; calibration may be required for high-precision analyses
- Be aware of data gaps and the 2015 instrument update when interpreting trends
- Suitable for examining relationships between atmospheric conditions and lake thermal profiles
- Provenance: associated with Jones et al. 2017; ongoing use in scientific studies including PhD work