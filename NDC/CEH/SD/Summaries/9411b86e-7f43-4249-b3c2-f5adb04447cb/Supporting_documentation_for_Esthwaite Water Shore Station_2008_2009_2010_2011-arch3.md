# Data from a meteorological station next to Esthwaite Water 2008, 2009, 2010 and 2011.

## Overview
- Data collected from a meteorological station on top of a boathouse in Cumbria, England, next to Esthwaite Water.
- Measured variables: air temperature (°C) and wind speed (m/s).
- Measurements occur every 4 minutes; hourly averages calculated by a Campbell Scientific datalogger.
- Time reference: GMT; sampled years: 2008, 2009, 2010, 2011.

## Sampling regime and collection methods
- Instruments provide continuous 4-minute interval data.
- Hourly averages are computed from the previous hour, using the value for 2 p.m. as the average of 1–2 p.m. (excluding 1 p.m., including 2 p.m.).
- Data are presented as raw observations collected from the station.

## Quality control and data status
- The dataset is raw and has not been calibrated or quality controlled yet.
- Visual checks performed and obvious hardware malfunctions removed.
- Gaps in data are due to maintenance work or sensor/logger problems.

## Data structure and format
- Data stored in a CSV file with columns:
  - Date_GMT: Date and time (GMT) of measurement.
  - Air_Temperature: Air temperature in degrees Celsius.
  - Wind_Speed: Wind speed in metres per second.
- Units clearly specified; timestamped in GMT.
- Note: Data from this station are used in several ongoing scientific studies, including by PhD students.

## Context and usage
- Represents a time series suitable for environmental monitoring analyses.
- Useful for evaluating environmental health measures and informing future decisions, with emphasis on data provenance and quality considerations.

## Relevance for monitoring frameworks (for the archetype)
- Highlights the need for robust metadata, provenance, and quality assurance before integration into monitoring frameworks.
- Illustrates common barriers: raw data needing calibration, potential data gaps, and reliance on data from a single station.
- Underlines importance of data governance: clear documentation of collection methods, data transformations, and access/sharing policies to enable reuse and avoid duplication.