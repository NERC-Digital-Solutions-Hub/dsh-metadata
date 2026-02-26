# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Blelham Tarn 2019. Feuchtmayr, H., Clarke, M., Maberly, S.C. (2022)

## Overview
- Dataset collected from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Measured variables: air temperature (°C), solar radiation flux (W/m^2), wind speed (m/s), and lake water temperatures at multiple depths.
- Lake temperatures measured with platinum resistance thermometers at depths: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 m.
- Data frequency: instruments record every 4 minutes; hourly averages are computed by an Oracle database.
- Timeframe and time zone: dates from 2019; times are in GMT.

## Data content and units
- Data format: comma separated values (CSV).
- Columns:
  - Date GMT
  - 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m (lake temperatures in °C)
  - Air Temperature (°C)
  - Pyranometer (Solar radiation in W/m^2)
  - Wind Speed (m/s)

## Data quality and quality control
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Gaps attributed to buoy maintenance or sensor/logger problems.

## Data structure details
- Column mappings:
  - Date GMT: timestamp of measurement
  - 0.5m to 12m: water temperatures at specified depths (°C)
  - Air Temperature: air temperature (°C)
  - Pyranometer: solar radiation (W/m^2)
  - Wind Speed: wind speed (m/s)
- Hourly averaging rule: value for a given hour represents the average from the previous hour (e.g., 2 p.m. is the average from 1–2 p.m.; excludes 1 p.m., includes 2 p.m.).

## Usage notes for GIS
- Suitable for mapping and visualizing spatial-temporal patterns of lake temperature at multiple depths, surface meteorology, and energy balance indicators.
- Can be joined with other spatial datasets (lake boundaries, catchment features, meteorological layers) for enriched analyses.
- Given the raw nature and lack of calibration, consider additional QA/calibration for precision-dependent analyses.

## Limitations and caveats
- Not calibrated or quality-controlled; data gaps exist due to maintenance or sensor issues.
- Use with caution for high-precision applications; apply calibration/validation as needed.

## Data provenance and funding
- Collected at Blelham Tarn.
- Funding: Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.