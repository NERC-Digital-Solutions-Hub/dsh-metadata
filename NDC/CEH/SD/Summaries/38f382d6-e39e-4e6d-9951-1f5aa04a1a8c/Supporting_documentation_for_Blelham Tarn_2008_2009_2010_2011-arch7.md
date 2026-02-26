# Sampling Regime and Collection Methods

- Location: Automatic lake monitoring buoy on Blelham Tarn, Cumbria, England.
- What is measured: Air temperature (°C), solar radiation flux (Pyranometer, W/m²), wind speed (m/s), and lake water temperature at multiple depths (0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 12 m).
- Sampling frequency: Data recorded every 4 minutes by the buoy; hourly averages calculated by a Campbell Scientific datalogger.
- Time reference: All data are in Greenwich Mean Time (GMT).
- Time aggregation example: The hourly value for 2 p.m. is the average of data from 1–2 p.m., excluding 1 p.m., including 2 p.m.
- Temporal coverage: 2008, 2009, 2010, and 2011.
- Data format: Comma separated values (CSV) with a single row per hourly observation and columns for each depth temperature, air temperature, pyranometer, and wind speed.

## Quality Control

- Data are raw and not yet calibrated or quality controlled.
- Visual checks performed; obvious hardware malfunctions removed.
- Gaps attributed to buoy maintenance or sensor/logger problems.

## Data Structure and Fields

- Date_GMT: Date and time of measurement (GMT).
- Water_temperature (per depth): 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m — temperature in °C at each depth.
- Air_Temperature: Air temperature in °C.
- Pyranometer: Solar radiation flux in W/m².
- Wind_Speed: Wind speed in m/s.

## Data Use and Context

- The buoy data are used in several scientific studies, including PhD research.
- Example publications:
  - 2014: A novel method for estimating the onset of thermal stratification in lakes from surface water measurements (Water Resources Research).
  - 2015: A comparison of diel variability in epilimnetic temperatures for five lakes (Inland Waters).
  - 2016: Diel surface temperature range scales with lake size (PLOS ONE).

## GIS-Relevant Considerations

- Suitable for map-based visualization of spatial/temporal lake dynamics, including:
  - Temperature profiles by depth over time.
  - Regional comparisons of lake thermal behavior when combined with similar datasets.
- Temporal alignment:
  - Use GMT timestamps; convert to local time if needed for user-facing maps or time-enabled GIS apps.
- Data quality handling:
  - Treat raw data with attention to gaps and potential instrument issues before creating choropleth or time-series maps.
- Data integration:
  - Can be joined with other datasets (e.g., meteorological layers, lake depth models) to create enriched lake environment maps or 3D representations.