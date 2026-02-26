# Data from automatic water monitoring buoy from Bassenthwaite Lake 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

## Overview
- Automatic lake-monitoring buoy located in Bassenthwaite Lake, Cumbria, England.
- Variables include air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and lake water temperatures at multiple depths (1–18 m).
- Data coverage: 2012, 2013, 2014, and 2015.
- Water temperatures measured with platinum resistance thermometers.
- Measurements originally captured every 4 minutes; hourly averages provided.
- Time zone: GMT. Data referenced to 24-hour periods (hourly averages) in GMT.

## Measurement details and data processing
- Sampling interval: data collected every 4 minutes.
- Hourly averages are calculated over the previous hour, e.g., 2 p.m. = average of data from 1:00–2:00 p.m., including 2:00 p.m. data and excluding 1:00 p.m. data.
- Data sources for hourly averaging:
  - Campbell Scientific datalogger (until 24 January 2013).
  - Oracle database (from 24 January 2013 onwards).
- Depths for water temperature: 1, 2, 3, 4, 5, 6, 8, 10, 12, 14, 16, 18 meters.
- Additional sensors: Air_Temperature (°C), Pyranometer (solar radiation, W/m²), Wind Speed (m/s).
- Data format: comma-separated values (CSV).

## Quality control and limitations
- Data are raw and have not been calibrated or quality-controlled beyond visual checks.
- Obvious hardware errors removed; gaps occur due to buoy maintenance or sensor/logger problems.
- Temperature data: temperature chain was lost in January 2014; no lake temperature profile data from that date onward.
- All data are provided as GMT time; users should perform their own QA/QC and calibration as needed for analyses.

## Data structure
- Columns in CSV:
  - Date_GMT
  - Water_temperature at 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m
  - Air_Temperature
  - Pyranometer
  - Wind Speed
- Depths covered: 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m
- Units: temperatures in °C; solar radiation in W/m²; wind speed in m/s; Date_GMT in GMT.

## Usage and context
- The dataset is used in ongoing scientific studies, including PhD research.
- Notable publication using the dataset: Woolway, Maberly, Jones, Feuchtmayr (2014) on estimating the onset of thermal stratification in lakes from surface measurements.
- Suitable for analyses of vertical temperature profiles, surface energy balance, and stratification dynamics, with appropriate QA/QC and calibration as needed.