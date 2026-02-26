# Climate data, Sirsi, Feb 2021 - April 2022

## Overview
- High-resolution climate measurements near Sirsi, Western Ghats, India.
- Coverage: February 2021 to April 2022.
- Measured variables include air temperature, precipitation, relative humidity, wind speed, wind direction, and dew point.
- Location specifics: latitude 14.49 N, longitude 74.75 E; altitude 538 m; data collected in an open space near a forest fragment.
- Instrument installed approximately 2 m above ground with no nearby trees or buildings.

## Collection method and site description
- Collected with a Watchdog Weather Station.
- Site characteristics: open area near forest fragment; installation height ~2 m above ground; minimal obstructions.

## Data structure and variables
- Data are stored in a CSV file with variables as columns.
- Date and Time formats:
  - Date: DD/MM/YYYY (date of sampling)
  - Time: HH:MM (time of sampling)
- Variables (with units and explanations):
  - RH_%: Relative humidity (%)
  - AirTemp_degC: Air temperature (°C)
  - Precip_mm/10mins: Precipitation (mm per 10 minutes)
  - WindDir_deg: Wind direction (degrees)
  - WindGust_km/hr: Wind gust speed (km/hr)
  - DewPoint_DegC: Dew point (°C)

## Quality control and data integrity
- Data quality checked by the team involved.
- Relative humidity sensor offset of approximately 5% observed in autumn 2021.
- Correction approach: applied a low-pass filter to daily maxima (night) and added the difference to 100% RH to adjust.