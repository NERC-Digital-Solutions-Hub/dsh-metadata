# Hourly water temperature of 16 experimental mesocosms and air temperature from April to November 2023

## Overview
- A high-resolution environmental dataset capturing hourly water temperatures from 16 mesocosms and concurrent air temperature from April to November 2023 in NW England.
- Mesocosms were used to study effects of nutrient ratio treatments (phosphate and nitrate) on metabolic processes and algal dynamics.

## Experimental setup and measurements
- Mesocosms: 1 m deep, 2 m diameter, containing ~2800 L of water from Windermere; labeled 1–32 (only mesocosms 5–12 and 21–28 were used).
- Sensors: two platinum resistance thermometers (PRTs) shaded by a plastic cover, placed at mid-depth (~40 cm) and offset ~30 cm from the wall; temperatures logged by a Campbell Scientific Data Logger.
- Air temperature: measured at a weather station within the mesocosm compound (Vaisala WXT520) at ~2.7 m height.
- Data period: 21 April to 7 November 2023; all times in Greenwich Mean Time (GMT).

## Measurement details and data processing
- Data granularity: 5-minute temperature measurements converted to hourly averages (e.g., 1 PM value equals the average from 1:00 to 1:55 PM).
- Temperature columns: T5–T12 and T21–T28 for mesocosms; AirT for air temperature.
- Data status: raw data, not yet calibrated or quality controlled; visual checks performed and obvious hardware errors removed.
- Data gaps: caused by sensor or logger problems.
- Sensor discrepancies and handling: if the two sensors differed by less than 0.2 °C, their average was used; if the difference exceeded 0.2 °C, data were checked against the overall logger average, and drifted sensors were ignored in those instances, using data from the remaining sensor.
- Single-sensor occasions: mesocosm 11 had 231 occasions; mesocosm 12 had 1594 occasions where only one sensor contributed hourly data.

## Data structure and metadata
- File format: comma-separated values (CSV).
- Columns:
  - Date (dd/mm/yyyy)
  - Hour (0–23)
  - T5, T6, T7, T8, T9, T10, T11, T12 (temperatures in °C for mesocosms 5–12)
  - T21, T22, T23, T24, T25, T26, T27, T28 (temperatures in °C for mesocosms 21–28)
  - AirT (air temperature in °C)

## Data gaps and caveats
- Air temperature data gaps: air sensor stopped working from 17 August to 6 September 2023; no air data during this period.
- Quality control status: data are raw and not calibration-controlled; some gaps exist due to hardware issues.
- Metadata richness: standard details about sensor placement and data processing are provided to support future reuse and integration into monitoring frameworks.

## Data provenance and governance
- Funding: European Union Horizon 2020 AQUACOSM-plus (grant No 871081) and NERC grant NE/X00497X/1.
- Reference: Feuchtmayr et al. (2019) for background on mesocosm facilities and related research.

## Implications for monitoring frameworks
- High-frequency, multi-sensor temperature monitoring across multiple controlled units provides robust indicators of thermal dynamics and responses to nutrient treatments.
- Key monitoring metrics evidenced:
  - Redundancy and cross-checking of sensors to mitigate drift and ensure data integrity.
  - Transparent handling of data gaps, sensor downtime, and post-processing steps (hourly aggregation from 5-min data).
  - Clear data provenance, including calibration status, hardware issues, and governance.
- Considerations for policy-relevant monitoring:
  - Ensure availability of raw and processed data along with metadata and sensor status to enable auditability and reuse.
  - Maintain data governance practices that allow open sharing while documenting limitations due to sensor downtime or calibration status.
  - Use high-resolution temporal data to inform models of temperature-dependent ecological processes under nutrient manipulation.