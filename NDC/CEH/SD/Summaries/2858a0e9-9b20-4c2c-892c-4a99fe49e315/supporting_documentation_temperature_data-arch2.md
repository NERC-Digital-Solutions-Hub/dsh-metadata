# Hourly water temperature of 28 experimental mesocosms and air temperature from July to September 2022

## Overview
- Dataset of hourly water temperature for an experimental mesocosm facility and concurrent air temperatures.
- Time period: 6 July to 30 September 2022 (GMT).
- Mesocosms: 28 active units (labels 1–32; numbers 1, 16, 17, and 32 not used in this experiment).
- Mesocosm setup: 1 m deep, 2 m diameter; about 2800 L reservoir water.
- Experimental treatments included inorganic and organic phosphorus additions and ammonium.

## What was collected
- Water temperature: hourly averages derived from 5-minute readings.
- Air temperature: measured at a weather station within the mesocosm compound (~2.7 m height).

## Measurement methods
- Temperature sensors: two platinum resistance thermometers (PRTs) per mesocosm, shaded by a plastic cover, positioned around mid-depth (~40 cm) and offset ~30 cm from the wall; data logged with a Campbell Scientific Data Logger.
- Data resolution: 5-minute measurements → hourly averages (e.g., 1 p.m. value is the average of 1:00–1:55 p.m.).
- Data quality checks:
  - If two sensors within an hour differed by less than 0.2 °C, their average was used.
  - If their difference exceeded 0.2 °C, data were checked against the overall sensor average; a drifting sensor could be ignored in those occasions, using data from the remaining sensor.
  - Totals of occasions where data came from a single sensor: 158 (sensor 4), 391 (sensor 6), 1614 (sensor 11), 8 (sensor 20), 7 (sensor 22), 14 (sensor 24), 7 (sensor 25), 17 (sensor 31).
- Data loss and issues:
  - Logging overheating affected mesocosms 18, 19, 20, 29, 30, 31 on three occasions; 5-minute data from those periods were removed; hourly data calculated excluding these periods.
  - One data logger (mesocosms 5–12) failed from 1 September 11:00 to 7 September 14:00; no data for that interval.
- Quality status: raw data; no calibration or full quality control performed yet. Visual checks conducted; obvious hardware malfunctions removed. Gaps attributed to sensor or logger problems.

## Data structure and format
- File format: comma-separated values (CSV).
- Columns:
  - Date: dd/mm/yyyy
  - Hour: 0–23
  - T2–T31: temperature in °C for mesocosms 2–31 (selected active units)
  - AirT: air temperature in °C
- Data notes:
  - Temperature data from mesocosms 2, 3, 4, 5–7, 8–14, 18–31 included (some units not used or affected by issues).
  - All times are in GMT.

## Data access, storage, and reproducibility
- Data were stored and prepared for upload to appropriate data portals as part of standard monitoring practices.

## Context and funding
- Experimental facility and dataset supported by the European Union’s Horizon 2020 programme, AQUACOSM-plus (grant No 871081).
- Related methodological reference: Feuchtmayr et al. (2019) on effects of brownification and warming in mesocosm ecosystems.

## Use considerations for analysts
- The data are raw and not calibrated; users should apply calibration/quality-control if required for precise analyses.
- Be mindful of periods with missing data due to logger issues or overheating.
- Sensor-drift handling is documented; in-hours with >0.2 °C discrepancies, single-sensor data were used after verification.
- The dataset captures environmental conditions under varying nutrient treatments, useful for examining temperature dynamics in relation to experimental manipulations.