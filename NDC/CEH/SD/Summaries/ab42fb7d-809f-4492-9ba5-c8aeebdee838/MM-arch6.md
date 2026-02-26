# MM Protocol

## Aim
- Establish standard meteorological observations per the British Meteorological Office (BMO) to preserve historic ECN data, provide calibration/back-up for ECN AWS, and support data management and analysis.

## Rationale
- Many ECN sites hold historic data; standardization ensures continuity, calibration backing, and robust data management for future analysis and cross-site comparisons.

## Equipment and Standards
- Large Stevenson screen with iron stand
- Dry and wet bulb thermometers (±0.1°C)
- Maximum and minimum thermometers (±0.1°C)
- Grass minimum thermometer (±0.1°C)
- Soil thermometers at 30 cm and 100 cm (±0.1°C)
- Octapent raingauge, BMO pattern Mk2A
- Run-of-wind counter anemometer (to BMO spec; or existing AWS alternative)
- Thermometers may be BS certified by supplier where applicable

## Location and Setup
- Manual station should be sited alongside the AWS if possible
- If an existing Meteorological Office Climatological Station is present, adjacency to the TSS/AWS may not be required

## Operation and Scheduling
- Methods follow the Observers’ Handbook (Meteorological Office 1982) and BMO standards
- For ECN purposes, instruments are read weekly on Wednesdays at 0900 GMT
- Existing BMO Climatological Stations continue daily readings at 0900 GMT
  - A monthly data sheet (as submitted to BMO, Metform 3208B) is sent to the ECN Data Manager in addition to the machine-readable data
- Any BMO quality control queries should be reported to the ECN Data Manager
- If sites already record sunshine hours, snow depth, or soil temperatures for non-ECN purposes, those data should also be sent to the ECN Data Manager

## Data Recording Conventions and Core Measurements
- Core identification fields needed in all datasets:
  - Site Identification Code (e.g., T05)
  - Core Measurement Code (e.g., PC)
  - Location Code (e.g., 01)
  - Sampling Date/Time (date with GMT time; time precision as required)
- Core measurement: meteorology – manual (MM Protocol)
- Daily measurements recorded at 0900 GMT:
  - Dry bulb temperature (°C)
  - Wet bulb temperature (°C)
  - Maximum temperature (°C)
  - Minimum temperature (°C)
  - Grass minimum temperature (°C)
  - Soil temperature 30 cm (°C)
  - Soil temperature 100 cm (°C)
  - Rainfall total (mm)
  - Wind run total (km)
- Units and recording precision specified for each variable

## Recording Forms and Documentation
- Use the standard British Meteorological Office recording form 3208B in the field
- Refer to instruction booklet 3100A and the Meteorological Office Handbook (1982)

## Data Transfer, Access, and Formats
- ECN site data submissions follow the accompanying Data Transfer documentation (ECNCCU)
- Data formats are defined for ECN datasets and are available on the restricted-access Site Managers’ extranet
- For access or documentation: contact ecnccu@ceh.ac.uk
- Daily monthly data (for climatological stations) and machine-readable data are coordinated with the ECN Data Manager

## Roles and Data Quality
- BMO personnel perform field calibration for climatological stations periodically
- ECN Data Manager handles data receipt, quality control feedback, and dissemination
- Queries arising from BMO quality control are communicated to the ECN Data Manager to ensure data integrity and consistency

## References
- Meteorological Office, Observers handbook, 4th edition (1982)
- Metform 3208B recording forms
- Data Transfer documentation (ECNCCU) and related ECN Data Manager procedures

## Contact
- ECN Data Manager: refer to ECN Data Transfer documentation
- For access to documentation: ecnccu@ceh.ac.uk