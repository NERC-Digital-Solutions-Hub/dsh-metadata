# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Blelham Tarn 2016 to 2018. Feuchtmayr, H., Jones, I.D., Clarke, M., Maberly, S.C. (2021)

## Overview
- Dataset from an automatic lake monitoring buoy located at Blelham Tarn, Cumbria, England.
- Variables: air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and lake water temperature profiles.
- Water temperatures measured at depths of 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 and 12 m.
- Measurements collected every 4 minutes; hourly averages computed and stored in GMT.
- Timeframe: 2016–2018.

## Sampling regime and collection methods
- Instruments include meteorological sensors and platinum resistance thermometers for in-lake temperatures.
- Hourly averages are calculated from the 4-minute measurements; for example, 2 pm is the average of 1–2 pm data (excluding 1 pm, including 2 pm).
- Data stored in an Oracle database.

## Quality control
- Data are raw and have not undergone calibration or formal quality control.
- Visual checks performed; obvious hardware malfunctions removed.
- Gaps arise from buoy maintenance or sensor/logger problems.

## Data structure and variables
- Data provided as a comma-separated values (CSV) file with columns:
  - Date GMT
  - Temperature at depths: 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m
  - Air Temperature (°C)
  - Pyranometer (solar radiation, W/m²)
  - Wind Speed (m/s)

## Units
- Air Temperature: °C
- Water Temperature: °C
- Solar Radiation: W/m²
- Wind Speed: m/s

## Temporal coverage
- 2016, 2017, and 2018

## Provenance and funding
- Collected at Blelham Tarn with Natural Environment Research Council (NERC) grant NE/R016429/1, as part of the UK-SCaPE programme delivering National Capability.