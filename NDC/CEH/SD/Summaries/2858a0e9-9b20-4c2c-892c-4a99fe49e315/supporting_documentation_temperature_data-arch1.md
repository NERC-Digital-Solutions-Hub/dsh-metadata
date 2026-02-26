# Hourly water temperature of 28 experimental mesocosms and air temperature from July to September 2022

## Overview
- Dataset of hourly water temperature for mesocosms and accompanying air temperature from 6 July to 30 September 2022 (GMT).
- 28 mesocosms were used in the experiment; mesocosms 1, 16, 17, and 32 were not utilized.
- Mesocosms are 1 m deep, 2 m diameter, containing ~2800 L of reservoir water; nutrient treatments included inorganic/organic phosphorus and ammonium.
- Data focus on temperatures, with air temperature measured at a nearby weather station.

## Data collection and content
- Water temperature recorded every 5 minutes using two platinum resistance thermometers (PRTs) shaded by a plastic cover, positioned around mid-depth (~40 cm) and offset ~30 cm from the wall.
- Readings logged by a Campbell Scientific Data Logger; hourly values are the average of the corresponding 5-minute measurements (hour 1 p.m. equals 1:00–1:55 p.m. data).
- Air temperature measured at a Vaisala weather transmitter WXT520 at ~2.7 m height within the mesocosm compound.
- Data are provided in GMT and cover 6 July to 30 September 2022.
- Data are raw (not yet calibrated) but visually checked; obvious hardware errors removed.

## Data quality and processing
- Sensor and logger issues caused data gaps:
  - Overheating of loggers for mesocosms 18, 19, 20, 29, 30, 31 on three occasions; 5-minute data from these periods deleted; hourly data recalculated without this data.
  - One logger (mesocosms 5–12) failed from 1 Sept 11:00 to 7 Sept 14:00; no data in that interval.
- Sensor drift handling:
  - If hourly readings from the two sensors differed by less than 0.2 °C, the two were averaged.
  - If the difference exceeded 0.2 °C, data were checked against the overall logger average; the drifted sensor was ignored when appropriate, using data from the remaining sensor.
- Instances with data from only one sensor:
  - Counts indicating occasions with single-sensor data: 158, 391, 1614, 8, 7, 14, 7, 17 (across different mesocosms/groups).
- Data are raw and not calibrated; validation performed visually; gaps due to sensor or logger problems.

## Data structure and formats
- Data provided as a comma-separated values (CSV) file with columns:
  - Date (dd/mm/yyyy)
  - Hour (0–23)
  - T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T18, T19, T20, T21, T22, T23, T24, T25, T26, T27, T28, T29, T30, T31 (temperature in °C for each mesocosm)
  - AirT (air temperature in °C)
- Timeframe: 6 July to 30 September 2022.
- Data are organized by mesocosm numbers (2–15 and 18–31; 1, 16, 17, 32 not used).

## Context, funding, and references
- Data collection supported by the European Union's Horizon 2020 research and innovation programme (AQUACOSM-plus), grant No 871081.
- Related reference: Feuchtmayr H, Pottinger TG, Moore A, et al. (2019) on effects of brownification and warming in mesocosm experiments (Science of the Total Environment). DOI provided in the document.