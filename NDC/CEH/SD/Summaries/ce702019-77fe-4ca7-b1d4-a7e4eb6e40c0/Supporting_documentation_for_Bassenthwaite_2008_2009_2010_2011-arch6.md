# Data from automatic water monitoring buoy from Bassenthwaite Lake 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Overview
- Dataset from an automatic lake monitoring buoy at Bassenthwaite Lake, Cumbria, England.
- Measurements include meteorological variables and in-lake temperature profiles.
- Time period: 2008–2011.
- Variables:
  - Air temperature (°C)
  - Solar radiation flux (Pyranometer, W/m^2)
  - Wind speed (m/s)
  - Lake water temperatures at depths of 1, 2, 3, 4, 5, 6, 8, 10, 12, 14, 16, and 18 meters (°C)

## Sampling regime and collection methods
- Measurements collected by an automatic buoy with meteorological instruments and in-lake temperature sensors.
- Data cadence: every 4 minutes; hourly averages are provided by a Campbell Scientific data logger.
- Hourly averaging rule: the value for time t is the average from the previous hour up to and including time t (e.g., 2 p.m. equals the average of 1–2 p.m., excluding 1 p.m. data, including 2 p.m. data).
- All timestamps are in GMT (UTC).

## Quality control
- Data are raw and have not been calibrated or quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Gaps occur due to buoy maintenance or sensor/logger problems.
- Notable data gaps: February 2010, May 2011, July 2011 (maintenance period).

## Data structure and formats
- Data provided as a comma-separated values (CSV) file.
- Columns:
  - Date_GMT: Date and time (GMT) of measurement
  - 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m: Water temperature at specified depths (°C)
  - Air_Temperature: Air temperature (°C)
  - Pyranometer: Solar radiation flux (W/m^2)
  - Wind_Speed: Wind speed (m/s)

## Data usage and publications
- The buoy data have been used in several scientific studies and by PhD researchers.
- Example publications:
  - Woolway, R.I., Maberly S.C., Jones, I.D., Feuchtmayr, H. (2014) A novel method for estimating the onset of thermal stratification in lakes from surface water measurements. Water Resources Research, 50(6), 5131-5140
  - Woolway, R.I., Jones, I.D., Feuchtmayr, H., Maberly S.C. (2015) A comparison of the diel variability in epilimnetic temperature for five lakes in the English Lake District. Inland Waters, 5, 139-154
  - Woolway et al. (2016) Diel surface temperature range scales with lake size. PLoS ONE, 11(3): e0152466

## Considerations for data support work
- Treat the dataset as raw data requiring calibration/quality control before extensive analysis.
- Cleaning steps may include:
  - Calibration of sensors (air temperature, water temperature at multiple depths, solar radiation, wind speed)
  - Handling gaps due to maintenance (document and potentially impute or flag missing periods)
  - Validation against known events or supplementary data sources
- Potential data products:
  - Time-series dashboards showing temperature profiles by depth and surface conditions
  - Summaries of stratification onset and diel temperature ranges
  - Self-serve exports for end users with depth-resolved temperature and meteorological context
- Ensure clear documentation of time semantics (GMT, hourly averaging method) for reproducibility.