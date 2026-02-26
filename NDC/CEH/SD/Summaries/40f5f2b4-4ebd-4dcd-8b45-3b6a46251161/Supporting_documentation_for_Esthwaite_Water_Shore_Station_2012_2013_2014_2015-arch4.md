# Data from a meteorological station next to Esthwaite Water 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

## Overview
- Location: Meteorological station on top of a boathouse in Cumbria, England, next to Esthwaite Water.
- Time period: Data from 2012, 2013, 2014 and 2015.
- Variables: Air temperature (degrees C) and wind speed (m/s).
- Data cadence: Measurements every 4 minutes; hourly averages calculated by a Campbell Scientific datalogger.
- Time reference: All data provided in GMT (UTC).

## Sampling regime and collection methods
- Instruments measure data every 4 minutes.
- Hourly averages are produced by the datalogger; example: the 2 p.m. value is the average from 1 p.m. to 2 p.m., including 2 p.m. but excluding 1 p.m.
- Data values are presented as hourly means based on the previous hour’s measurements.

## Quality control
- The dataset is raw and has not undergone calibration or formal quality control.
- Visual checks have been performed to remove obvious hardware-malfunction errors.
- Gaps in the data are due to maintenance work or sensor/logger problems.

## Data structure and accessibility
- Format: Comma-separated values (CSV) file.
- Columns:
  - Date_GMT: Date and time (GMT) of measurement.
  - Air_Temperature: Air temperature in degrees Celsius.
  - Wind_Speed: Wind speed in metres per second.
- Data range: Present for 2012–2015.
- Usage note: Data from this station are used in several current scientific studies, including those by PhD students.

## Context and implications for data leadership
- The data provide a high-frequency, location-specific climate time series (temperature and wind) suitable for local analyses and cross-site comparisons when combined with other datasets.
- Being raw and not yet calibrated, the dataset requires calibration, quality assessment, and potentially metadata enrichment for robust reuse.
- Data gaps and limited metadata present governance and discoverability challenges; provenance and instrument specifications are not detailed beyond basic description.

## Governance considerations and recommendations
- Document instrument specifics (sensor types, mounting height, calibration status) and QC procedures for future reuse.
- Consider adding quality flags and a metadata trail to aid discoverability and trust.
- Plan for calibration or post-collection processing if used for comparative analyses or integration with calibrated datasets.
- Maintain and disclose data provenance, update frequency, and any corrections to enhance transparency for data consumers and cross-institution collaboration.