# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Blelham Tarn 2016 to 2018. Feuchtmayr, H., Jones, I.D., Clarke, M., Maberly, S.C. (2021)

## Overview
- Location: Blelham Tarn, Cumbria, England.
- Purpose: Data from an automatic lake monitoring buoy carrying meteorological instruments and in-lake temperature sensors.
- Variables included: air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and lake water temperature at multiple depths (0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 12 m).
- Temporal coverage: 2016–2018.
- Time reference: All data in GMT (UTC±0).
- Sampling frequency: Measurements every 4 minutes; hourly averages computed from the preceding hour with a specific rule (average of 1–2 p.m. data, excluding 1 p.m., including 2 p.m.).

## Data structure and content
- Format: Comma-separated values (CSV).
- Columns:
  - Date GMT: timestamp of measurement (GMT).
  - 0.5m … 12m: water temperature at specified depths (°C).
  - Air Temperature: air temperature (°C).
  - Pyranometer: solar radiation flux (W/m²).
  - Wind Speed: wind speed (m/s).

## Quality control and limitations
- Status: Raw data not yet calibrated or quality controlled.
- QA steps: Visual checks performed; obvious hardware-related errors removed.
- Gaps: Occur due to buoy maintenance or sensor/logger problems.
- Caution: Data may require calibration and further QA for rigorous analyses.

## Use for analysis
- Suitable for examining lake thermal structure, surface energy balance, and relationships between atmospheric drivers (air temperature, solar radiation, wind) and vertical temperature profiles.
- Potential analyses: correlations, trend detection, and development of predictive models, with attention to data gaps and calibration needs.

## Provenance and access
- Funding: Natural Environment Research Council award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.
- Source: Data collection at Blelham Tarn via an automatic buoy with attached meteorological and temperature sensors.
- Data availability: Provided as a documented CSV with described fields and units.