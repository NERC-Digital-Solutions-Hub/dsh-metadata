# Data from automatic water monitoring buoy from Windermere South Basin 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly S.C. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
- Temporal coverage: 2012–2015; includes meteorological data and multi-depth lake temperatures.
- Data used in ongoing scientific studies and referenced in a publication by Woolway et al. (2014).

## Sampling regime and collection methods
- Buoy instruments measure:
  - Air temperature (°C)
  - Solar radiation flux (W/m^2)
  - Wind speed (m/s)
  - Lake water temperatures at depths: 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, 35 m
- Data cadence: every 4 minutes.
- Hourly averages:
  - Calculated by a Campbell Scientific datalogger (until 1 June 2012) and an Oracle database (from 1 June 2012 onwards).
  - Definition: The value for 2 p.m. is the average of data between 1 and 2 p.m., excluding 1 p.m. data and including 2 p.m. data.
- Time standard: all data in GMT (UTC).
- Dates covered: 2012, 2013, 2014, 2015.

## Quality control and data integrity
- Data are raw (not calibrated or quality controlled yet).
- Visually checked; obvious hardware malfunctions removed.
- Gaps attributed to buoy maintenance or sensor/logger problems.

## Data structure and fields
- Format: comma-separated values (CSV).
- Key columns:
  - Date_GMT (Date and time in GMT)
  - Water_temperature at depths: 1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m
  - Air_Temperature (°C)
  - Pyranometer (Solar radiation flux in W/m^2)
  - Wind Speed (m/s)

## Usage and references
- Data have been used in current scientific studies and by PhD students.
- Reference publication: Woolway, R.I., Maberly S.C., Jones, I.D., Feuchtmayr, H. (2014) “A novel method for estimating the onset of thermal stratification in lakes from surface water measurements,” Water Resources Research, 50(6), 5131-5140.