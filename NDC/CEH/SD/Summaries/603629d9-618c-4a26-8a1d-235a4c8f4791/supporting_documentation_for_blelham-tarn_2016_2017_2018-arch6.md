# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Blelham Tarn 2016 to 2018. Feuchtmayr, H., Jones, I.D., Clarke, M., Maberly, S.C. (2021)

## Overview
- Dataset from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Variables observed: air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and lake water temperature profiles (°C) at depths 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 m.
- Time span: 2016, 2017, and 2018.
- Measurements are taken every 4 minutes; hourly averages are provided.

## Sampling regime and collection methods
- Instruments: meteorological sensors and in-lake platinum resistance thermometers.
- Location: automatic buoy in Blelham Tarn, Cumbria.
- Data processing: hourly averages computed from the preceding 4-minute data; example rule: the value for 2 p.m. equals the average of data from 1:00–2:00 p.m., excluding 1:00 p.m. data and including 2:00 p.m. data.
- Time zone: all data are in Greenwich Mean Time (GMT).

## Quality control
- Data are raw and not yet calibrated or quality controlled.
- Visual checks performed; obvious hardware-induced errors removed.
- Gaps in data occur due to buoy maintenance or sensor/logger problems.

## Data structure and variables
- Format: comma-separated values (CSV).
- Columns:
  - Date GMT
  - 0.5m water temperature (°C)
  - 1m water temperature (°C)
  - 2m water temperature (°C)
  - 3m water temperature (°C)
  - 4m water temperature (°C)
  - 5m water temperature (°C)
  - 6m water temperature (°C)
  - 7m water temperature (°C)
  - 8m water temperature (°C)
  - 9m water temperature (°C)
  - 10m water temperature (°C)
  - 12m water temperature (°C)
  - Air Temperature (°C)
  - Pyranometer / Solar radiation (W/m²)
  - Wind Speed (m/s)

## Temporal coverage and access details
- Coverage: 2016–2018.
- All timestamps are in GMT.
- Data are provided as raw measurements with corresponding metadata on measurement depths and instruments.

## Funding and provenance
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.