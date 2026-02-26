# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Windermere South Basin 2016 to 2018

## Overview
- Dataset from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England (2016–2018).
- Variables collected: air temperature (°C), solar radiation flux (W/m^2), wind speed (m/s), and lake water temperature profile at depths from 1 m to 35 m.
- Data cadence: measurements every 4 minutes; hourly averages computed by an Oracle database.
- Time zone and dating: all data in GMT; dates cover 2016, 2017, and 2018.
- Data format: provided as comma separated values (CSV) with explicit column definitions and units.

## Sampling regime and collection methods
- Instrumentation: buoy-mounted meteorological sensors and platinum resistance thermometers for in-lake temperatures at multiple depths.
- Depths for temperature: 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, and 35 meters.
- Hourly value calculation: the hourly average (e.g., 2 p.m. value is the average from 1–2 p.m., excluding 1 p.m. data, including 2 p.m. data).
- All values are recorded in GMT and cover 2016–2018.

## Data structure and format
- File format: CSV with columns for Date GMT and each measurement depth (1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m), plus Air Temperature, Pyranometer (solar radiation), and Wind Speed.
- Column descriptions: each water temperature column corresponds to temperature in °C at the specified depth; air temperature in °C; pyranometer in W/m^2; wind speed in m/s.
- Data units: temperatures in degrees Celsius, solar radiation in Watts per square metre, wind speed in metres per second.

## Quality control and data quality
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Data gaps attributable to buoy maintenance or sensor/logger problems.

## Provenance, funding, and usage
- Funding: Natural Environment Research Council grant NE/R016429/1, part of the UK-SCaPE programme delivering National Capability.
- Example usage: 2021 publication on storm-induced temperature changes in lakes (Doubek et al., Limnology & Oceanography) citing this dataset.