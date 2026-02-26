# Hourly water temperature of 28 experimental mesocosms and air temperature from July to September 2022

## Overview
- Dataset of hourly water temperature for mesocosms and accompanying air temperature data from July 6 to September 30, 2022.
- Location: UKCEH mesocosms facility.
- Mesocosms: 28 experimental units (labels 1–32, with 1, 16, 17, and 32 not used in this experiment).
- Measurements: water temperature (hourly average) from two platinum resistance thermometers (PRTs) shaded by a plastic cover, logged by a Campbell Scientific Data Logger; air temperature measured at a weather station at ~2.7 m height.
- Data units: degrees Celsius; times in GMT.
- Data are raw (not calibrated/fully quality controlled) but visually checked; obvious hardware errors removed.

## Data collection and scope
- Sampling: water temperature recorded every 5 minutes; hourly values are the average of the 5-minute data within each hour (e.g., 1 p.m. = average of 1:00–1:55 p.m.).
- Sensor setup: sensors placed around mid-depth (~40 cm) and offset from the mesocosm side wall; measurements from mesocosms 2–15 and 18–31 (excluding 1, 16, 17, 32) plus air temperature.
- Data quality events:
  - Logger overheating affected mesocosms 18, 19, 20, 29, 30, 31 on three occasions; 5-minute data deleted; hourly data recalculated without affected data.
  - One logger failed for mesocosms 5–12 from Sept 1 11:00 to Sept 7 14:00; no data recorded during that interval.
- Sensor drift handling:
  - When hourly data from the two sensors differed by more than 0.2 °C, data were checked against the overall logger-average; if drift detected, the anomalous sensor was ignored and data from the remaining sensor used.
  - Occasions where data came from a single sensor only are recorded (counts shown for specific sensors).

## Data processing and quality control
- Data are raw and have not been calibrated or fully quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Gaps reflect sensor or logger problems rather than data omissions due to sampling.

## Data structure and variables
- File format: comma-separated values (CSV).
- Columns:
  - Date: dd/mm/yyyy
  - Hour: 0–23
  - T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15: water temperature for mesocosms 2–15
  - T18, T19, T20, T21, T22, T23, T24, T25, T26, T27, T28, T29, T30, T31: water temperature for mesocosms 18–31
  - AirT: air temperature
- Note: Mesocosms 1, 16, 17, and 32 are not included in the dataset; therefore, T1, T16, T17, T32 columns are absent.
- Temperature units: degrees Celsius.
- Time reference: Greenwich Mean Time (GMT).

## Data limitations and gaps
- Data are not fully calibrated or quality-controlled; users should apply calibration/validation if precise accuracy is required.
- Occasional data gaps due to sensor or logger failures; some city-wide issues (overheating, logger outages) result in missing hourly values.
- Where sensor drift occurred, reliance on single-sensor data may affect some hourly observations.

## Provenance and funding
- Data collection supported by the European Union Horizon 2020 programme under grant agreement No 871081 (AQUACOSM-plus).
- Reference for context: Feuchtmayr et al. (2019) Science of the Total Environment; effects of brownification and warming on algal blooms and ecosystem metabolism.

## Potential uses and data support recommendations
- Suitable for analyzing temporal dynamics of mesocosm water temperature relative to air temperature, including treatment effects if combined with nutrient regimes.
- Useful for building dashboards or self-serve analyses of temperature trends across mesocosms and time.
- Before use, perform calibration/validation and handle gaps (e.g., imputation or exclusion) as appropriate for the analysis.
- Validate sensor agreement thresholds (e.g., 0.2 °C) and document any sensor-specific data removals or single-sensor periods.
- Reference metadata and methodology when integrating with other datasets or when reproducing analyses.