# Climate data, Sirsi, Feb 2021 - April 2022

## Overview
- High-resolution climate measurements taken near a forest fragment close to Sirsi, Western Ghats, India.
- Timeframe: February 2021 to April 2022.
- Location coordinates: 14.49 N, 74.75 E; altitude: 538 m.
- Instrument: Watchdog Weather Station, installed about 2 m above ground with no trees or buildings nearby. Technical details available at the instrument vendor: https://www.industrialneeds.com/technical-data/weather-station-watchdog.htm

## Collection method
- Data comprise measurements of air temperature, precipitation, relative humidity, wind speed, wind direction, and dew point.
- Measured in an open space near a forest fragment.

## Data file and structure
- File name: Climate_Sirsi_WesternGhats.csv
- Structure: Variables are organized as columns in a CSV file.

## Variables and units
- Date: DD/MM/YYYY (date of sampling)
- Time: HH:MM (time of sampling)
- RH_%: Relative Humidity (%)
- AirTemp_degC: Air temperature (°C)
- Precip_mm/10mins: Precipitation (mm per 10 minutes)
- WindDir_deg: Wind direction (degrees)
- WindGust_km/hr: Wind gust speed (km/hr)
- DewPoint_DegC: Dew point (°C)

## Quality control
- Data were checked by the project team.
- Relative humidity offset of approximately 5% detected in autumn 2021; corrected by applying a low-pass filter to daily maxima (night) and adding the offset to 100% RH.