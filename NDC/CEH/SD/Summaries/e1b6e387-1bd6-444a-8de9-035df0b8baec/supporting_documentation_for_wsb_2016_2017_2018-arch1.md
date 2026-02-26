# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Windermere South Basin 2016 to 2018

## Sampling Regime and Collection Methods
- Location: automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
- Instrument suite: meteorological sensors (air temperature, solar radiation flux) and in-lake temperature sensors measuring water temperature at multiple depths.
- Depths for water temperature: 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30 and 35 meters.
- Measurement cadence: data recorded every 4 minutes.
- Time aggregation: hourly averages computed in an Oracle database. The value for an hour t is the average of data from the previous hour (t-1 to t), excluding the data measured at the start of the hour (t-1) and including the data measured at the end of the hour (t).
- Units and timing: all data are in GMT (Greenwich Mean Time).

## Quality Control
- Data are raw and not yet calibrated or quality controlled.
- Visual checks performed; obvious hardware malfunction errors removed.
- Data gaps attributed to buoy maintenance or sensor/logger problems.

## Data Structure
- Format: comma separated values (CSV).
- Columns include:
  - Date GMT
  - Water temperature at 1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m
  - Air Temperature
  - Pyranometer (solar radiation flux)
  - Wind Speed

## Data Variables and Units
- Water temperatures: degrees Celsius (°C) at specified depths.
- Air temperature: degrees Celsius (°C).
- Solar radiation: Watts per square meter (W/m²).
- Wind speed: meters per second (m/s).

## Temporal and Geographic Scope
- Time period: 2016, 2017, and 2018.
- Location: Windermere South Basin, Cumbria, England, UK.

## Data Processing Details
- Hourly averages derive from data recorded every 4 minutes.
- Data have not undergone full calibration or quality control at the time of this dataset.

## Data Availability and Access
- Dataset provided as CSV with detailed column descriptions and timing rules.
- Part of broader research efforts, with recent usage indicated in published work.

## Funding
- Collected with support from Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.

## Notable Usage
- Example publications using this dataset include: Doubek, J.P. et al. (2021) on storm-induced temperature changes in lakes, referencing long-term and high-frequency data.