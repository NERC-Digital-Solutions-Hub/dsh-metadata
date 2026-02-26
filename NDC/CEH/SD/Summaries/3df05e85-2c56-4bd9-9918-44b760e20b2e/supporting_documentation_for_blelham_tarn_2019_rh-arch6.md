# Hourly data (relative humidity) from automatic monitoring buoy from Blelham Tarn 2012 to 2019. Feuchtmayr, H., Clarke, M., Jones, I.D., Maberly, S.C. (2022)

## Overview
- Dataset of hourly relative humidity (RH %) from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Instruments: Onset HOBO U23 Pro V2 sensor; data recorded every 4 minutes.
- Hourly averages computed by an Oracle database; GMT timestamps.
- Coverage: January 2012 – December 2019.

## Sampling regime and collection methods
- Sensor deployed on buoy with a range of meteorological instruments; hourly RH values derived from 4-minute data.
- Deployment cycle: sensor stays on buoy for ~2–3 months, then replaced with another HOBO sensor.
- Post-deployment conditioning: sensor left in low RH conditions (~40%) for at least 2 months before re-deployment.

## Quality control and data processing
- Data are raw (not calibrated or quality controlled) but visually checked; obvious hardware-related errors removed.
- Data immediately before and after deployment excluded; 30–60 minutes after deployment also removed to allow environmental settling.
- Hourly values omitted if fewer than seven measurements were available to compute the mean.
- Remaining data gaps attributed to buoy maintenance or sensor/logger problems.

## Data structure and access
- Format: comma-separated values (CSV).
- Columns:
  - Date GMT: Date of measurement.
  - Hour GMT: Hour of measurement.
  - RH: Relative humidity (%) for the hour.
  - N: Number of measurements used to calculate the hourly mean.

## Calculation detail
- Hourly averages reflect the previous hour, calculated as: for hour H, the average of data from H-1 to H, excluding data at the start of the previous hour (e.g., value at 2 p.m. = average of 1–2 p.m., excluding 1 p.m., including 2 p.m.).

## Coverage, limitations, and caveats
- Data are raw and not calibrated; users may require calibration for certain analyses.
- Gaps exist due to sensor replacements, maintenance, and logger issues.
- Some periods may be missing or have limited measurements due to deployment/removal cycles.

## Funding and provenance
- Supported by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.