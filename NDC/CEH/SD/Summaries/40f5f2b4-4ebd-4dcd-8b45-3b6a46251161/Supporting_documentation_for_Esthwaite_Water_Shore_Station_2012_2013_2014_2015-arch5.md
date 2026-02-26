# Data from a meteorological station next to Esthwaite Water 2012, 2013, 2014 and 2015

## Overview
- Meteorological data collected from a station on top of a boat house in Cumbria, England, next to Esthwaite Water.
- Recorded variables: Air Temperature (°C) and Wind Speed (m/s).
- Data cadence: measurements every 4 minutes; hourly averages calculated by a Campbell Scientific datalogger.
- All times are in GMT; dates span 2012–2015.
- Dataset used in multiple current scientific studies, including PhD research.

## Sampling regime and collection methods
- The hourly average for a given time is computed over the previous hour (e.g., 2 p.m. = average of 1–2 p.m., including 2 p.m., excluding 1 p.m.).
- Instruments and datalogger are Campbell Scientific equipment.

## Quality control
- Data are raw and have not yet been calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Gaps occur due to maintenance work or sensor/logger problems.

## Data structure and contents
- Format: comma separated values (CSV).
- Columns:
  - Date_GMT: Date and time of measurement (GMT).
  - Air_Temperature: Air temperature in degrees Celsius.
  - Wind_Speed: Wind speed in metres per second.
- Data from this station are used across several current scientific studies (including PhD research).

## Data governance and stewardship implications
- Status: raw data; calibration and formal QC pending.
- Metadata needs: instrument details (sensor types, heights, orientations), datalogger specifics, measurement methods, calibration status, maintenance logs, data gaps, and location coordinates.
- Access considerations: ongoing use in multiple studies; plan for data availability, versioning, and clear citation.

## Recommendations for Data Stewards
- Implement calibration and formal QC procedures; attach quality flags to measurements.
- Develop and publish comprehensive metadata: instrument specifications, datalogger model/serials, sensor placement, data processing steps, and maintenance history.
- Document data lineage and data gaps; maintain a data dictionary and data release notes.
- Clarify licensing, access permissions, and citation requirements; establish a stable data availability and update process for ongoing research use.