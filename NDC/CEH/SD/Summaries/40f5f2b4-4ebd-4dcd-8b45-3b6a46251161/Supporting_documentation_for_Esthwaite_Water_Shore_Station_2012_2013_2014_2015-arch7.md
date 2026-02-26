# Data from a meteorological station next to Esthwaite Water 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

## Overview
- Meteorological data collected from a station on top of a boathouse near Esthwaite Water, Cumbria, England.
- Measurements include air temperature (°C) and wind speed (m/s).
- Data captured every 4 minutes; hourly averages computed by a Campbell Scientific datalogger.
- All times are in GMT; data cover 2012–2015.
- Data provided as a CSV with: Date_GMT, Air_Temperature, Wind_Speed.

## Sampling Regime and Collection Methods
- Instruments: range of meteorological instruments at the station; data processed by a Campbell Scientific datalogger.
- Temporal aggregation: hourly averages represent the period from the previous hour, e.g., the 2 p.m. value is the average of 1–2 p.m., including data from 2 p.m. but excluding data from 1 p.m.
- Time standard: GMT; dataset spans 2012–2015.

## Quality Control
- Data are raw and have not yet been calibrated or fully quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Gaps occur due to maintenance or sensor/logger problems.

## Data Structure
- CSV file with:
  - Date_GMT: Date and time (GMT) of measurement.
  - Air_Temperature: Air temperature in degrees Celsius.
  - Wind_Speed: Wind speed in metres per second.

## Temporal Coverage
- Years: 2012, 2013, 2014, 2015.

## Relevance for GIS Specialists
- Provides time-series meteorological data that can accompany spatial analyses (e.g., environmental and hydrological GIS applications around Esthwaite Water).
- Useful for building or validating climate and weather-related map layers and models when integrated with spatial datasets.

## Considerations for GIS Use
- Data are from a single station; spatial representativeness is limited without additional stations.
- Data require calibration and full quality control before formal analysis.
- Prepare for data gaps due to maintenance or sensor issues; consider metadata on missing periods.

## Usage and Notes
- The station’s data are used in multiple current scientific studies, including PhD research, and should be cited when incorporated into analyses.