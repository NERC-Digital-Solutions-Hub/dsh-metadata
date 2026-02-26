# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Blelham Tarn 2016 to 2018. Feuchtmayr, H., Jones, I.D., Clarke, M., Maberly, S.C. (2021)

## Overview
- Data collected from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Variables include air temperature (°C), solar radiation (W/m²), wind speed (m/s), and lake temperature profiles at multiple depths.
- Depths recorded: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 and 12 meters.
- Time period: 2016–2018.
- Measurements spaced every 4 minutes; hourly averages computed from the 4-minute data.

## Sampling regime and collection methods
- Instruments mounted on a lake buoy with both meteorological sensors and in-lake temperature sensors.
- Hourly values represent the average of data from the preceding hour (e.g., 2 p.m. = average of 1–2 p.m., excluding 1 p.m., including 2 p.m.).
- All times reported in GMT (UTC).

## Quality control
- Data are raw and have not been calibrated or fully quality controlled.
- Visual checks performed; obvious hardware errors removed.
- Data gaps due to buoy maintenance or sensor/logger issues.

## Data structure
- Format: comma-separated values (CSV).
- Columns:
  - Date GMT: date and time of measurement.
  - 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m: water temperature (°C) at each depth.
  - Air Temperature: air temperature (°C).
  - Pyranometer: solar radiation flux (W/m²).
  - Wind Speed: wind speed (m/s).

## Temporal and spatial context
- Single buoy location (Blelham Tarn, Cumbria, England) providing point-based, time-series and depth-resolved lake temperature data.
- Data suitable for GIS workflows when combined with location context and other spatial datasets (e.g., lake bathymetry, meteorological layers, or multi-site comparisons).

## Potential GIS applications
- Visualizing spatially-resolved lake temperature profiles over time (depth vs. temperature) at a fixed location.
- Integrating with surface meteorological layers (air temperature, solar radiation, wind) for environmental modelling and risk assessment.
- Creating time-enabled map products to show temporal dynamics of lake stratification and heat content.

## Provenance and funding
- Data collection supported by Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.