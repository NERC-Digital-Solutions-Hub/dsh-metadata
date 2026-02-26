# Data from automatic water monitoring buoy from Bassenthwaite Lake 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly, S.C. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy in Bassenthwaite Lake, Cumbria, England.
- Measures meteorological variables and in-lake temperature profile.
- Variables include air temperature (°C), solar radiation flux (W/m^2), wind speed (m/s), and lake temperatures at depths 1–18 m.
- Data collected every 4 minutes; hourly averages provided.
- Time frame: 2012–2015; times are given in GMT.

## Sampling regime and collection methods
- Instruments include a buoy with meteorological sensors and platinum resistance thermometers for lake temperature at multiple depths (1, 2, 3, 4, 5, 6, 8, 10, 12, 14, 16, 18 m).
- Hourly averages computed from 4-minute data; method of averaging described (previous hour’s data excluded, current hour included).
- Data files: CSV format with specific column naming for each depth and variable.
- Data collection transitioned from a Campbell Scientific datalogger (until 24 January 2013) to an Oracle database (from 24 January 2013 onwards).

## Quality Control
- Data are raw and not yet calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Gaps occur due to buoy maintenance or sensor/logger problems.
- Temperature profile data missing from January 2014 onward due to loss of the temperature chain.

## Data structure
- CSV columns:
  - Date_GMT: Date and time (GMT) of measurement.
  - Water_temperature at depths: 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m (°C).
  - Air_Temperature (°C).
  - Pyranometer: Solar radiation flux (W/m^2).
  - Wind Speed (m/s).

## Use and context
- Dataset has been used in several current scientific studies and by PhD researchers.
- Example publication leveraging the data: Woolway, Maberly, Jones, Feuchtmayr (2014) on estimating the onset of thermal stratification in lakes from surface measurements (Water Resources Research).

## Limitations and considerations for analysts
- Must apply calibration/quality control for rigorous analyses due to raw data status.
- Notable data gaps, especially after January 2014 for the lake temperature profile.
- 4-minute sampling vs hourly averages; analysts may need to resample to align with analysis needs.
- All data are in GMT; time-zone alignment needed when integrating with other datasets.

## Potential analyses and questions for data-driven insights
- Correlations between surface meteorology (air temperature, solar radiation, wind) and subsurface temperatures across depths.
- Detection and characterization of thermal stratification onset using surface and depth-temperature data.
- Diurnal and seasonal patterns in lake temperature and stability of the water column.
- Integration with other local datasets to address scale, accessibility, and data standardization challenges.