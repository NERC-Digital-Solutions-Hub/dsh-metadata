# MM Protocol

## Aim
- Establish standard meteorological observations per British Meteorological Office (BMO) protocols.
- Preserve continuity of historic ECN data and provide calibration/back-up for ECN automatic weather stations (AWS).
- Ensure weekly readings (and daily readings where applicable) and integrate data into ECN data management processes.

## Equipment and Method
- Standard instrument suite:
  - Large Stevenson screen with iron stand
  - Dry and wet bulb thermometers (±0.1°C)
  - Maximum and minimum thermometers (±0.1°C)
  - Grass minimum thermometer (±0.1°C)
  - Soil thermometers at 30 cm and 100 cm (±0.1°C)
  - Octapent raingauge, BMO pattern Mk2A
  - Run-of-wind counter anemometer (to BMO spec; alternative AWS may be present)
  - Thermometers may be certified to BSI standard by supplier where applicable
- Operation follows the Observers’ Handbook (Meteorological Office, 1982; BMO standards).
- Climatological Stations may involve periodic field calibration by BMO personnel.
- Readings:
  - Weekly measurements on Wednesdays at 0900 GMT (except existing BMO Climatological Stations with daily readings at 0900 GMT)
  - For ECN purposes, data submitted in machine-readable form along with the monthly data sheet
  - Any BMO quality control queries to ECN Data Manager
  - If sites already record sunshine hours, snow depth, and soil temperatures for non-ECN purposes, these should be sent to the ECN Data Manager

## Location
- Manual station should be sited alongside the AWS if possible.
- If an existing Meteorological Office Climatological Station is present, adjacency to the TSS/AWS may not be required.

## Data Specification and Recording Conventions
- Core data framework for ECN sampling locations (ECN Site metadata):
  - Site Identification Code (unique per ECN Site)
  - Core Measurement Code (e.g., PC)
  - Location Code (e.g., 01)
  - Recording Date/Time (with appropriate time precision)
- Core measurement: meteorology - manual (MM Protocol)
- Variables recorded daily at 0900 GMT:
  - Dry bulb temperature (°C)
  - Wet bulb temperature (°C)
  - Maximum temperature (°C)
  - Minimum temperature (°C)
  - Grass minimum temperature (°C)
  - Soil temperature at 30 cm (°C)
  - Soil temperature at 100 cm (°C)
  - Rainfall total (mm)
  - Wind run total (km)
- Each variable includes specified recording time (GMT 24-h clock) and precision (as listed in protocol)
- Data should conform to the ECN Data Transfer documentation for site submissions to ECNCCU (restricted extranet; contact ecnccu@ceh.ac.uk for access)

## Recording Forms
- Use the standard British Meteorological Office recording form 3208B for field recording
- Refer to instruction booklet 3100A
- Follow the Meteorological Office Handbook (1982)

## Data Management and Accessibility
- Data and metadata should be managed and submitted to ECN systems per the Data Transfer documentation
- Instrumentation calibration and quality control are aligned with BMO processes
- Documentation and data lineage are maintained to enable verification and reuse within ECN analyses