# Soil moisture data, Sirsi, Western Ghats

- Overview
  - Measurements of soil moisture profile near trees on a farm near Sirsi, Karnataka, Western Ghats, India.
  - Time period: January 2020 to January 2022.
  - Depths measured: 10 cm, 25 cm, 50 cm, and 110 cm.

- Location and Collection Method
  - Location: Sirsi, Western Ghats (latitude 14.49 N, longitude 74.75 E; altitude 538 m).
  - Sensor: Campbell CS616 Water Content Reflectometers.
  - Installation context: On a gentle slope approximately 500 m from the local valley bottom.
  - Depths surveyed: 10 cm, 25 cm, 50 cm, 110 cm.

- Data Details
  - Data structure: Variables arranged as columns in a CSV file; missing data indicated as NaN (Not A Number).
  - Date and time formats: Date as DD/MM/YY; Time as HH:MM:SS.
  - Recorded variables and units:
    - SM_m3/m3_at10cm_depth: soil moisture at 10 cm depth (m3/m3).
    - SM_m3/m3_at25cm_depth: soil moisture at 25 cm depth (m3/m3).
    - SM_m3/m3_at50cm_depth: soil moisture at 50 cm depth (m3/m3).
    - SM_m3/m3_at110cm_depth: soil moisture at 110 cm depth (m3/m3).

- Data Quality and Limitations
  - Quality control: Data were quality checked by the project team.
  - Calibration: Sensors were not independently calibrated using soils from this site, which may affect absolute accuracy.

- Considerations for Monitoring Frameworks
  - Useful for assessing vertical soil moisture profiles across depths and over time.
  - Gaps in data indicated by NaN; data consistency relies on future calibration and possibly validation with site-specific soils.
  - Metadata includes location, depth, and instrument details to support data governance and traceability.