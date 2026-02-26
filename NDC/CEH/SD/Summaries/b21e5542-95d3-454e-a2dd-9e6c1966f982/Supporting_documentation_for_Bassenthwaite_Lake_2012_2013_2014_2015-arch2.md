# Data from automatic water monitoring buoy from Bassenthwaite Lake 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy at Bassenthwaite Lake, Cumbria, England.
- Measurements include air temperature, solar radiation, wind speed, and lake water temperatures at multiple depths (1, 2, 3, 4, 5, 6, 8, 10, 12, 14, 16, 18 m).
- Data collection period: 2012–2015; times are in GMT.

## Sampling Regime and Collection Methods
- Instruments: meteorological sensors and platinum resistance thermometers for lake temperatures.
- Depths for water temperature: 1–6 m, 8, 10, 12, 14, 16, 18 m.
- Data frequency: measurements every 4 minutes; hourly averages computed automatically.
- Data storage: Campbell Scientific datalogger (until 24 Jan 2013) and Oracle database (from 24 Jan 2013 onwards).
- Hourly averaging method: average of data from the previous hour up to the current hour, excluding the previous hour’s data and including the current hour’s data.
- Units: water temperatures (°C); air temperature (°C); solar radiation (W/m²); wind speed (m/s).
- All data timestamps are GMT.

## Quality Control
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Gaps due to buoy maintenance or sensor/logger problems.
- Temperature profile data missing from January 2014 onward due to loss of the temperature chain.

## Data Structure
- Format: comma separated values (CSV).
- Columns:
  - Date_GMT: date and time of measurement (GMT).
  - 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m: water temperature at respective depths (°C).
  - Air_Temperature: air temperature (°C).
  - Pyranometer: solar radiation flux (W/m²).
  - Wind Speed: wind speed (m/s).

## Data Use and References
- The buoy data are used in multiple ongoing scientific studies, including PhD research.
- Notable publication leveraging the data: Woolway, R.I., Maberly, S.C., Jones, I.D., Feuchtmayr, H. (2014) “A novel method for estimating the onset of thermal stratification in lakes from surface water measurements,” Water Resources Research.
- Dataset supports standardised environmental monitoring and can be integrated with other datasets; raw data suitable for calibration and QA workflows.