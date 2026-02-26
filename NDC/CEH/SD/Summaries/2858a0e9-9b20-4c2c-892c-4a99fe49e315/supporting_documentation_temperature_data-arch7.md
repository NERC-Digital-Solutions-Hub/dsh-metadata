# Hourly water temperature of 28 experimental mesocosms and air temperature from July to September 2022

- Dataset covers hourly water temperatures for 28 active mesocosms (numbers 2–15 and 18–31; 1, 16, 17, and 32 not used) plus corresponding air temperature, from 6 July to 30 September 2022.
- Measurements are derived from 5-minute readings averaged hourly; times are in GMT (UTC). Example: the 1 p.m. value is the average of 1:00–1:55 p.m.
- Data collection site: UKCEH mesocosms facility; supports AQUACOSM-plus project.

## Data content and structure

- File format: CSV with the following columns:
  - Date (dd/mm/yyyy)
  - Hour (0–23)
  - T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T18, T19, T20, T21, T22, T23, T24, T25, T26, T27, T28, T29, T30, T31 (temperatures in °C for each mesocosm)
  - AirT (air temperature in °C)
- Note: 28 mesocosms are included (2–15 and 18–31). Temperature data for mesocosms 1, 16, 17, and 32 are not provided.

## Data collection and quality control

- Sensors: two platinum resistance thermometers per mesocosm, logged by Campbell Scientific Data Logger; sensors positioned around mid-depth (~40 cm) with shading.
- Data handling rules:
  - If hourly difference between the two sensors < 0.2 °C, the two readings are averaged.
  - If the difference > 0.2 °C, data are checked against the overall logger average; if a sensor drift is detected (higher or lower than the average), data from the drifted sensor are ignored for those occasions, and data from the remaining sensor are used.
  - The dataset documents the number of occasions where data from only one sensor were used (example counts are provided in the notes for several mesocosms).
- Quality status:
  - Data are raw and have not been calibrated or quality controlled beyond visual checks.
  - Obvious hardware malfunctions have been removed.
  - Gaps are due to sensor or logger problems.
- Specific data issues noted:
  - During the study, loggers overheating affected mesocosms 18, 19, 20, 29, 30, and 31 on three occasions; 5-minute data were deleted and hourly data recalculated without this data.
  - A logger recording temperatures for mesocosms 5–12 failed from 1 September 11:00 to 7 September 14:00, with no data in that period.

## Temporal coverage and provenance

- Date range: 6 July – 30 September 2022
- Data provenance: funded by the European Union’s Horizon 2020 AQUACOSM-plus programme; grant No 871081
- Reference: Feuchtmayr H, et al. (2019) Science of the Total Environment (related study of the mesocosm facility and treatments)

## Relevance for GIS and map-based data products

- Enables spatial visualization of temperature patterns across 28 mesocosms within the facility.
- Can be combined with metadata (mesocosm ID, nutrient treatments, experimental conditions) to create layer-structured maps and dashboards.
- Suitable for time-series mapping and analysis when merged with other environmental variables or treatment data.
- Requires handling of missing data periods and sensor-specific data gaps during processing for GIS applications.

## Usage notes and caveats

- Treat the data as raw temperature observations pending calibration; apply quality filters as needed for GIS analyses.
- Be aware of periods with missing data due to sensor/logger issues; document gaps when performing spatial or temporal analyses.
- When integrating with other spatial datasets, ensure consistent time references (GMT) and alignment of mesocosm identifiers.