# Data from automatic water monitoring buoy from Bassenthwaite Lake 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

## Overview
- Automatic lake monitoring buoy operated in Bassenthwaite Lake, Cumbria, England.
- Sensors measure air temperature, solar radiation (pyranometer), wind speed, and lake temperature profiles at multiple depths (1–18 m).
- Data coverage: 2012–2015; data recorded every 4 minutes; hourly averages calculated.
- Time zone: all data reported in GMT.
- Data collection method changed from Campbell Scientific datalogger (through 24 Jan 2013) to Oracle database (from 24 Jan 2013 onward).

## Data Content and Structure
- Measurements and units:
  - Water temperature: degrees C at depths 1, 2, 3, 4, 5, 6, 8, 10, 12, 14, 16, 18 m.
  - Air temperature: degrees C.
  - Solar radiation: Watts per square metre.
  - Wind speed: metres per second.
- Data format: comma-separated values (CSV).
- Columns in CSV:
  - Date_GMT: date and time of measurement (GMT).
  - 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m: water temperatures at corresponding depths.
  - Air_Temperature: air temperature (°C).
  - Pyranometer: solar radiation flux (W/m²).
  - Wind Speed: wind speed (m/s).

## Quality Control and Limitations
- Data are raw and have not been calibrated or fully quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Gaps occur due to buoy maintenance or sensor/logger problems.
- Specific limitation: temperature profile data unavailable after January 2014 due to loss of the temperature chain.
- No explicit mention of embargoes or proprietary restrictions; data availability may depend on ongoing usage in studies.

## Data Availability, Usage, and References
- Dataset has supported ongoing scientific studies, including PhD work.
- Notable publication using this dataset: Woolway, R.I., Maberly, S.C., Jones, I.D., Feuchtmayr, H. (2014) on estimating the onset of thermal stratification in lakes from surface measurements (Water Resources Research, 50(6), 5131-5140).

## Provenance and Citation
- Source authors: Jones, I.D.; Feuchtmayr, H.; Maberly, S.C.
- Publication year: 2017.
- Dataset intended to support transparent reuse and traceability for researchers relying on lake buoy observations and derived hourly data.

## Data Stewardship Considerations
- Metadata completeness: ensure documentation includes sensor types, calibration status, data processing steps (hourly averaging method), time zone, and dates of data collection and system changes.
- Data quality workflow: establish calibration procedures, flag quality-controlled data, and maintain a log of data gaps with reasons (maintenance, sensor failure).
- Provenance tracking: maintain lineage from raw 4-minute records to hourly aggregates, including database transition details ( Campbell Scientific to Oracle) for reproducibility.
- Versioning and updates: implement a clear schema for versioning new data, especially when sensor configurations or data pipelines change.
- Interoperability: ensure consistent naming conventions for depth-specific columns and standardize units across datasets to facilitate cross-dataset integration.
- Access and licensing: confirm data access rights, any usage restrictions, and provide DOI or persistent identifier if hosting in a data portal.
- User needs and discoverability: provide comprehensive metadata to support discovery, re-use, and appropriate interpretation of gaps (e.g., post-2014 temperature profile unavailability).