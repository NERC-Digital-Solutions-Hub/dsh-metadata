# Climate data, Sirsi, Feb 2021 - April 2022

## Overview
- High-resolution climate measurements near Sirsi, Western Ghats, India.
- Variables recorded: air temperature, precipitation, relative humidity, wind speed, wind direction, and dew point.
- Timeframe: February 2021 to April 2022.
- Location: near Sirsi (latitude 14.49 N, longitude 74.75 E; altitude 538 m).
- Instrument setup: Watchdog Weather Station installed about 2 meters above ground in an open space near a forest fragment; no nearby trees or buildings affecting measurements.

## Data Collection Method
- Measurements taken in an open space adjacent to a forest fragment to capture local climate conditions.
- Instrument: Watchdog Weather Station.
- Sampling context: high-resolution measurements; precipitation recorded as mm per 10-minute intervals (Precip_mm/10mins). Other variables implied to be measured at standard high-resolution cadence.
- Height and placement chosen to minimize obstructions and ground influence.

## Data Structure and Variables
- Data stored in a CSV file with variables organized in columns.
- Date: format DD/MM/YYYY; Time: format HH:MM.
- Key variables:
  - RH_%: Relative Humidity (percent).
  - AirTemp_degC: Air Temperature (degrees Celsius).
  - Precip_mm/10mins: Precipitation (mm per 10 minutes).
  - WindDir_deg: Wind Direction (degrees).
  - WindGust_km/hr: Wind Gust (km/h).
  - DewPoint_DegC: Dew Point (degrees Celsius).

## Quality Control and Corrections
- Data were quality checked by the involved team.
- Relative humidity sensor showed an offset of about 5% in autumn 2021.
- Correction: offset adjustment applied using a low-pass filter on nightly daily maxima, with the difference added to RH readings to align with 100% RH at high humidity.
- This correction ensures more accurate representation of humidity during periods of high moisture.