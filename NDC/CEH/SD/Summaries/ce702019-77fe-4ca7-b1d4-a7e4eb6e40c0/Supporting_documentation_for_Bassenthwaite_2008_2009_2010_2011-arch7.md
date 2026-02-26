# Data from automatic water monitoring buoy from Bassenthwaite Lake 2008, 2009, 2010 and 2011. Jones, I., Feuchtmayr, H. (2017)

## Overview
- Lake: Bassenthwaite Lake, Cumbria, England
- Monitoring buoy carrying meteorological instruments and in-lake temperature sensors
- Measured variables: air temperature (°C), solar radiation flux (W/m²), wind speed (m/s), and lake water temperatures at multiple depths
- Data cadence: measurements every 4 minutes; hourly averages computed by a Campbell Scientific datalogger
- Timeframe: 2008–2011; all times in GMT
- Data type: raw (not yet calibrated or quality controlled); some obvious hardware errors removed; gaps due to buoy maintenance or sensor/logger issues

## Sampling regime and collection methods
- Instruments mounted on an automatic lake monitoring buoy
- Temperature sensors at depths: 1 m, 2 m, 3 m, 4 m, 5 m, 6 m, 8 m, 10 m, 12 m, 14 m, 16 m, 18 m (platinum resistance thermometers)
- Additional sensors: air temperature, pyranometer (solar radiation flux), wind speed
- Data processing: hourly averages derived from the 4-minute measurements

## Data quality and limitations
- Status: raw data not calibrated or quality controlled
- Visual checks performed; clearly erroneous data from hardware issues removed
- Data gaps explained by maintenance: February 2010, May 2011, July 2011
- Caution: for GIS analyses, may require calibration/verification and handling of gaps

## Data structure and metadata
- File format: comma-separated values (CSV)
- Columns include:
  - Date_GMT: date and time in GMT
  - Water_temperature at depths: 1m, 2m, 3m, 4m, 5m, 6m, 8m, 10m, 12m, 14m, 16m, 18m
  - Air_Temperature (°C)
  - Pyranometer (Solar radiation, W/m²)
  - Wind_Speed (m/s)
- Hourly averaging rule example: value for 2 p.m. = average data from 1–2 p.m., excluding 1 p.m., including 2 p.m.
- Units: water and air temperatures in °C; solar radiation in W/m²; wind speed in m/s

## Data usage and GIS considerations
- Suitable for time-enabled (temporal) map visualizations and analysis of lake stratification, diurnal patterns, and depth-dependent temperature structure
- Recommended data transformation for GIS: convert to long format (Date_GMT, Depth_m, Water_Temperature_C) plus separate fields for Air_Temperature, Solar_Radiation, and Wind_Speed if needed
- Align with other datasets or models; address missing data and potential calibration needs
- Temporal resolution supports high-frequency time-series mapping and trend analysis across multiple depths

## Publications and context
- Used in ongoing scientific studies, including PhD research
- Related publications:
  - Woolway et al. (2014) on onset of thermal stratification from surface measurements (Water Resources Research)
  - Woolway et al. (2015) on diel variability in epilimnetic temperature (Inland Waters)
  - Woolway et al. (2016) on diel surface temperature range and lake size (PLOS ONE)

## Access and provenance
- Data provenance: collected by automatic buoy; published dataset with accompanying literature
- No licensing details provided in the text; refer to original publications for usage rights and data access notes