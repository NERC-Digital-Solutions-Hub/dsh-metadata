# Climate data, Sirsi, Feb 2021 - April 2022

- Overview
  - High-resolution climate measurements near a forest fragment in Sirsi, Western Ghats, India (approx. 14.49 N, 74.75 E; altitude 538 m) collected from February 2021 to April 2022.
  - Parameters recorded: air temperature, relative humidity, precipitation (mm per 10 minutes), wind direction, wind gust speed, and dew point.
  - Measurements taken in an open space with no nearby trees or buildings, approximately 2 m above ground.

- Collection and instrumentation
  - Instrument: Watchdog Weather Station.
  - Installation: placed ~2 m above ground with unobstructed surroundings.
  - Sampling context implied by variable list; precipitation reported in 10-minute intervals.

- Data structure and variables
  - File format: CSV with variables arranged in columns.
  - Key fields:
    - Date: DD/MM/YYYY
    - Time: HH:MM
    - RH_%: Relative humidity (%)
    - AirTemp_degC: Air temperature (°C)
    - Precip_mm/10mins: Precipitation in millimeters per 10 minutes
    - WindDir_deg: Wind direction (degrees)
    - WindGust_km/hr: Wind gust speed (km/h)
    - DewPoint_DegC: Dew point (°C)

- Units and metadata
  - Clear explanations for each variable’s name and unit.
  - Details included on data structure and formatting (e.g., date/time formats).

- Quality control and data correction
  - Data quality checks conducted by the project team.
  - Relative humidity sensor offset of about 5% observed in autumn 2021.
  - Correction applied: offset addressed using a low-pass filter on daily maxima (nighttime) and the difference added to 100% RH.

- Temporal and spatial coverage
  - Timeframe: February 2021 – April 2022.
  - Location: Sirsi, Western Ghats, India; near-forest open-space site.

- Implications for monitoring frameworks
  - Detailed metadata and variable explanations support usability for monitoring and evaluation.
  - Documented QA process and correction steps enhance data reliability for policy scrutiny and future decisions.
  - Recognition of data quality challenges (sensor offset, need for ongoing validation) aligns with governance needs to maintain up-to-date, trustworthy datasets.