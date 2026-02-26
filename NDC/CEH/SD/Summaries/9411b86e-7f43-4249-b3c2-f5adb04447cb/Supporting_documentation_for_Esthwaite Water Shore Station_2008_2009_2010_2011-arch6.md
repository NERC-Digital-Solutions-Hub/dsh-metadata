# Data from a meteorological station next to Esthwaite Water 2008, 2009, 2010 and 2011

## Overview
- Location: meteorological station on top of a boathouse in Cumbria, England, next to Esthwaite Water.
- Period: data from 2008, 2009, 2010 and 2011.
- Variables: air temperature (degrees C) and wind speed (m/s).
- Data cadence: measurements every 4 minutes; hourly averages calculated by a Campbell Scientific datalogger.
- Timezone and format: data are in GMT (UTC); dates span 2008–2011.

## Sampling regime and collection methods
- Instrumentation: range of meteorological instruments; this dataset includes Air_Temperature and Wind_Speed.
- Hourly averaging rule: the hourly average for a given hour (e.g., 2 p.m.) is the average of data from the previous hour, excluding the data measured at the start of that hour and including data measured at the end of the hour (e.g., 2 p.m. includes data up to 2 p.m.).
- Data recording device: Campbell Scientific datalogger.

## Quality control
- Data are raw and not yet calibrated or quality controlled.
- Visual checks have been performed; obvious hardware-related errors removed.
- Gaps in data are due to maintenance or sensor/logger problems.

## Data structure
- File format: comma separated values (CSV).
- Columns:
  - Date_GMT: Date and time (GMT) of measurement.
  - Air_Temperature: Air temperature in degrees C.
  - Wind_Speed: Wind speed in metres per second.

## Usage and context
- The dataset is used in several current scientific studies, including those involving PhD students.