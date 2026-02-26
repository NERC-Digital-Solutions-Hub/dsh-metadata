# Supporting information for automatic water monitoring buoy data from Windermere South Basin 2008-2011.

## Data availability and citation
- Data come from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
- Collected data include meteorological instruments and in-lake temperature sensors.
- Source: Jones, I.; Feuchtmayr, H. (2017). south basin, 2008 to 2011. NERC Environmental Information Data Centre. DOI: https://doi.org/10.5285/bd37710e-6a53-49f0-9a07-6973408a3342

## Sampling regime and collection methods
- Location: automatic buoy in Windermere South Basin.
- Measured variables:
  - Air temperature (°C)
  - Solar radiation flux (Pyranometer, W/m²)
  - Wind speed (m/s)
  - Lake water temperatures at depths: 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, and 35 meters (°C)
- Measurement cadence: every 4 minutes; hourly averages computed by a Campbell Scientific datalogger (hourly value is the average of the interval, excluding the start of the hour, including the end).
- Time reference: GMT; dates 2008–2011.

## Quality control
- Data are raw (not calibrated or fully quality controlled).
- Visually checked; obvious hardware-related errors removed.
- Gap: ~10 days in 2010 due to logger/telemetry change.
- Other gaps due to buoy maintenance or sensor/logger problems.

## Data structure
- Format: comma-separated values (CSV).
- Columns:
  - Date GMT
  - 1m (temperature, °C)
  - 2m (temperature, °C)
  - 4m (temperature, °C)
  - 7m (temperature, °C)
  - 10m (temperature, °C)
  - 13m (temperature, °C)
  - 16m (temperature, °C)
  - 19m (temperature, °C)
  - 22m (temperature, °C)
  - 25m (temperature, °C)
  - 30m (temperature, °C)
  - 35m (temperature, °C)
  - Air Temperature (°C)
  - Pyranometer (solar radiation flux, W/m²)
  - Wind Speed (m/s)

## Additional information
- The buoy data are used in multiple scientific studies, including PhD research.
- Notable publications using the dataset include:
  - Woolway et al. (2014) on estimating the onset of thermal stratification from surface measurements (Water Resources Research).
  - Woolway et al. (2015) on diel variability in epilimnetic temperature (Inland Waters).
  - Woolway et al. (2016) on diel surface temperature range and lake size (PLoS ONE).