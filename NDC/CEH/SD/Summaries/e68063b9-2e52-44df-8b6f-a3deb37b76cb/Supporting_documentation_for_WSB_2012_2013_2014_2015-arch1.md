# Data from automatic water monitoring buoy from Windermere South Basin 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly S.C. (2017)

## Sampling Regime and Collection Methods
- Location and instrumentation: data collected from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England, carrying meteorological sensors and in-lake temperature probes.
- Variables recorded: air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and lake water temperatures at multiple depths (1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, 35 m).
- Temporal resolution: measurements every 4 minutes; hourly averages are provided.
- Hourly averaging method: the hourly value is the average of data from the previous hour, excluding the data measured at the start of the hour and including data from the current hour (e.g., 2 p.m. is the average from 1–2 p.m., excluding 1 p.m. data, including 2 p.m. data).
- Time reference and period: all data are in GMT; covers 2012, 2013, 2014, and 2015.
- Data collection systems: datalogger (Campbell Scientific) used until 1 June 2012; Oracle database used from 1 June 2012 onwards.

## Quality Control
- Data status: raw data not yet calibrated or fully quality controlled.
- Quality checks: visually inspected; obvious hardware-related errors removed.
- Gaps: arise from buoy maintenance or sensor/logger problems.

## Data structure
- Format: comma separated values (CSV) file.
- Columns:
  - Date_GMT: date and time in GMT of each measurement.
  - 1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m Water_temperature: temperature in °C at each depth.
  - Air_Temperature: air temperature in °C.
  - Pyranometer: solar radiation flux in W/m².
  - Wind Speed: wind speed in m/s.
- Units and naming: temperatures in °C, solar radiation in W/m², wind speed in m/s; data aligned with GMT timestamps.

## Notes on use and context
- The buoy dataset is used in ongoing scientific work, including PhD research.
- Published example using this data: Woolway, R.I., Maberly S.C., Jones, I.D., Feuchtmayr, H. (2014) “A novel method for estimating the onset of thermal stratification in lakes from surface water measurements,” Water Resources Research, 50(6), 5131-5140.
- Relevance for analysts: suitable for exploring correlations between surface meteorology and vertical thermal structure, developing or validating stratification indicators, and informing models of lake temperature dynamics.
- Considerations for analysis: raw data require calibration and quality checks; potential data gaps due to maintenance or sensor issues; single buoy source may limit spatial representativeness.