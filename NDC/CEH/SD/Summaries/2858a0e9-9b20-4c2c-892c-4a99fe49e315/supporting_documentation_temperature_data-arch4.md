# Hourly water temperature of 28 experimental mesocosms and air temperature from July to September 2022

## Overview
- Dataset of hourly water temperature from 28 mesocosms and concurrent air temperature measurements.
- Time period: July 6 to September 30, 2022; all times in GMT.
- Location: UKCEH mesocosms facility; mesocosms are 1 m deep, 2 m diameter, approximately 2800 L of reservoir water per unit.
- Measurements:
  - Water temperature logged every 5 minutes by two platinum resistance thermometers (PRTs) shaded by a plastic cover, positioned around mid-depth (~40 cm) and offset 30 cm from the wall.
  - Air temperature measured at a weather station (Vaisala WXT520) at ~2.7 m height.
- Experimental design context: multiple inorganic/organic phosphorus and ammonium nutrient treatments applied.
- Data collection supported by EU Horizon 2020 AQUACOSM-plus (grant No 871081).

## Data collection and scope
- Mesocosms are labeled 1–32, but numbers 1, 16, 17, and 32 were not used in this experiment.
- Data include raw 5-minute records and hourly averages derived from those records.
- The dataset covers hourly averages, calculated by averaging 5-minute values within each hour (e.g., 1 p.m. value is the average from 1:00 to 1:55).
- Calibration status: raw data without calibration or formal quality control; visual checks performed to remove obvious hardware errors.

## Data structure and contents
- File format: comma-separated values (CSV).
- Columns include:
  - Date (dd/mm/yyyy) and Hour (0–23).
  - Temperature columns for mesocosms (e.g., T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15, T18, T19, T20, T21, T22, T23, T24, T25, T26, T27, T28, T29, T30, T31).
  - Air temperature: AirT.
- Note: Temperature data from mesocosms 1, 16, 17, and 32 are not included; data available for mesocosms 2–15 and 18–31.
- Data gaps and sensor issues:
  - Some loggers overheating caused 5-minute data gaps for mesocosms 18, 19, 20, 29, 30, and 31; hourly data were recalculated excluding the problematic periods.
  - A logger for mesocosms 5–12 failed from Sept 1 11:00 to Sept 7 14:00.
  - When two sensors differed by more than 0.2 °C, one sensor was discarded; otherwise, the two sensors were averaged if within 0.2 °C.
  - Counts of occasions where only one sensor contributed data: 158 (4), 391 (6), 1614 (11), 8 (20), 7 (22), 14 (24), 7 (25), 17 (31). In such cases, data from a single sensor was used to derive the hourly value.

## Quality, limitations, and data provenance
- Data are raw and not calibrated or quality controlled beyond visual checks.
- Any obvious hardware malfunctions or data gaps have been removed or excluded; remaining gaps attributed to sensor or logger problems.
- Measurements are time-stamped in GMT; date range specified (6 July–30 September 2022).
- Data provenance includes references to the broader mesocosm facility and prior related work (Feuchtmayr et al., 2019) and project funding details (AQUACOSM-plus).

## Data usage and governance considerations for data leaders
- Metadata needs:
  - Sensor IDs, placement details, and calibration status; logger IDs; any drift corrections applied.
  - Documentation of data cleaning rules (e.g., the 0.2 °C difference threshold and single-sensor selections).
- Data quality flags and provenance:
  - Explicit flags for hours affected by overheating or logger failure for transparency and reusability.
- Data discoverability and interoperability:
  - Ensure clear mapping of T2–T31 columns to specific mesocosms and the exclusion of mesocosms 1, 16, 17, and 32.
  - Maintain timezone and timestamp conventions (GMT) for cross-dataset integration.
- Reproducibility:
  - Provide clear method notes for hourly averaging and sensor comparison rules to enable replication or reprocessing.
- Potential use:
  - Baseline for analyses of temperature dynamics under different nutrient treatments and validation of models of mesocosm thermal regimes.

## References
- Feuchtmayr H, Rankin G, McShane G. (2022). Hourly water temperature of 28 experimental mesocosms and air temperature from July to September 2022. UKCEH dataset. Funding: European Union's Horizon 2020 AQUACOSM-plus (grant No 871081).
- Feuchtmayr H, Pottinger TG, Moore A, De Ville MM, Caillouet L, Carter HT, Pereira MG, Maberly SC. (2019). Effects of brownification and warming on algal blooms, metabolism and higher trophic levels in productive shallow lake mesocosms. Science of the Total Environment, 678, 227-238.