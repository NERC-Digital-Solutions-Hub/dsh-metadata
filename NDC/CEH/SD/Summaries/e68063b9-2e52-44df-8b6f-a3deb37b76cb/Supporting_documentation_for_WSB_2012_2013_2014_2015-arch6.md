# Data from automatic water monitoring buoy from Windermere South Basin 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly S.C. (2017)

- Overview
  - Dataset from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
  - Timeframe: 2012–2015.
  - Measurements: air temperature, solar radiation, wind speed, and lake water temperatures at multiple depths (1 m to 35 m).
  - Data cadence: instrument readings every 4 minutes; hourly averages provided in GMT.

- Sampling regime and collection methods
  - Instruments measure: air temperature (°C), solar radiation flux (W/m^2), wind speed (m/s).
  - Lake temperatures measured with platinum resistance thermometers at depths: 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, 35 m.
  - Hourly averaging method: the value for a given hour (e.g., 2 p.m.) is the average of data from the previous hour up to and including the current hour (2 p.m.), with the 1 p.m. data excluded.
  - Data collection hardware: Campbell Scientific datalogger used until 1 June 2012; Oracle database used from 1 June 2012 onwards.
  - All timestamps are in Greenwich Mean Time (GMT).

- Quality control
  - The dataset is raw and has not been calibrated or quality controlled.
  - Visual checks performed; obvious hardware-related errors removed.
  - Gaps arise from buoy maintenance or sensor/logger problems.

- Data structure
  - Provided as a comma-separated values (CSV) file.
  - Columns include: Date_GMT; Water_temperature at 1 m, 2 m, 4 m, 7 m, 10 m, 13 m, 16 m, 19 m, 22 m, 25 m, 30 m, 35 m; Air_Temperature; Pyranometer (solar radiation); Wind Speed.

- Data provenance and usage
  - Used in multiple current scientific studies, including work by PhD students.
  - Associated publication: Woolway, R.I., Maberly S.C., Jones, I.D., Feuchtmayr, H. (2014) "A novel method for estimating the onset of thermal stratification in lakes from surface water measurements," Water Resources Research, 50(6), 5131-5140.
  - Potential uses: analysis of lake thermal structure, stratification timing, and relationships between atmospheric conditions and lake temperatures; development of data products or dashboards for exploration and dissemination.