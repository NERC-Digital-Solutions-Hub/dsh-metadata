# Data from automatic water monitoring buoy from Blelham Tarn 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

## Overview
- Automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Measures meteorological variables (air temperature, solar radiation, wind speed) and in-lake temperatures.
- Data period: 2012–2015; all times recorded in GMT.

## Sampling regime and collection methods
- Instruments include meteorological sensors and underwater temperature sensors (platinum resistance thermometers) at depths of 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 meters.
- Data cadence: measurements every 4 minutes.
- Hourly averages are reported, calculated over the preceding hour (excluding the measurement at the start of the hour, including the measurement at the end of the hour).
- Data storage transitioned from Campbell Scientific datalogger (until 19 July 2012) to an Oracle database (from 19 July 2012 onwards).

## Quality control
- Data are raw and not yet calibrated or quality controlled.
- Visual checks performed; obvious hardware errors removed.
- Gaps occur due to buoy maintenance or sensor/logger problems.

## Data structure and variables
- Data format: CSV with Date_GMT and the following columns:
  - Water temperatures: 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m depths.
  - Air_Temperature (C).
  - Pyranometer (solar radiation flux, W/m^2).
  - Wind Speed (m/s).
- All temperature measurements are in degrees Celsius; solar radiation in W/m^2; wind speed in m/s.

## Data management and usage
- Data from this buoy are used in several current scientific studies, including those by PhD students.
- Indicates ongoing research value and relevance for environmental monitoring frameworks.

## Relevance for monitoring frameworks
- Demonstrates integration of multi-parameter, long-term lake monitoring data for environmental health assessment.
- Highlights practical monitoring framework challenges: reliance on raw data, need for calibration/QA, data gaps, metadata completeness, and data governance when sharing data.