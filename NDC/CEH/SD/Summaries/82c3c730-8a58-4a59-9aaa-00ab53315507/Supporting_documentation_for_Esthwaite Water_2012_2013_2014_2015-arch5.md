# Data from automatic water monitoring buoy from Esthwaite Water 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly S.C. (2017)

## Overview of data collection
- Automatic lake monitoring buoy located in Esthwaite Water, Cumbria, England.
- Instruments measure: air temperature, solar radiation flux, wind speed, and lake water temperatures.
- Water temperatures recorded at depths: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 and 12 meters.
- Data capture cadence: measurements every 4 minutes; hourly averages computed by a Campbell Scientific datalogger.
- All data are in GMT and cover years 2012, 2013, 2014, and 2015.

## Sampling regime and collection methods
- Raw data are provided; hourly averages reflect the previous hour (e.g., 2 p.m. average is from 1–2 p.m., excluding 1 p.m. data and including 2 p.m. data).
- Measurements include:
  - Water temperature at multiple depths (°C)
  - Air temperature (°C)
  - Pyranometer (solar radiation flux, W/m^2)
  - Wind speed (m/s)

## Quality control and data status
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware malfunctions removed.
- Data gaps occur due to buoy maintenance or sensor/logger problems.
- A new temperature chain was installed in August 2015.

## Data structure and metadata
- Data format: comma-separated values (CSV) file.
- Columns included:
  - Date_GMT: date and time of measurement (GMT)
  - 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m: water temperature at specified depths (°C)
  - Air_Temperature: air temperature (°C)
  - Pyranometer: solar radiation flux (W/m^2)
  - Wind_Speed: wind speed (m/s)
- Documentation notes: data are used in ongoing scientific studies, including work by PhD students.