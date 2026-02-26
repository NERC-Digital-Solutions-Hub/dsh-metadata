# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Blelham Tarn 2019. Feuchtmayr, H., Clarke, M., Maberly, S.C. (2022)

## Overview
- Dataset from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Measurements include air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and lake water temperatures at multiple depths (0.5–12 m).
- Depths covered: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 m.
- Water temperature sensors are platinum resistance thermometers.
- All data timestamps are in GMT; dates start from 2019.
- Data are raw (not yet calibrated or fully quality-controlled).

## Sampling regime and collection methods
- Instrumentation: automatic lake monitoring buoy with meteorological sensors and in-lake temperature sensors.
- Data collection cadence: measurements every 4 minutes.
- Data processing: hourly averages computed by an Oracle database.
  - Example: the 2 p.m. value is the average from 1:00–2:00 p.m. (excluding 1 p.m. data, including 2 p.m. data).
- Location and purpose: supports environmental monitoring of lake conditions.

## Quality control
- Data are raw and have not undergone full calibration or formal quality assurance.
- Visual checks performed; obvious hardware malfunctions removed.
- Gaps in data primarily due to buoy maintenance or sensor/logger issues.

## Data structure and variables
- File format: comma-separated values (CSV).
- Columns and descriptions:
  - Date GMT: date/time of measurement (GMT).
  - 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m: water temperature (°C) at each depth.
  - Air Temperature: air temperature (°C).
  - Pyranometer: solar radiation flux (W/m²).
  - Wind Speed: wind speed (m/s).
- Metadata included via column descriptions to clarify units and depths.

## Funding and context
- Funding: Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.