# Hourly data (relative humidity) from automatic monitoring buoy from Blelham Tarn 2012 to 2019. Feuchtmayr, H., Clarke, M., Jones, I.D., Maberly, S.C. (2022)

## Overview
- Dataset from an automatic lake monitoring buoy located in Blelham Tarn, Cumbria, England.
- Relative humidity (% RH) measured with an Onset HOBO U23 Pro V2 sensor.
- Data collected every 4 minutes; hourly averages calculated by an Oracle database.
- Hourly value definitions: the hour is the average of the previous hour (e.g., 2 p.m. is the average of 1–2 p.m., excluding 1 p.m. data, including 2 p.m. data).
- Temporal coverage: January 2012 to December 2019.
- All times are in GMT (UTC).

## Sampling regime and collection methods
- Sensor deployed on the buoy; typically on-site for ~2–3 months before replacement with another HOBO sensor.
- After deployment, the sensor is left in low humidity conditions (around 40%) for at least 2 months prior to redeployment.

## Quality control and data processing
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware errors removed.
- Data before and after deployment removed, as well as 30–60 minutes after deployment to allow sensor stabilization.
- Hourly values removed if fewer than seven measurements were available to compute the mean; other data gaps due to buoy maintenance or sensor/logger problems.

## Data structure and access
- Provided as a comma-separated values (CSV) file.
- Columns:
  - Date GMT: Date of measurement
  - Hour: Hour of measurement (GMT)
  - RH: Relative humidity (%)
  - N: Number of measurements used to calculate the hourly mean

## Temporal scope and context
- Sensor deployment cycle: ~2–3 months per sensor, with re-deployment following removal.
- Data are raw, with no calibration or formal QC applied within this dataset.

## Data management and use
- Data are stored with clear provenance (buoy location, sensor type, calculation method) and formatted for standard use in environmental monitoring.
- Funding and project context noted (see below) for data collection and program goals.

## Funding
- Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.