# Data from automatic water monitoring buoy from Windermere South Basin 2012, 2013, 2014 and 2015

## Overview
- Automatic lake monitoring buoy located in Windermere South Basin, Cumbria, England.
- Instruments include meteorological sensors and in-lake temperature sensors.
- Recorded variables: air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and lake water temperatures at multiple depths.
- Water temperatures measured at 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, and 35 meters depth.
- Data cover years 2012–2015 and are provided in Greenwich Mean Time (GMT).
- Measurements occur every 4 minutes; hourly averages are calculated from the 4-minute data.

## Sampling regime and collection methods
- Depth-resolved water temperatures are captured by platinum resistance thermometers.
- Hourly averages are computed by a Campbell Scientific datalogger (until 1 June 2012) and by an Oracle database (from 1 June 2012 onwards).
- The hourly value for a given hour is the average of the data from the previous hour, excluding data measured at the start of the hour and including data at the end of the hour.
- Data collection and storage transition:
  - Before 1 June 2012: Campbell Scientific datalogger.
  - From 1 June 2012 onwards: Oracle database.

## Data quality and limitations
- The dataset comprises raw data that have not yet been calibrated or quality controlled.
- Visual checks have been performed and obvious hardware malfunctions have been removed.
- Data gaps are due to buoy maintenance or sensor/logger problems.

## Data structure and format
- Provided as a comma separated values (CSV) file.
- Columns include:
  - Date_GMT: date and time of measurement (GMT).
  - Water_temperature at depths: 1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m.
  - Air_Temperature: air temperature in °C.
  - Pyranometer: solar radiation flux in W/m².
  - Wind Speed: wind speed in m/s.

## Usage and publications
- The buoy data are used in several ongoing scientific studies, including work by PhD students.
- Example publication utilizing the dataset:
  - Woolway, R.I., Maberly S.C., Jones, I.D., Feuchtmayr, H. (2014) A novel method for estimating the onset of thermal stratification in lakes from surface water measurements. Water Resources Research, 50(6), 5131-5140.

## Accessibility and integration
- The dataset is stored with the respective data collection systems (datalogger and Oracle DB) and is suitable for integration with other environmental datasets (e.g., meteorological observations) to enhance analyses of lake thermal dynamics and environmental health indicators.
- The data description emphasizes reproducibility and applicability for monitoring environmental health over time, supporting standardized outputs and potential data sharing.