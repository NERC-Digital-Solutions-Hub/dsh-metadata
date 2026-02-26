# Sampling Regime and Collection Methods

## Overview
- Location: automatic lake monitoring buoy on Blelham Tarn, Cumbria, England.
- Instruments: meteorological sensors and in-lake temperature sensors.
- Measured variables and units:
  - Air temperature in °C.
  - Solar radiation flux (Pyranometer) in W/m^2.
  - Wind speed in m/s.
  - Lake water temperatures at depths: 0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, and 12 m (each in °C).
- Sampling cadence: data collected every 4 minutes; hourly averages computed by a Campbell Scientific datalogger.
- Time reference: all data in GMT (UTC); dates span 2008–2011.
- Hourly averaging rule: the value for a given hour is the average of the preceding hour, excluding the data at the start of the hour and including the data at the end of the hour (example provided for 2 p.m.).

## Quality Control
- Data are raw and have not been calibrated or quality controlled yet.
- Visual checks performed; obvious hardware-related errors removed.
- Data gaps attributed to buoy maintenance or sensor/logger problems.

## Data Structure and Metadata
- Format: comma-separated values (CSV).
- Columns:
  - Date_GMT: date and time in GMT.
  - Water_temperature: 0.5m, 1m, 2m, 3m, 4m, 5m, 6m, 7m, 8m, 9m, 10m, 12m depths (each in °C).
  - Air_Temperature: air temperature in °C.
  - Pyranometer: solar radiation flux in W/m^2.
  - Wind_Speed: wind speed in m/s.
- Notes: explicit mapping of depth-based water temperature measurements; all temperature-related data labeled by depth.

## Usage and Provenance
- The buoy data are used in multiple current scientific studies, including PhD work.
- Publications utilizing the dataset include:
  - Woolway et al. (2014) A novel method for estimating the onset of thermal stratification in lakes from surface water measurements. Water Resources Research.
  - Woolway et al. (2015) A comparison of the diel variability in epilimnetic temperature for five lakes in the English Lake District. Inland Waters.
  - Woolway et al. (2016) Diel surface temperature range scales with lake size. PLoS ONE.
- The dataset is linked to a broad set of authors and research outputs; citations indicate ongoing use and impact.

## Challenges for Data Stewards
- Incomplete picture of user needs and priorities.
- Timely access to data from the buoy.
- Encouraging data creators to meet standards (metadata completeness, consistent formats).
- Interoperability across multiple systems and formats, including legacy or bespoke solutions.
- Handling large datasets and older databases that may require custom transfer approaches.

## Additional Notes
- The dataset is actively used in ongoing studies and supports multiple researchers and publications.