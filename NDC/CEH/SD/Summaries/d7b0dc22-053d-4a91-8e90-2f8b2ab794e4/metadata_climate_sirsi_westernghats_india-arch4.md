# Climate data, Sirsi, Feb 2021 - April 2022

## Overview
- High-resolution climate measurements near Sirsi, Western Ghats, India (latitude 14.49 N, longitude 74.75 E; altitude 538 m).
- Time period: February 2021 to April 2022.
- Collected in an open space close to a forest fragment; installed ~2 m above ground with no nearby trees or buildings.
- Instrument: Watchdog Weather Station.

## Data collection and provenance
- Data collected as environmental climate variables: air temperature, precipitation, relative humidity, wind speed, wind direction, and dew point.
- Data are organized in a CSV file with variables in columns.
- File name: Climate_Sirsi_WesternGhats.csv.

## Variables and units
- Date: sampling date in DD/MM/YYYY.
- Time: sampling time in HH:MM.
- RH_%: Relative Humidity (%).
- AirTemp_degC: Air Temperature (°C).
- Precip_mm/10mins: Precipitation (mm per 10 minutes).
- WindDir_deg: Wind Direction (degrees).
- WindGust_km/hr: Wind Gust (km/h).
- DewPoint_DegC: Dew Point (°C).

## Quality control and data corrections
- Data verified by the project team.
- Relative Humidity offset of about 5% observed in autumn 2021.
- Correction applied: low-pass filter to daily maxima (night) and added the difference to 100% RH.