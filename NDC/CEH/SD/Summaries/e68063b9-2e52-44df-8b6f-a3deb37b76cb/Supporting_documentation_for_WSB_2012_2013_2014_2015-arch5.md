# Data from automatic water monitoring buoy from Windermere South Basin 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly S.C. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
- Instruments collect air temperature, solar radiation, wind speed, and lake water temperatures at multiple depths (1–35 m).
- Data are 4-minute interval measurements, with hourly averages provided.
- Timeframe: 2012–2015; data are recorded in GMT.
- The dataset has contributed to published research and ongoing PhD studies.

## Sampling regime and collection methods
- Measurements taken by a buoy equipped with meteorological sensors and in-lake temperature sensors.
- Water temperature recorded at depths: 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, 35 m.
- Additional measurements: Air temperature, solar radiation (Pyranometer), and wind speed.
- Measurement cadence: every 4 minutes.
- Hourly averages calculated as the mean over the preceding hour, excluding the endpoint data from the start of the hour and including the data from the end of the hour.
- Data processing lineage:
  - Up to 1 June 2012: hourly averages produced by a Campbell Scientific datalogger.
  - From 1 June 2012 onwards: hourly averages produced by an Oracle database.

## Data quality and cleaning
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obviously erroneous hardware signals removed.
- Gaps attributable to buoy maintenance or sensor/logger problems.

## Data structure and fields
- Format: comma-separated values (CSV).
- Key columns:
  - Date_GMT: Date and time of measurement (GMT).
  - Water_temperature at depths: 1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m (degrees C).
  - Air_Temperature: Air temperature (degrees C).
  - Pyranometer: Solar radiation flux (W/m^2).
  - Wind Speed: Wind speed (m/s).

## Temporal coverage and scope
- Period: 2012–2015 (inclusive).
- Data include 2012 through 2015 measurements, with instrument and database changes affecting data processing from mid-2012 onward.

## Provenance, usage, and attribution
- The dataset has supported multiple current scientific studies, including PhD work.
- Acknowledgement and citation example: Woolway, R.I., Maberly S.C., Jones, I.D., Feuchtmayr, H. (2014) on a method for estimating onset of thermal stratification in lakes.
- Users should attribute findings to the provided citation and note the data’s raw status and quality checks when presenting analyses.

## Data governance considerations for Data Stewards
- Metadata should document:
  - Measurement depths and sensor types, units, and data processing steps (hourly averaging method, end-of-hour handling).
  - Time zone (GMT) and any changes in data storage (Campbell Scientific datalogger vs. Oracle database) to support data lineage.
  - Quality control status: raw data, with notes on manual cleaning and known gaps due to maintenance or hardware issues.
  - Data gaps and their causes to aid users in assessing data completeness.
- Ensure clear data provenance and provide guidance on calibration status and expected updates or corrections.
- Plan for discoverability and reuse by including the dataset in appropriate data portals with the described schema and a machine-readable metadata record.
- Include licensing/usage terms and allow for proper citation to the referenced publication(s).