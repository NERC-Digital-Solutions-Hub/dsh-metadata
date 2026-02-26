# Hourly data (relative humidity) from automatic monitoring buoy from Blelham Tarn 2012 to 2019

## Overview
- Location: Blelham Tarn, Cumbria, England
- Data: hourly relative humidity (%) from an automatic lake monitoring buoy
- Sensor: Onset HOBO U23 Pro V2
- Sampling: data every 4 minutes; hourly averages calculated in an Oracle database
- Time period: January 2012 to December 2019
- Time zone: GMT

## Sampling regime and collection methods
- Buoy carries meteorological instruments; data include relative humidity
- Sensor deployment cycle: sensor on buoy for ~2–3 months, then exchanged for another
- Pre-deployment conditioning: sensor left in low RH conditions (~40%) for at least 2 months prior to re-deployment
- Hourly average definition: average over the previous hour (e.g., 2 p.m. value = average of data from 1–2 p.m., excluding 1 p.m., including 2 p.m.)
- Data format: CSV with columns — Date GMT, Hour (GMT), RH (%), N (number of measurements used)

## Quality control
- Data are raw and have not been calibrated or fully quality controlled
- Visual checks performed; obvious hardware-related errors removed
- Data outside deployment windows removed; 30–60 minutes after deployment also removed to allow sensor to settle
- Hourly records dropped if fewer than seven constituent measurements available
- Gaps may occur due to buoy maintenance or sensor/logger problems

## Data structure
- File format: comma-separated values (CSV)
- Columns: Date GMT, Hour, RH (%), N
- Metadata captured within the dataset (sensor type, sampling cadence, time zone, deployment cycle)
- Data availability: 2012–2019

## Funding and provenance
- Funding: Natural Environment Research Council (NE/R016429/1)
- Programme: UK-SCaPE (delivering National Capability)