# Hourly water temperature of 16 experimental mesocosms and air temperature from April to November 2023

## Overview
- Dataset of hourly water temperatures from an experimental mesocosm facility and hourly air temperatures for 21 April to 7 November 2023.
- Location: North West England; mesocosms (1 m depth, 2 m diameter) filled with ~2800 L water from Windermere.
- Mesocosms used: numbers 5–12 and 21–28.
- Purpose includes examining effects of nutrient treatments (phosphate and nitrate) alongside temperature data.
- Time zone: GMT.

## Measurements and setup
- Water temperature: measured every 5 minutes using two platinum resistance thermometers (PRTs), shaded by a plastic cover, near mid-depth (~40 cm), and offset ~30 cm from the wall.
- Air temperature: measured at a weather station within the mesocosm compound, using a Vaisala WXT520 at ~2.7 m height.
- Data logging: Campbell Scientific Data Logger.
- Data aggregation: hourly averages computed from 5-minute intervals (e.g., 1:00–1:55 p.m. → 1 p.m. value).

## Data quality and processing
- Air temperature gap: sensor stopped working 17 August to 6 September 2023; no air temperature data during this period.
- Sensor comparison and handling:
  - If the difference between the two water temperature sensors < 0.2 °C, average the two.
  - If the difference > 0.2 °C, compare to overall logger average; if drift detected, ignore the offending sensor and use data from the remaining sensor for those occasions.
  - The dataset includes counts of occasions where only one sensor data was used (illustrative in accompanying table).
- Quality status: raw data, not yet calibrated or formally quality controlled. Visual checks performed; obvious hardware errors removed. Gaps due to sensor/logger problems.

## Data structure and format
- Format: comma separated values (CSV).
- Columns:
  - Date (dd/mm/yyyy)
  - Hour (0–23)
  - T5–T12 (water temperatures for mesocosms 5–12)
  - T21–T28 (water temperatures for mesocosms 21–28)
  - AirT (air temperature)
- Temperature units: degrees Celsius (°C).

## Temporal coverage and gaps
- Period: 21 April to 7 November 2023.
- Air temperature data missing 17 August–6 September 2023.
- Water temperature data coverage varies by mesocosm due to sensor checks and drift handling; some occasions rely on a single sensor.

## Funding and references
- Funding: European Union Horizon 2020 AQUACOSM-plus (grant No 871081) and NERC highlight topic NE/X00497X/1 (impact of nutrient imbalance on carbon flux from lakes).
- Reference: Feuchtmayr et al. (2019) on effects of brownification and warming in mesocosm experiments.