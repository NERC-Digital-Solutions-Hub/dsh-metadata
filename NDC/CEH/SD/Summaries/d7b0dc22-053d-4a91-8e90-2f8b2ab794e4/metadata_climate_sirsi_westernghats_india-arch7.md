# Climate data, Sirsi, Feb 2021 - April 2022

- Overview
  - High-resolution climate measurements near a forest fragment in Sirsi, Western Ghats, India, collected between February 2021 and April 2022.
  - Location details: latitude 14.49 N, longitude 74.75 E, altitude 538 m.
  - Instrument: Watchdog Weather Station installed about 2 m above ground with no nearby trees or buildings.
  - Data format: CSV file with variables ordered in columns.

- Collection method
  - Measurements taken in an open space near a forest fragment.
  - Timeframe: February 2021 to April 2022.
  - Data are intended for use in GIS-style analyses and map-based visualisations.

- Data structure and variables
  - Columns include:
    - Date (DD/MM/YYYY)
    - Time (HH:MM)
    - RH_% (Relative Humidity, %)
    - AirTemp_degC (Air Temperature, °C)
    - Precip_mm/10mins (Precipitation, mm per 10 minutes)
    - WindDir_deg (Wind Direction, degrees)
    - WindGust_km/hr (Wind Gust, km/h)
    - DewPoint_DegC (Dew Point, °C)

- Units and explanations
  - Date: sampling date
  - Time: sampling time
  - RH_%: relative humidity percentage
  - AirTemp_degC: air temperature in degrees Celsius
  - Precip_mm/10mins: precipitation amount per 10-minute interval
  - WindDir_deg: wind direction in degrees
  - WindGust_km/hr: wind gust speed in kilometers per hour
  - DewPoint_DegC: dew point in degrees Celsius

- Quality control and data corrections
  - Data were checked by the project team.
  - Relative humidity sensor exhibited an offset of approximately 5% in autumn 2021.
  - Offset corrected using a low-pass filter on daily maxima (nighttime) and adding the difference to 100% RH.

- GIS-relevant considerations
  - Single measurement site with precise coordinates and altitude allows linking to spatial basemaps; can be integrated with other GIS layers to study climate-landscape interactions near the forest fragment.
  - Data enable temporal visualisations (time series) of temperature, humidity, precipitation, wind direction/gust, and dew point at high temporal resolution.
  - Users should account for the RH correction and potential residual uncertainty post-correction when performing spatial analyses or model calibrations.