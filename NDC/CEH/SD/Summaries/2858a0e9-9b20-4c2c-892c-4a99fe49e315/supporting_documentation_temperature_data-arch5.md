# Hourly water temperature of 28 experimental mesocosms and air temperature from July to September 2022

## Overview
- Dataset of hourly water temperature for 28 mesocosms and hourly air temperature covering 6 July to 30 September 2022.
- Mesocosms are labeled 1–32, but only 2–15 and 18–31 were used (28 mesocosms in total). Measurements from two platinum resistance thermometers (PRTs) per mesocosm, shielded by a plastic cover, logged by a Campbell Scientific Data Logger.
- Water temperature sensors are positioned around mid-depth (~40 cm) with a radial offset of ~30 cm from the mesocosm wall; air temperature measured at a Vaisala weather transmitter WXT520 at ~2.7 m height.
- Data collection supported by EU Horizon 2020 AQUACOSM-plus (Grant No 871081). Reference context provided by Feuchtmayr et al. 2019.

## Data Content
- Values are hourly averages derived from 5-minute readings.
- Dates are in GMT (UTC); data cover 6 July to 30 September 2022.
- Columns include:
  - Date (dd/mm/yyyy), Hour (0–23)
  - T2–T15, T18–T31 (temperatures in °C for mesocosms 2–15 and 18–31)
  - AirT (air temperature in °C)
- Note: Data are raw (not calibrated or fully quality controlled) but visually checked; obvious hardware errors removed.

## Data Collection and Processing Details
- Two sensors per mesocosm; when their hourly values differ by ≤0.2 °C, the average is used. If the difference >0.2 °C, the reading is checked against the overall logger average; if a sensor shows drift, that sensor is ignored and the other sensor's data used.
- Sensor/logger issues caused data gaps:
  - Overheating in mesocosms 18, 19, 20, 29, 30, 31 led to three occasions of 5-minute data deletion before hourly averaging.
  - A logger for mesocosms 5–12 failed during 1 Sept 11:00 to 7 Sept 14:00.
- Counts of single-sensor hourly data occurrences are reported (indicating when one sensor’s data were used due to drift).

## Data Quality and Gaps
- Raw data not yet calibrated or fully quality controlled; visual checks performed and hardware-origin errors removed.
- Gaps attributed to sensor or logger problems rather than calibration issues.
- Overall, the processing notes provide traceability for how hourly values were derived from 5-minute measurements and how anomalies were handled.

## Data Structure and Format
- CSV file with columns:
  - Date (dd/mm/yyyy)
  - Hour (0–23)
  - T2, T3, T4, T5, T6, T7, T8, T9, T10, T11, T12, T13, T14, T15
  - T18, T19, T20, T21, T22, T23, T24, T25, T26, T27, T28, T29, T30, T31
  - AirT
- Temperature values are in degrees Celsius.

## Provenance and References
- Funding: European Union Horizon 2020 AQUACOSM-plus, Grant No. 871081.
- Related context: UKCEH mesocosms facility; reference to Feuchtmayr et al. (2019) Science of the Total Environment for background on the facility and prior experiments.

## Implications for Data Stewardship
- Clear documentation of instrumentation, deployment, averaging method, and data handling (including drift handling and data gaps) supports governance, reproducibility, and reuse.
- Highlights the need for consistent metadata when sharing across heterogeneous sensor systems and loggers.
- Indicates the dataset status as raw with partial QC, guiding data users to account for calibration needs and known issues in analyses.
- Provides a defined temporal scope and time zone (GMT) for discoverability and integration with other datasets.