# Hourly water temperature of 16 experimental mesocosms and air temperature from April to November 2023

## What this dataset contains
- Hourly water temperature data for 16 experimental mesocosms and accompanying air temperature data, covering 21 April to 7 November 2023.
- Mesocosms used: numbers 5–12 and 21–28 (1 m deep, 2 m diameter; ~2800 L water from Windermere).
- Water temperature measured every 5 minutes using two platinum resistance thermometers (PRTs) shaded by a plastic cover, positioned around mid-depth (~40 cm) and offset ~30 cm from the mesocosm wall; data logged by a Campbell Scientific Data Logger.
- Air temperature recorded at a Vaisala weather transmitter WXT520 weather station located in the mesocosm compound at ~2.7 m height.
- Experimental nutrient treatments applied (phosphate and nitrate ratio variations).

## Data collection and instrumentation
- Temperature sensors: two PRTs per mesocosm for redundancy; if drift suspected, data from one sensor may be used.
- Data loggers: Campbell Scientific system recording 5-minute temperature readings.
- Time reference: all data provided in Greenwich Mean Time (GMT).

## Temporal coverage and data processing
- Hourly averages computed from 5-minute readings (e.g., 1 p.m. value is the average of 1:00–1:55 p.m.).
- Date range: 21 April to 7 November 2023.
- Air temperature sensor issue: stopped on 17 August and reconnected on 6 September; no air temperature data available during that period.
- Data processing approach for sensor agreement:
  - If the hourly difference between the two mesocosm sensors < 0.2 °C, average the two.
  - If the difference > 0.2 °C, compare to the overall average across loggers; if a sensor drift is indicated, the aberrant sensor is ignored for those occasions (one sensor used).

## Quality control and data handling
- Data are raw and have not yet been calibrated or fully quality controlled.
- Visual checks performed; obvious hardware malfunctions removed.
- Data gaps attributed to sensor or logger problems.
- Instances where only one sensor contributed hourly data (per mesocosm) recorded; examples include mesocosm 11 (231 occasions) and mesocosm 12 (1,594 occasions).

## Data structure and format
- Format: comma-separated values (CSV).
- Columns:
  - Date (dd/mm/yyyy)
  - Hour (0–23)
  - T5–T12 (water temperatures for mesocosms 5–12)
  - T21–T28 (water temperatures for mesocosms 21–28)
  - AirT (air temperature)
- Units: degrees Celsius (°C).

## Temporal gaps and issues
- Air temperature data missing from 17 August to 6 September 2023 due to sensor downtime.
- Other data gaps present due to sensor or logger problems.

## Metadata, provenance, and references
- Funding:
  - European Union Horizon 2020 AQUACOSM-plus (grant agreement No 871081)
  - NERC highlight topic grant NE/X00497X/1 (impact of nutrient imbalance on carbon flux from lakes)
- Facility: UKCEH mesocosms facility.
- Reference: Feuchtmayr H, Pottinger TG, Moore A, et al. (2019) Effects of brownification and warming on algal blooms, metabolism and higher trophic levels in productive shallow lake mesocosms. Science of the Total Environment, 678, 227-238. https://doi.org/10.1016/j.scitotenv.2019.04.105

## Usage notes for analysts
- The dataset provides raw, hourly-averaged temperature data suitable for monitoring environmental conditions and assessing temperature-related responses to nutrient treatments.
- Prior to analysis, apply calibration/QA procedures and handle gaps (noted above) consistently.
- Consider integrating with other environmental datasets and metadata (e.g., treatment conditions, sensor status) to enhance cross-dataset comparability and policy-relevant assessments.
- Ensure proper attribution to funding sources and facility when using the data.