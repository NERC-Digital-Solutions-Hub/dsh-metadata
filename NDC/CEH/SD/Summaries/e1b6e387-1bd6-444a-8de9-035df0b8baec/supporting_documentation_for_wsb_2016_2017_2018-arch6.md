# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Windermere South Basin 2016 to 2018. Feuchtmayr, H., Jones, I.D., Clarke, M., Maberly S.C. (2021)

## Overview
- Dataset from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
- Measures air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and lake temperature profiles at multiple depths (1–35 m).

## Sampling regime and collection methods
- Instruments measure data every 4 minutes.
- Hourly averages provided in the dataset; definition: average from the previous hour (excluding 1 p.m. data, including data from 2 p.m.).
- All timestamps are in GMT.
- Temperature sensors are platinum resistance thermometers; depth coverage includes 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, and 35 m.

## Quality control
- Data are raw (not calibrated or quality controlled).
- Visual checks performed; obvious hardware-related errors removed.
- Gaps attributed to buoy maintenance or sensor/logger problems.

## Data structure and format
- File format: comma-separated values (CSV).
- Key columns:
  - Date GMT: Date and time of measurement (GMT).
  - 1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m: water temperature (°C) at each depth.
  - Air Temperature: air temperature (°C).
  - Pyranometer: solar radiation flux (W/m²).
  - Wind Speed: wind speed (m/s).

## Coverage and scope
- Timeframe: 2016–2018.
- Dataset uses GMT timestamps.
- Depth coverage spans from 1 m to 35 m.

## Usage and applications
- Enables exploratory data analysis and self-serve data products (e.g., dashboards, charts) for end users.
- Can be combined with other datasets for broader analyses of lake dynamics and climate interactions.
- Users should be aware that data are raw and uncalibrated; consider additional calibration/quality control if precise measurements are required.

## Funding and provenance
- Collected at Windermere South Basin; supported by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.
- Notable publications using the dataset include: Doubek et al. (2021) on storm-induced temperature changes in lakes.