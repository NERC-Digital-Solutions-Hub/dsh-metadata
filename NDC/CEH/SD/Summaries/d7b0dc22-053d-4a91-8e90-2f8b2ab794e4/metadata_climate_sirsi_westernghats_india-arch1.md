# Climate data, Sirsi, Feb 2021 - April 2022

## Overview
- High-resolution climate measurements including air temperature, precipitation, relative humidity, wind speed, wind direction, and dew point.
- Collected in an open space near a forest fragment close to Sirsi, Western Ghats, India (latitude 14.49 N, longitude 74.75 E; altitude 538 m) between February 2021 and April 2022.
- Instrument: Watchdog Weather Station installed ~2 m above ground; no trees or buildings nearby.

## Data structure
- Data stored in a CSV file with variables arranged in columns.

## Variables and units
- Date: DD/MM/YYYY
- Time: HH:MM
- RH_%: Relative Humidity (%)
- AirTemp_degC: Air Temperature (°C)
- Precip_mm/10mins: Precipitation (mm per 10 minutes)
- WindDir_deg: Wind Direction (degrees)
- WindGust_km/hr: Wind Gust speed (km/h)
- DewPoint_DegC: Dew Point (°C)

(Note: Each variable has a corresponding explanation as described in the data documentation.)

## Quality control
- Data were checked by the team.
- Relative Humidity sensor showed an offset of approximately 5% in autumn 2021.
- Correction applied using a low-pass filter on nightly daily maxima and adding the difference to 100% relative humidity.