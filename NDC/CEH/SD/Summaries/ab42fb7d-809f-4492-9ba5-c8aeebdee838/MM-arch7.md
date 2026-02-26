# MM Protocol

## Aim
- Standardize meteorological observations according to British Meteorological Office (BMO) protocols.
- Preserve continuity of historic data and provide calibration/back-up for ECN automatic weather stations (AWS).

## Rationale
- ECN sites hold historic data collected to meet Meteorological Office criteria; standardization helps maintain long-term datasets.
- Ensures calibration and data backup through a consistent suite of standard instruments.

## Equipment and Site Requirements
- Large Stevenson screen with iron stand.
- Dry and wet bulb thermometers (±0.1°C).
- Maximum and minimum thermometers (±0.1°C).
- Grass minimum thermometer (±0.1°C).
- Soil thermometers at 30 cm and 100 cm (±0.1°C).
- Octapent raingauge, BMO pattern Mk2A.
- Run-of-wind counter anemometer (to BMO spec unless an additional anemometer is available with AWS).
- Temperature thermometers may be certified to BSI standards by the supplier where applicable.

## Location
- Manual station should be sited alongside the AWS if possible.
- If there is an existing Meteorological Office Climatological Station, proximity to the TSS/AWS may not be necessary.

## Operation and Procedures
- Follow methods in the Observers' handbook (Meteorological Office 1982) and BMO standards.
- For ECN purposes, instruments are periodically field-calibrated by BMO personnel (for Climatological Stations).
- Readings:
  - Weekly ECN stations: Wednesdays at 0900 GMT.
  - Existing BMO Climatological Stations: daily at 0900 GMT.
  - If applicable, submit sunshine hours, snow depth, and soil temperatures (for non-ECN purposes) to the ECN Data Manager.
- Time and cadence:
  - 1 hour per month for weekly sites (specifics in protocol).
- Data management:
  - Any QA queries raised by BMO should be reported to the ECN Data Manager.

## Data Recording, Conventions, and Formats
- Core data variables collected daily at 0900 GMT:
  - Dry bulb temperature (°C)
  - Wet bulb temperature (°C)
  - Maximum temperature (°C)
  - Minimum temperature (°C)
  - Grass minimum temperature (°C)
  - Soil temperature 30 cm (°C)
  - Soil temperature 100 cm (°C)
  - Rainfall total (mm)
  - Wind run total (km)
- Recording specifics:
  - Recording time: GMT 24-hour clock.
  - Recording precision: generally 1 minute for time; specified decimal precision for each measurement (e.g., 0.1 for temperatures, 0.1 for rainfall, 1 for wind run, etc.).
  - Units and precision per variable are defined in the protocol.
- Metadata keys that identify every sample/record:
  - Site Identification Code (unique ECN site code, e.g., T05)
  - Core Measurement Code (e.g., PC for core meteorology)
  - Location Code (e.g., 01 for sampling location)
  - Sampling Date/Time (with time if sampling more frequently than daily)
- Data specifications and transfer:
  - ECNCCU data transfer documentation defines dataset formats for ECN data submissions.
  - Access to this documentation is via the restricted-site Managers’ extranet; contact ecnccu@ceh.ac.uk for access.
  
## Recording Forms and References
- Use the standard British Meteorological Office recording form 3208B with instruction booklet 3100A.
- Refer to the Meteorological Office Handbook (1982) for procedures.

## Data Access and Contact
- Data submitted to the ECN Data Manager with additional machine-readable data for daily/weekly observations.
- Any BMO quality-control queries directed to the ECN Data Manager.
- If additional weather variables are recorded for non-ECN purposes, these should also be transmitted to the ECN Data Manager.