# MM Protocol

- Purpose and rationale
  - Conduct standard meteorological observations following British Meteorological Office (BMO) protocols.
  - Preserve historic ECN data continuity and provide calibration/back-up for ECN automatic weather stations (AWS).
  - Ensure data from ECN sites are collected consistently to support long-term records.

- Data governance and stewardship
  - Data are collected and managed to high standard, with instruments calibrated to BMO/BSI specifications.
  - BMO quality control processes may raise queries; such queries should be reported to the ECN Data Manager.
  - Data submissions (including any additional variables like sunshine hours, snow depth, soil temperatures if recorded for non-ECN purposes) are sent to the ECN Data Manager; data formats and transfer procedures are documented in restricted extranet resources (Data Transfer documentation) and ECNCCU guidance.
  - Access to dataset formats and documentation requires appropriate authorization (ecnccu@ceh.ac.uk).

- Data model and core schema
  - Core identifiers required for every sample/record:
    - Site Identification Code (e.g., T05)
    - Core Measurement Code (e.g., PC)
    - Location Code (e.g., 01)
    - Sampling Date/Time (with precise time as needed)
  - Data recorded daily at 0900 GMT; some stations record daily data (including sunshine, snow depth, soil temperatures) and monthly/monthly-like data for others.
  - Core measurement category: meteorology – manual (MM Protocol).

- Observations, timing, and variables
  - Weekly manual observations at 0900 GMT (except where daily recording is norm for existing BMO Climatological Stations).
  - Recorded variables (units and precision specified):
    - Dry bulb temperature (°C)
    - Wet bulb temperature (°C)
    - Maximum temperature (°C)
    - Minimum temperature (°C)
    - Grass minimum temperature (°C)
    - Soil temperature 30 cm (°C) and 100 cm (°C)
    - Rainfall total (mm)
    - Wind run total (km)
  - Time of recording: 0900 GMT; data entries include precise recording time to a 1-minute or specified precision.

- Equipment and site setup
  - Standard meteorological instrumentation per BMO specifications, including:
    - Large Stevenson screen with iron stand
    - Dry and wet bulb thermometers, maximum/minimum thermometers, grass minimum thermometer
    - Soil thermometers at 30 cm and 100 cm
    - Octapent raingauge (BMO Mk2A)
    - Run-of-wind counter anemometer (to BMO specification)
  - Where available, installation alongside an AWS; if a Meteorological Office Climatological Station exists, daily recording may be used.
  - Calibration: BMO field calibration; where appropriate, thermometers certified to BSI standards by suppliers.

- Recording forms and documentation
  - Use standard British Meteorological Office recording form 3208B and instruction booklet 3100A.
  - Refer to the Meteorological Office Handbook (1982) for methodologies.
  - Data transfer and dataset format specifications are provided in ECNCCU-related documentation and restricted extranet resources; contact ECN Data Manager for access.

- Data submission, quality control, and follow-up
  - For ECN data, a monthly data sheet submission to BMO is expected for certain stations, with copies sent to the ECN Data Manager.
  - Any BMO quality control queries should be reported back to the ECN Data Manager.
  - If sites already collect additional variables (sunshine, snow depth, soil temperatures) for non-ECN purposes, those data should also be forwarded to the ECN Data Manager.

- Stakeholders and access
  - ECN Data Manager responsible for data integrity, management, and liaison with BMO.
  - Data formats and transfer procedures are accessible via restricted extranet; ecnccu@ceh.ac.uk handles access requests.