# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Blelham Tarn 2019. Feuchtmayr, H., Clarke, M., Maberly, S.C. (2022)

## Overview
- Data collected from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Variables include air temperature, solar radiation flux, wind speed, and lake water temperatures at multiple depths (0.5 m to 12 m).
- Timeframe: measurements and 2019 dates; all data reported in GMT.

## Sampling regime and collection methods
- Instruments: meteorological sensors and in-lake temperature probes using platinum resistance thermometers.
- Depths for water temperature: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 meters.
- Data cadence: measurements every 4 minutes.
- Hourly values: hourly averages calculated in an Oracle database. For example, the 2 p.m. value is the average from 1:00–2:00 p.m., excluding 1:00 p.m. data and including 2:00 p.m. data.
- Units: air temperature in °C; solar radiation flux (pyranometer) in W/m²; wind speed in m/s; water temperatures in °C.

## Data quality and limitations
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware-induced errors removed.
- Gaps attributed to buoy maintenance or sensor/logger problems.

## Data structure and contents
- File format: CSV with columns:
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
  - Pyranometer (solar radiation flux, W/m²)
  - Wind Speed (m/s)

## Context, access, and funding
- Data collection supported by Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.