# Hourly water temperature of 16 experimental mesocosms and air temperature from April to November 2023

## Overview
- Dataset of hourly water temperature from 16 mesocosms (numbers 5–12 and 21–28) and corresponding air temperature.
- Mesocosms are 1 m deep, 2 m diameter, located in NW England; water sourced from Windermere (~2800 L).
- Water temperature measured every 5 minutes using two platinum resistance thermometers (PRTs) per mesocosm, shaded and placed around mid-depth (≈40 cm), logged by a Campbell Scientific Data Logger.
- Air temperature measured at a Vaisala WXT520 weather transmitter, at ~2.7 m height, from 21 Apr to 7 Nov 2023. Air sensor stopped 17 Aug–6 Sep 2023 (no air data during this period).
- Experiment included different nutrient ratio treatments (phosphate and nitrate).
- Data are raw (not calibrated/fully quality controlled); visual checks performed and obvious hardware errors removed. Gaps due to sensor or logger problems.

## Data content and structure
- Data cover 16 mesocosms (5–12, 21–28) with hourly averages derived from 5-minute measurements.
- Time is provided in GMT; hourly value for a given hour is the average of data from that hour (e.g., 1 p.m. = 1:00–1:55 p.m.).
- Data columns in CSV:
  - Date (dd/mm/yyyy), Hour (0–23)
  - T5–T12 (water temperature in °C for mesocosms 5–12)
  - T21–T28 (water temperature in °C for mesocosms 21–28)
  - AirT (air temperature in °C)
- Temperature units: degrees Celsius.

## Methods and quality control
- Each mesocosm used two temperature sensors; data quality decisions:
  - If the difference between the two sensors is ≤ 0.2 °C, the two readings are averaged.
  - If the difference > 0.2 °C, readings are checked against the overall average per data logger. If a sensor drifted, that sensor is ignored and data from the remaining sensor are used for that time.
- Data gaps are due to sensor or logger problems; air temperature data are unavailable during the period when the air sensor was offline.

## Data availability and format
- Data provided as a comma-separated values (CSV) file with the columns described above.
- No calibration or formal quality-controlled pass included; usable with awareness of raw status and sensor drift adjustments noted above.

## Limitations and gaps
- Air temperature data missing for 17 Aug–6 Sep 2023.
- Data are raw and not fully quality-controlled; some hours rely on a single sensor due to drift.
- Metadata on individual sensor performance and calibration status is limited beyond the described quality rules.

## Context, provenance, and references
- Facility: UK Centre for Ecology & Hydrology (UKCEH) mesocosms facility.
- Funding: Horizon 2020 AQUACOSM-plus (Grant No. 871081) and NERC highlight topic grant NE/X00497X/1.
- Related reference: Feuchtmayr et al. (2019) Science of the Total Environment, 678, 227-238, describing effects of brownification and warming in mesocosms.
- This dataset forms part of a broader effort to understand how nutrient balance and temperature dynamics influence aquatic systems.