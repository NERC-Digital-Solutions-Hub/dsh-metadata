# Data from automatic water monitoring buoy from Bassenthwaite Lake 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy located in Bassenthwaite Lake, Cumbria, England.
- Temporal coverage: 2012–2015.
- Measured variables: air temperature, solar radiation, wind speed, and lake water temperature at depths of 1, 2, 3, 4, 5, 6, 8, 10, 12, 14, 16 and 18 meters.
- Data types: raw 4-minute interval data, with hourly averages calculated and reported in GMT.

## Sampling regime and collection methods
- Measurements taken every 4 minutes by buoy-mounted instruments.
- Hourly averages computed from 4-minute data:
  - Until 24 January 2013: via Campbell Scientific datalogger.
  - From 24 January 2013 onwards: via Oracle database.
- Units:
  - Air temperature: degrees Celsius (°C)
  - Solar radiation: Watts per square metre (W/m²)
  - Wind speed: metres per second (m/s)
  - Water temperature: degrees Celsius (°C) at specified depths
- All timestamps are in Greenwich Mean Time (GMT).

## Quality control
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware misbehaviour removed.
- Data gaps due to buoy maintenance or sensor/logger problems.
- Specific data limitation: temperature profile data missing after January 2014 due to loss of the temperature chain.

## Data structure
- Format: comma-separated values (CSV).
- Columns:
  - Date_GMT: Date and time (GMT) of measurement.
  - Water_temperature: 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m (temperature in °C at each depth).
  - Air_Temperature: Air temperature in °C.
  - Pyranometer: Solar radiation flux in W/m².
  - Wind Speed: Wind speed in m/s.

## Data availability and usage
- The buoy data have been used in multiple studies, including PhD research.
- Related publication: Woolway, R.I., Maberly, S.C., Jones, I.D., Feuchtmayr, H. (2014) on estimating the onset of thermal stratification in lakes from surface water measurements (Water Resources Research).

## GIS considerations
- Suitable for time-enabled map visualisations and depth-resolved lake temperature analyses at Bassenthwaite Lake.
- Primarily a single-point temporal dataset; depth-resolved data enable 3D visualization or cross-sections when combined with bathymetry.
- Be mindful of data gaps and the absence of calibration/QA data when interpreting maps or performing analyses.
- GMT timestamps ensure consistency with other geospatial datasets; consider converting to local time if needed for policy or stakeholder presentations.

## Limitations
- No calibrated/quality-controlled data provided.
- Temperature profile data not available after January 2014.
- Data gaps exist due to maintenance and sensor/logger issues.