# Sampling Regime and Collection Methods

- Overview
  - Automatic lake monitoring buoy located in Blelham Tarn, Cumbria, England.
  - Measures a range of meteorological and in-lake parameters: air temperature, solar radiation, wind speed, and lake temperature profiles.

- Measurement details
  - Data collection frequency: instrument readings every 4 minutes.
  - Data processing: hourly averages calculated by a Campbell Scientific datalogger.
  - Time reference: all data in GMT (Greenwich Mean Time).
  - Measurement period: dates from 2008, 2009, 2010, and 2011.
  - Temperature profiling: lake water temperatures at depths of 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 meters using platinum resistance thermometers.
  - Units:
    - Air temperature: degrees Celsius
    - Solar radiation: Watts per square meter
    - Wind speed: metres per second
    - Water temperature: degrees Celsius at specified depths

- Data processing and time window
  - Example of hourly averaging: value at 2 p.m. is the average of data from 1–2 p.m., excluding 1 p.m. data and including 2 p.m. data.

- Quality control
  - Data are raw, not yet calibrated or quality controlled.
  - Visual checks performed; obvious hardware-malfunction data removed.
  - Gaps attributed to buoy maintenance or sensor/logger problems.

- Data structure
  - Format: comma-separated values (CSV).
  - Columns:
    - Date_GMT: Date and time of measurement (GMT)
    - 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m: water temperature (°C) at respective depths
    - Air_Temperature: air temperature (°C)
    - Pyranometer: solar radiation flux (W/m²)
    - Wind_Speed: wind speed (m/s)

- Data use and publications
  - Dataset is used in several scientific studies, including work by PhD students.
  - Notable publications referencing the data:
    - 2014: A novel method for estimating the onset of thermal stratification in lakes from surface water measurements. Water Resources Research.
    - 2015: A comparison of the diel variability in epilimnetic temperature for five lakes in the English Lake District. Inland Waters.
    - 2016: Diel surface temperature range scales with lake size. PLoS ONE.

- Relevance for monitoring-framework authors
  - Illustrates practical data collection for environmental health monitoring, including instrument suite, deployment in a freshwater setting, and depth-resolved temperature profiling.
  - Highlights common data challenges for monitoring programs:
    - Raw data requiring calibration, QA/QC, and metadata completion.
    - Data gaps due to maintenance and sensor/logger issues.
    - The need for clear data processing rules (e.g., hourly averaging method) and consistent time references.
  - Demonstrates the importance of documenting data structure and units to facilitate reuse in policy evaluation, stakeholder reporting, and future decision-making.