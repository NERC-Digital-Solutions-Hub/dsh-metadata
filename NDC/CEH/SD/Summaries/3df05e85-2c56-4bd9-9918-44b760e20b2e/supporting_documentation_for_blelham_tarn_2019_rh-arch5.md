# Hourly data (relative humidity) from automatic monitoring buoy from Blelham Tarn 2012 to 2019. Feuchtmayr, H., Clarke, M., Jones, I.D., Maberly, S.C. (2022)

## Overview
- Dataset from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Relative humidity (percent) measured with a HOBO U23 Pro V2 sensor.
- Data cadence: sensor records every 4 minutes; hourly averages are produced in an Oracle database.
- Timeframe: January 2012 to December 2019.
- All timestamps provided in GMT.

## Sampling regime and collection methods
- Instrument and measurements:
  - HOBO U23 Pro V2 sensor; measurements every 4 minutes.
  - Hourly average is calculated over the previous hour, e.g., the value for 2 p.m. is the average of data from 1–2 p.m., excluding 1 p.m. data but including 2 p.m. data.
- Deployment and field handling:
  - Sensor remains on the buoy for approximately 2–3 months, then swapped.
  - After deployment, a period of low humidity (~40%) is used for at least 2 months before re-deployment.
- Time zone and data scope:
  - All data are in GMT; covers 2012–2019.

## Quality control and provenance
- Data status:
  - Raw data not calibrated or fully quality controlled.
  - Visually checked; obvious hardware-induced errors removed.
- Deployment-related exclusions:
  - Data before and after deployment removed.
  - 30–60 minutes of data post-deployment removed to allow sensor to settle.
- Data completeness:
  - Hourly values computed only when at least seven measurements were available.
  - Other gaps arise from buoy maintenance or sensor/logger problems.

## Data structure and access
- File format:
  - Comma-separated values (CSV).
- Columns:
  - Date GMT: date of measurement.
  - Hour: hour of measurement (GMT).
  - RH: relative humidity (%).
  - N: number of measurements used to compute the hourly mean.

## Temporal coverage and reuse considerations
- Coverage: January 2012 to December 2019.
- Usability considerations:
  - Data are raw; use requires calibration/processing for precise humidity analyses.
  - Provenance details (sensor type, deployment timing, data processing steps) support reproducibility but should be captured in any extended metadata.

## Funding and governance
- Data collection supported by Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.