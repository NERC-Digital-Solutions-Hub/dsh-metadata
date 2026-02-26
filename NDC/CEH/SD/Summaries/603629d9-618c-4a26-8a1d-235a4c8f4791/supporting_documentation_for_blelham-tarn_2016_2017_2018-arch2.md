# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Blelham Tarn 2016 to 2018. Feuchtmayr, H., Jones, I.D., Clarke, M., Maberly, S.C. (2021)

## Overview
- Dataset from an automatic lake monitoring buoy located at Blelham Tarn, Cumbria, England.
- Covers 2016–2018 and includes meteorological and in-lake temperature measurements.

## Data Collected
- Variables and units:
  - Air temperature (degrees C)
  - Solar radiation flux (Watts per square metre)
  - Wind speed (metres per second)
  - Lake water temperature at depths: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 metres
- Measurement cadence:
  - Raw data recorded every 4 minutes
  - Hourly averages calculated from the 4-minute readings (hourly value for the hour i.e., between t-1 and t, excluding data at t-1 and including data at t)
- Time zone: Greenwich Mean Time (GMT)

## Sampling Regime and Collection Methods
- Location: Automatic lake monitoring buoy on Blelham Tarn, Cumbria.
- Instrumentation:
  - Meteorological sensors for air temperature, solar radiation (pyranometer), wind speed
  - In-lake platinum resistance thermometers at specified depths
- Data processing:
  - Hourly averages produced via an Oracle database

## Quality Control and Limitations
- Data are raw and have not yet been calibrated or quality controlled.
- Visual checks performed; obvious hardware-induced errors removed.
- Data gaps attributed to buoy maintenance or sensor/logger problems.

## Data Structure (Format)
- File format: CSV
- Columns:
  - Date GMT: date and time of measurement (GMT)
  - 0.5m to 12m: temperatures in degrees C at each listed depth
  - Air Temperature: air temperature in degrees C
  - Pyranometer: solar radiation flux in Watts per square metre
  - Wind Speed: wind speed in metres per second

## Data Management and Access
- Hourly averages are stored/produced via an Oracle database.
- Raw data are presented in a CSV structure for downstream use; calibration and quality control steps are pending.

## Funding and Acknowledgements
- Funded by Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.

## Relevance to Environmental Monitoring
- Provides standardized, time-stamped environmental and atmospheric measurements suitable for monitoring environmental health and informing policy over time.
- Data can be integrated with other datasets to enhance monitoring value; underscores the need for accessible underlying data and ongoing quality assurance.