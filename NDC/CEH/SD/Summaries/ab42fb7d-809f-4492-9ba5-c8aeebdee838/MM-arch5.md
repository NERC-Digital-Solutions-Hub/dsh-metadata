# MM Protocol

## Purpose and Scope
- Establish standard meteorological observations following British Meteorological Office (BMO) protocols.
- Preserve continuity of historic ECN data and provide calibration/back-up for ECN automatic weather stations.
- Ensure data from standard instruments are collected at defined cadences and are suitable for reuse and integration with ECN data holdings.

## Data Standards and Governance
- Instruments and methods must meet BMO standards; where applicable, thermometers may be certified to BSI standards.
- Data are associated with ECN sites and must be recorded and stored in a consistent, interoperable format.
- Data management and transfer are governed by ECN’s data management practices, including coordination with the ECN Data Manager and adherence to data transfer documentation.

## Data Collection, Instruments, and Site Layout
- Each ECN site uses a defined array of standard meteorological instruments (e.g., Stevenson screen, dry/wet bulb thermometers, maximum/minimum/grass minimum thermometers, soil thermometers at 30 cm and 100 cm, Octapent raingauge Mk2A, run-of-wind counter).
- The manual station should be co-located with the AWS where possible; existing Meteorological Office Climatological Stations may be accepted if not adjacent to the ECN weather station.
- Readings are conducted weekly, with daily readings for existing BMO Climatological Stations.

## Data Recording, Scheduling, and Submission
- Readings are conducted on a fixed schedule: weekly measurements at 0900 GMT; daily measurements at 0900 GMT for climatological stations.
- For ECN sites, daily data plus a monthly data sheet (as submitted to the BMO) must be sent to the ECN Data Manager, in addition to agreed machine-readable data.
- Any quality-control queries from BMO should be reported to the ECN Data Manager.
- Where available, additional data (sunshine hours, snow depth, soil temperatures for non-ECN purposes) should also be forwarded to the ECN Data Manager.

## Data Formats, Metadata, and Identifiers
- Data must include four primary identifiers for each sampling occasion:
  - Site Identification Code (unique to each ECN Site)
  - Core Measurement Code (e.g., MM)
  - Location Code (represents sampling point)
  - Recording Date/Time (date and time with appropriate precision; GMT 24-h clock)
- Core measurement: meteorology - manual (MM Protocol).
- Variables recorded daily at 0900 GMT include:
  - Dry bulb temperature (°C)
  - Wet bulb temperature (°C)
  - Maximum temperature (°C)
  - Minimum temperature (°C)
  - Grass minimum temperature (°C)
  - Soil temperature 30 cm (°C)
  - Soil temperature 100 cm (°C)
  - Rainfall total (mm)
  - Wind run total (km)
- Data recording conventions specify units, precision, and time, with guidance to refer to Data Transfer documentation for ECN dataset formats.

## Data Transfer, Access, and Documentation
- ECN dataset formats and transfer specifications are documented in the restricted-access Site Managers’ extranet (Data Transfer documentation).
- Access to these documents requires contacting the ECN Data Manager or ecnccu@ceh.ac.uk.
- Recording forms: use the standard British Meteorological Office recording form 3208B and instruction booklet 3100A; refer to the Meteorological Office Handbook (1982).

## Roles and Contacts
- Data submission and quality control involve coordination with the ECN Data Manager.
- Data management and QC queries from BMO are to be directed to the ECN Data Manager.

## References
- Meteorological Office, Observers’ Handbook (1982), 4th edition.
- Recording forms: Met Office Metform 3208B; instruction booklet 3100A.