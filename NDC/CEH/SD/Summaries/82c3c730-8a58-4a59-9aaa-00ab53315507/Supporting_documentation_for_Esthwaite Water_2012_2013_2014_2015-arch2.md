# Data from automatic water monitoring buoy from Esthwaite Water 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly S.C. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy at Esthwaite Water, Cumbria, England.
- Instruments include meteorological sensors and in-lake temperature sensors.
- Variables: air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and water temperatures at multiple depths.
- Depths recorded: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 m.
- Data cadence: measurements every 4 minutes; hourly averages calculated by a Campbell Scientific datalogger.
- Timeframe: data from 2012, 2013, 2014, and 2015, all in GMT.

## Sampling regime and collection methods
- Automatic buoy located in Esthwaite Water providing continuous environmental observations.
- Measurements include air temperature, solar radiation flux, wind speed, and lake water temperatures across specified depths.

## Quality control
- Data are raw (not yet calibrated or quality controlled).
- Visual checks conducted; obvious hardware-origin errors removed.
- Data gaps due to buoy maintenance or sensor/logger problems.
- A new temperature chain was installed in August 2015.

## Data structure and format
- File format: comma-separated values (CSV).
- Columns:
  - Date_GMT: date and time of measurement (GMT).
  - Water_temperature: depths—0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m (degrees C).
  - Air_Temperature: air temperature (degrees C).
  - Pyranometer: solar radiation flux (W/m²).
  - Wind_Speed: wind speed (m/s).

## Data usage and significance
- Data are used in multiple current scientific studies, including work by PhD students.
- Represents a concrete example of standardized environmental data collection and initial QC processes.

## Relevance for environmental monitoring aims
- Demonstrates systematic data collection from automated monitoring stations.
- Illustrates preprocessing steps: raw data capture, visual QA, and documentation of data gaps.
- Provides clearly defined variables and units suitable for monitoring environmental health and informing policy performance over time.
- Highlights data stewardship practices: proper timestamping (GMT) and storage of datasets for reuse and portal upload.