# Data from automatic water monitoring buoy from Bassenthwaite Lake 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy in Bassenthwaite Lake, Cumbria, England.
- Instruments measure: air temperature, solar radiation (pyranometer), wind speed, and in-lake temperature profiles at multiple depths.
- Depths: 1, 2, 3, 4, 5, 6, 8, 10, 12, 14, 16, and 18 meters.
- Data cadence: raw measurements every 4 minutes; hourly averages computed by a Campbell Scientific datalogger.
- All times are in GMT; data span 2008–2011 and are used in several scientific studies.

## Sampling regime and collection methods
- Data collected by a buoy carrying meteorological instruments and temperature sensors for lake water.
- Temperature measurements use platinum resistance thermometers at specified depths.
- Hourly averages reflect the previous hour’s data (excluding the start of the hour, including the end of the hour).

## Quality control and data integrity
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware faults removed.
- Gaps due to buoy maintenance or sensor/logger problems.
- Specific missing periods: February 2010, May 2011, July 2011.

## Data structure and variables
- Data format: comma-separated values (CSV).
- Columns include:
  - Date_GMT: date and time of measurement (GMT)
  - Water_temperature at 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m (degrees C)
  - Air_Temperature (degrees C)
  - Pyranometer: Solar radiation flux (Watts per square metre)
  - Wind_Speed (m/s)

## Temporal coverage and data gaps
- Coverage: 2008, 2009, 2010, and 2011.
- Notable gaps caused by maintenance: February 2010; May 2011; July 2011.

## Data usage and publications
- Used in multiple scientific studies, including:
  - 2014: A method for estimating onset of thermal stratification from surface measurements (Woolway et al., Water Resources Research).
  - 2015: Diel variability in epilimnetic temperature across five English lakes (Woolway et al., Inland Waters).
  - 2016: Diel surface temperature range scales with lake size (Woolway et al., PLoS ONE).
- Dataset also used by PhD students and other researchers.

## Data accessibility and storage
- Described as raw data within a CSV dataset; data management practices include storage and uploading to appropriate data portals as part of standard monitoring workflows.

## Relevance to environmental monitoring objectives
- Provides high-resolution, vertically resolved thermal and meteorological data for Bassenthwaite Lake.
- Supports assessment of thermal structure, stratification onset, and diel temperature dynamics.
- Useful for cross-study standardization and methodological comparisons in environmental monitoring.