# Data from automatic water monitoring buoy from Esthwaite Water 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly S.C. (2017)

## Overview
- Automatic lake buoy-based dataset from Esthwaite Water, Cumbria, England.
- Contains meteorological and in-lake temperature measurements collected during 2012–2015.
- Used in ongoing scientific studies, including PhD research, highlighting its role in monitoring and research environments.

## Sampling Regime and Collection Methods
- Measurements collected by an automatic lake monitoring buoy with:
  - Air temperature (°C)
  - Solar radiation flux (Watts per square metre)
  - Wind speed (m/s)
  - Lake water temperatures at multiple depths (0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 12 m)
- Instruments: Platinum resistance thermometers for water temperatures; Campbell Scientific datalogger for data handling.
- Data frequency: Every 4 minutes; hourly averages computed by the datalogger.
  - Example: the 2 p.m. value is the average from 1–2 p.m., excluding 1 p.m. data and including 2 p.m. data.
- Time reference: All data are in GMT.
  
## Quality Control
- Presented data are raw and not yet calibrated or fully quality controlled.
- Visual checks performed; obvious hardware-malfunction data removed.
- Data gaps attributable to buoy maintenance or sensor/logger problems.
- A new temperature chain was installed in August 2015.

## Data Structure
- File format: Comma separated values (CSV).
- Columns include:
  - Date_GMT (Date and time in GMT)
  - Water_temperature: 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m (temperatures in °C)
  - Air_Temperature (°C)
  - Pyranometer (Solar radiation flux in W/m²)
  - Wind_Speed (m/s)

## Data Use and Context
- Data are being employed in multiple current scientific studies, including work by PhD students.
- Provides multi-parameter coverage (meteorological and vertical water temperature profiles) at fine temporal resolution.

## Implications for Monitoring Frameworks
- Strengths for monitoring:
  - High-frequency, multi-parameter data with a clear structure and time reference (GMT).
  - Detailed depth-resolved water temperature measurements enabling vertical profiling.
  - Documented data processing step for hourly averages and explicit QA statements.
- Challenges and considerations for monitoring frameworks:
  - Data calibration/QA needed before use in policy or indicators.
  - Raw data status and potential gaps require robust metadata and provenance tracking.
  - Maintenance-induced gaps and sensor issues highlight the need for data governance and resilience planning.
  - Metadata completeness (e.g., instrument specifications, calibration history) important for data reuse and comparability.
  - Data sharing and openness must balance with data quality and rights considerations.