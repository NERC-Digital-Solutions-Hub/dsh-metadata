# Data from automatic water monitoring buoy from Bassenthwaite Lake 2012, 2013, 2014 and 2015

## Overview
- Dataset collected from an automatic lake monitoring buoy on Bassenthwaite Lake, Cumbria, England.
- Measures meteorological variables (air temperature, solar radiation, wind speed) and lake temperature profiles.
- Time period: 2012–2015; data recorded in GMT.
- Data have supported multiple scientific studies, including work by PhD students and publications on lake stratification.

## Sampling regime and collection methods
- Instruments: air temperature sensors, pyranometer (solar radiation flux), wind speed sensors, and platinum resistance thermometers for lake temperature.
- Depths for temperature: 1 m, 2 m, 3 m, 4 m, 5 m, 6 m, 8 m, 10 m, 12 m, 14 m, 16 m, and 18 m.
- Data cadence: every 4 minutes; hourly averages computed from the preceding hour (examples provided in dataset description).
- Data storage: Campbell Scientific datalogger used until 24 January 2013; Oracle database used from 24 January 2013 onwards.

## Quality control and limitations
- Data provided as raw, not yet calibrated or quality controlled.
- Visual checks conducted; obvious hardware faults removed.
- Gaps due to buoy maintenance or sensor/logger issues.
- Temperature measurement chain was lost in January 2014; no lake temperature profile data after that date.

## Data structure and access
- Format: comma-separated values (CSV).
- Columns:
  - Date_GMT: date and time in GMT.
  - Water_temperature at depths: 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m (degrees C).
  - Air_Temperature (degrees C).
  - Pyranometer (solar radiation flux in W/m^2).
  - Wind Speed (m/s).
- Metadata includes units, depth definitions, and measurement methods.
- Data used in ongoing studies and referenced in publications (e.g., Woolway et al. 2014).

## Usage and impact
- Provides a time series platform for analyzing lake thermal structure, stratification onset, and surface–deep temperature relationships.
- Suitable for integration with other datasets or modelling efforts on lake dynamics.
- Widely utilized in scientific research and by PhD students exploring aquatic systems.

## Data governance, discoverability, and updates
- Described data lineage: instrumentation, data collection method, and storage transition (datalogger to Oracle).
- Clear documentation of data quality status, measurement units, and depth-specific variables to aid discoverability and reuse.
- Data availability contingent on ongoing access to the CSV dataset and accompanying methodological notes.

## Notable references
- Woolway, R.I., Maberly, S.C., Jones, I.D., Feuchtmayr, H. (2014). A novel method for estimating the onset of thermal stratification in lakes from surface water measurements. Water Resources Research, 50(6), 5131-5140.