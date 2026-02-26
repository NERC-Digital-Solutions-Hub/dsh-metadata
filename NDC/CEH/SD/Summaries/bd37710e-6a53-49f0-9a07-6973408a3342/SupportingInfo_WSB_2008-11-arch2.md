# Supporting information for automatic water monitoring buoy data from Windermere South Basin 2008-2011.

## Overview
- Dataset from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
- Instruments include meteorological sensors and in-lake temperature sensors.
- Measured variables: air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and lake water temperatures at depths of 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, and 35 m (°C).
- Data cadence: measurements every 4 minutes; hourly averages calculated by a Campbell Scientific datalogger.
- Times are in GMT; data cover 2008–2011.

## Data content and units
- Water temperatures: degrees Celsius at each specified depth.
- Air temperature: degrees Celsius.
- Solar radiation: Watts per square metre.
- Wind speed: metres per second.

## Quality control and limitations
- Data are raw and have not been calibrated or fully quality controlled.
- Visually checked; obvious hardware errors removed.
- Approximately a 10-day data gap in 2010 due to logger/telemetry changes.
- Other gaps result from buoy maintenance or sensor/logger problems.

## Data structure
- Format: comma-separated values (CSV).
- Columns:
  - Date GMT
  - 1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m (lake temperature at each depth, °C)
  - Air Temperature (°C)
  - Pyranometer (Solar radiation, W/m²)
  - Wind Speed (m/s)

## Availability and use
- Data availability: NERC Environmental Information Data Centre; DOI: 10.5285/bd37710e-6a53-49f0-9a07-6973408a3342.
- Used in multiple studies and publications:
  - Woolway et al. 2014, Water Resources Research
  - Woolway et al. 2015, Inland Waters
  - Woolway et al. 2016, PLoS ONE
- Demonstrates potential for data reuse in methods development (e.g., onset of thermal stratification, diel temperature variability) and broader environmental analyses.

## Additional information
- Dataset has supported ongoing scientific work, including PhD research.
- Indicates value of long-term, high-frequency buoy data for environmental monitoring and methodological development.