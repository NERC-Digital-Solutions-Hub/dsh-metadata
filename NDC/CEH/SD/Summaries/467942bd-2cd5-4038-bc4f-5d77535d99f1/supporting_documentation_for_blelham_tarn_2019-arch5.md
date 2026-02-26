# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Blelham Tarn 2019. Feuchtmayr, H., Clarke, M., Maberly, S.C. (2022)

## Overview
- Dataset from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Variables: air temperature (°C), solar radiation flux (W/m^2), wind speed (m/s), and lake water temperature profiles.
- Water temperature measured by platinum resistance thermometers at depths: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 and 12 m.
- Instrument period: measurements every 4 minutes; hourly averages computed in an Oracle database.
- All data are in GMT; dates from 2019.
- Data collection funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCaPE.

## Sampling regime and collection methods
- Location: automatic buoy on Blelham Tarn, Cumbria.
- Instruments: meteorological sensors for air temperature and solar radiation (pyranometer) and in-lake temperature sensors (platinum resistance thermometers) at specified depths.
- Hourly average calculation: the value for a given hour (e.g., 2 p.m.) is the average of data from the preceding hour, excluding the 1 p.m. measurement and including the 2 p.m. measurement.

## Quality control
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware-malfunction errors removed.
- Gaps primarily due to buoy maintenance or sensor/logger problems.

## Data structure and format
- Format: comma-separated values (CSV).
- Columns include:
  - Date GMT
  - 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m (water temperatures at respective depths)
  - Air Temperature
  - Pyranometer (solar radiation flux)
  - Wind Speed

## Data provenance and funding
- Data collection supported by Natural Environment Research Council award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.