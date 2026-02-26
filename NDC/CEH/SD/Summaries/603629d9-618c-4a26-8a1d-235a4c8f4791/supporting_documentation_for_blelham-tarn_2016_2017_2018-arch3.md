# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Blelham Tarn 2016 to 2018. Feuchtmayr, H., Jones, I.D., Clarke, M., Maberly, S.C. (2021)

- Overview
  - Data from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
  - Measured variables: air temperature, solar radiation (pyranometer), wind speed, and lake water temperature at depths of 0.5 to 12 meters.
  - Measurements are collected every 4 minutes; hourly averages are computed from the 4-minute data.
  - Times are recorded in GMT; study period covers 2016, 2017, and 2018.

- Sampling Regime and Methods
  - Buoy equipped with meteorological instruments and in-lake temperature sensors.
  - Temperature profiles captured at multiple depths (0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 12 m).
  - Hourly value at a given time is the average over the preceding hour (e.g., 2 p.m. = average 1–2 p.m., excluding 1 p.m., including 2 p.m.).

- Quality Control
  - Data are raw and not yet calibrated or fully quality controlled.
  - Visual checks conducted; obvious hardware malfunctions removed.
  - Gaps occur due to buoy maintenance or sensor/logger issues.

- Data Structure and Processing
  - Data provided as a CSV file.
  - Columns include:
    - Date GMT
    - Water temperatures at 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 m
    - Air Temperature
    - Pyranometer (solar radiation, W/m^2)
    - Wind Speed (m/s)
  - Descriptions specify measurement units and depths; data are grouped by depth and variable.

- Temporal and Spatial Coverage
  - Location: Blelham Tarn, Cumbria, England.
  - Timeframe: 2016–2018.

- Data Availability and Governance
  - Raw data with documented structure and processing rules; hourly averages derived from 4-minute data.
  - Underlying data and metadata are described; data are shareable in a transparent format (CSV) to support monitoring and evaluation efforts.

- Funding
  - Data collection supported by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.