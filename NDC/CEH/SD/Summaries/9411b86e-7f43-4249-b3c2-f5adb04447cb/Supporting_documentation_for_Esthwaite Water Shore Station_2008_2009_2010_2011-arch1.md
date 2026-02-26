# Data from a meteorological station next to Esthwaite Water 2008, 2009, 2010 and 2011.

## Overview
- Data collected from a meteorological station atop a boathouse in Cumbria, England, next to Esthwaite Water.
- Variables: air temperature (°C) and wind speed (m/s).
- Data cadence: measurements every 4 minutes; hourly averages computed by a Campbell Scientific datalogger.
- Time zone: all data in GMT; date range covers 2008–2011.
- Data are raw (not yet calibrated or quality controlled) but visually checked; gaps due to maintenance or sensor/logger issues.
- The dataset is used in multiple current scientific studies, including PhD research.

## Sampling regime and collection methods
- Station location: top of a boathouse near Esthwaite Water.
- Instruments measure air temperature and wind speed.
- Measurements are taken every 4 minutes.
- Hourly averages are calculated as the average over the preceding hour, using data from the current hour up to and including the current measurement (example: the value for 2 p.m. is the average of data between 1 and 2 p.m., excluding 1 p.m. and including 2 p.m.).
- Data are provided in GMT.

## Quality control
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware malfunctions removed.
- Gaps arise from maintenance activities or sensor/logger problems.

## Data structure
- Format: comma separated values (CSV).
- Columns:
  - Date_GMT: Date and time of measurement (GMT).
  - Air_Temperature: Air temperature in degrees C.
  - Wind_Speed: Wind speed in metres per second.

## Usage and notes
- Used in several current scientific studies, including PhD research.
- Users should account for lack of calibration and potential data gaps when performing analyses.
- Data can be leveraged for correlational studies and modeling, with attention to the averaging method and time zone.