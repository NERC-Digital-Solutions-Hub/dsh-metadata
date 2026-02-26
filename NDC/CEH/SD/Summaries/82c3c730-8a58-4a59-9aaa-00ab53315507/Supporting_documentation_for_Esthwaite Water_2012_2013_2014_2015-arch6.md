# Data from automatic water monitoring buoy from Esthwaite Water 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly S.C. (2017)

- Overview
  - Data come from an automatic lake monitoring buoy on Esthwaite Water, Cumbria, England.
  - Variables include air temperature (°C), solar radiation flux (W/m^2), wind speed (m/s), and lake water temperatures at multiple depths.

- Sampling regime and data collected
  - Measurements recorded every 4 minutes; hourly averages calculated by a Campbell Scientific datalogger.
  - Variables and depths:
    - Water temperature at 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 m depths.
    - Air temperature (°C).
    - Pyranometer (solar radiation flux in W/m^2).
    - Wind speed (m/s).
  - Dates cover 2012, 2013, 2014, and 2015; all times provided in GMT.

- Data quality and QC
  - The dataset is raw data and has not been calibrated or quality controlled.
  - Visual checks performed; obvious hardware-related errors removed.
  - Data gaps attributed to buoy maintenance or sensor/logger problems.
  - A new temperature chain was installed in August 2015.

- Data structure and units
  - Provided as a comma-separated values (CSV) file.
  - Columns include:
    - Date_GMT: date and time (GMT) of measurement.
    - Water_temperature at 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m (°C).
    - Air_Temperature (°C).
    - Pyranometer (Solar radiation flux, W/m^2).
    - Wind_Speed (m/s).
  - Note: 11 m depth is not included; data are provided for the specified depths.

- Usage and context
  - Data are being used in several current scientific studies, including work by PhD students.
  - The hourly averages are derived from 4-minute data, with precise averaging rule noted (e.g., value for 2 p.m. is the average of 2–3 p.m. excluding 2 p.m., including 3 p.m.). All times are in GMT.

- Practical considerations for analysis
  - Treat as raw data requiring calibration/quality control before formal analyses.
  - Useful for multi-depth temperature profiling, surface energy balance studies, and environmental monitoring research.
  - Can be combined with other datasets for broader analyses on lake dynamics and meteorological influences.