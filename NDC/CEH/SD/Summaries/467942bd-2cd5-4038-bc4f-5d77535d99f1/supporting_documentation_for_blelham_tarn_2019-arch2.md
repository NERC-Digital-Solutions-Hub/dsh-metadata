# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Blelham Tarn 2019. Feuchtmayr, H., Clarke, M., Maberly, S.C. (2022)

## Overview
- Dataset from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Measurements include air temperature, solar radiation, wind speed, and in-lake water temperature profiles.
- Covers temperatures at multiple depths (0.5–12 m) using platinum resistance thermometers.
- Data collected in 4-minute intervals with hourly averages calculated and stored in an Oracle database.
- All data are provided in GMT and date notes begin in 2019.

## Sampling regime and collection methods
- Instruments mounted on a buoy deliver:
  - Air temperature (°C)
  - Solar radiation flux (W/m²) from a pyranometer
  - Wind speed (m/s)
  - In-lake water temperatures at depths of 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 m (°C) using platinum resistance thermometers
- Measurements are captured every 4 minutes.
- Hourly values are averages of the 4-minute data within the preceding hour, calculated by an Oracle database.

## Quality control
- Data are raw and have not been fully calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Gaps arise from buoy maintenance or sensor/logger issues.

## Data structure
- Provided as a comma-separated values (CSV) file.
- Columns include:
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
  - Pyranometer (solar radiation, W/m²)
  - Wind Speed (m/s)

## Coverage and context
- Location: Blelham Tarn, Cumbria, England.
- Temporal coverage begins in 2019; ongoing data collection indicated.
- Data are raw and may be augmented with calibration/QA in future iterations.

## Funding and provenance
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.