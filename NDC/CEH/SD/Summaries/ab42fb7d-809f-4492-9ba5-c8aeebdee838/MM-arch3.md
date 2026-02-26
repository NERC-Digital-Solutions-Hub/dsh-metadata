# MM Protocol

- Aim
  - To conduct standard meteorological observations according to British Meteorological Office (BMO) protocols, providing continuity for historic ECN data and calibration/back-up for ECN automatic weather stations (AWS).

- Rationale
  - Maintain consistency with national records across ECN sites and ensure data continuity and back-up for AWS, with field calibration support from BMO where applicable.

- Equipment and Location
  - Instruments: Stevenson screen with iron stand, dry and wet bulb thermometers, maximum and minimum thermometers, grass minimum thermometer, soil thermometers at 30 cm and 100 cm, Octapent raingauge (BMO Mk2A), run-of-wind counter anemometer (to BMO spec unless an alternative is available), and BSI-certified thermometers where applicable.
  - Location: Manual stations should be sited alongside the AWS when possible; existing Meteorological Office Climatological Stations may be non-adjacent to the TSS/AWS.

- Operation
  - Methods follow the Observers’ Handbook (Meteorological Office 1982); instruments to BMO standards; BMO field calibration for climatological stations.
  - Readings: ECN stations (for ECN purposes) weekly on Wednesdays at 0900 GMT; existing BMO Climatological Stations perform daily readings at 0900 GMT.
  - Data handling: Monthly data sheets sent to the ECN Data Manager in addition to machine-readable data; any BMO quality-control queries reported to the ECN Data Manager.
  - Data sharing: If sites already record sunshine hours, snow depth, or soil temperatures for non-ECN purposes, these data should also be sent to the ECN Data Manager.

- Data Recording and Formats
  - Core identification: first four parameters to uniquely identify each sample/recording moment
    - Site Identification Code (e.g., T05)
    - Core Measurement Code (e.g., PC)
    - Location Code (e.g., 01)
    - Recording Date/Time (including time element when sampling frequency exceeds daily)
  - Core measurements (daily at 0900 GMT) and units:
    - Dry bulb temperature (°C)
    - Wet bulb temperature (°C)
    - Maximum temperature (°C)
    - Minimum temperature (°C)
    - Grass minimum temperature (°C)
    - Soil temperature 30 cm (°C)
    - Soil temperature 100 cm (°C)
    - Rainfall total (mm)
    - Wind run total (km)
  - Recording specifics: time in GMT (24-hour clock), precision for each variable (e.g., 0.1°C for temperatures; 0.1 mm for rainfall; 1 km for wind run).
  - Recording forms: Use the standard British Meteorological Office forms 3208B and instruction booklet 3100A; refer to the Meteorological Office Handbook (1982).

- Data Transfer and Governance
  - Data formats and transfer specifications are documented in the ECNCCU Data Transfer documentation (restricted Site Managers extranet); contact ecnccu@ceh.ac.uk for access.
  - Data management: ECN Data Manager receives data; BMO QA processes may generate queries that should be reported back to the Data Manager.
  - Data sharing and openness: underlying data should be shared with the ECN Data Manager as part of governance and quality assurance.

- Endnotes and Additional Context
  - For climatological stations, daily observations are maintained; non-ECN data already collected for other purposes should be shared with the ECN Data Manager when applicable.
  - Calibration and data quality rely on BMO field calibration and ongoing QA processes, with dataset formats and metadata standardized to support clear identification and downstream use.