# AWS Calibration and Maintenance Log (2006-2009)

- Overview
  - Chronological field log of an Automatic Weather Station (AWS) covering calibrations, maintenance, sensor issues, and data quality notes from 2006 to 2009.
  - Documents multiple sensors and data streams: soil temperature probes, air temperature, humidity, net radiometer, pyronometer, wind (direction and speed), anemometer, solarimeter, and logger equipment.
  - Emphasizes data provenance, calibration adjustments, and the impact of field problems on data quality and GIS-ready datasets.

- Sensors, data streams, and mounting
  - Soil temperature probes (depths including 5 cm and 10 cm)
  - Air temperature and humidity sensors (including later Vaisala HMP installation)
  - Net Radiometer (Net Rad) and solar-related measurements
  - Pyronometer (solar radiation) and solarimeter
  - Wind measurements: wind direction, wind speed, anemometer
  - Power/battery status and logger status
  - Sensor heights above ground recorded (e.g., Net Radiometer ~1575 mm, Humidity/Temp probe ~1475 mm, Wind vane ~2395 mm, Anemometer ~2500 mm, Solarimeter ~2867.5 mm)

- Calibration, adjustments, and data corrections
  - 21/09/06–10/11/06: Noted soil temperature readings; calibration adjustments proposed for various sensors (e.g., soil temp offset corrections and air temperature adjustments) with some retrospective implications.
  - 16/11/06–28/11/06: Net radiometer inspection; new logger installed; pyronometer recalibration noted.
  - 03/01/07–08/03/07: Mechanical issues (anemometer screw loss; shaft angle corrections); re-routing and re-seating soil probes; program/channel wiring conflicts resolved (Net Rad vs humidity channel).
  - 19/03/07–01/05/07: Temperature issues resolved; multiple program updates to correct readings.
  - 19/07/07–24/07/07: Net Rad misalignment (angled readings) due to structural issues; damaged net radiometer replaced; guy ropes tightened.
  - 2007–2009: Ongoing calibration checks for air, soil temperatures, and net rad; periodic adjustments to sensor offsets and channel mappings; issues with data continuity and sensor stability noted.
  - 03/06/09–04/06/09: Installation of a new net radiometer with updated multiplication factor (113.77) and AWS reprogramming (AWS_03_JUNE); preparation for additional net rad installations across six channels.

- Data quality issues and data gaps
  - Recurrent data gaps and potential data loss periods:
    - 28/04/08–05/05/08: data lost during calibration/maintenance window.
    - 6–12 January (year not explicit but within log): data loss suspected due to battery/solar recharge behavior.
    - 15:00–12:00 on occasions where sensor maintenance occurred (e.g., 11:00–12:00 removal events).
  - Sensor anomalies caused by physical damage or misconfiguration:
    - Net Rad readings intermittently misread due to misalignment, channel conflicts, and later physical damage.
    - Sheep-chewed wiring affecting wind-related readings; corrective actions included re-installation and soldering of wires.
  - Calibration and agreement issues:
    - Air temperature, soil temperature, and pyronometer readings showed drift or offset that required recalibration and, in some cases, retrospective adjustments (e.g., offset corrections and proposed data adjustments like adding 4.034 C to prior soil temp data, and applying a slope-intercept correction for soil temperature).

- Data handling implications for GIS and data products
  - Data lineage and versioning: numerous sensor replacements, recalibrations, and program updates necessitate robust metadata to trace versions of datasets.
  The following should be captured for GIS-ready products:
  - Calibration offsets, channel mappings, and any retrospective adjustments.
  - Dates of sensor maintenance, replacements, and reprogramming events.
  - Data gaps and reasons (maintenance, hardware failure, environmental interruption).
  - Sensor mounting heights and positions (for accurate spatial representation and comparisons across time).
  - Quality flags indicating data integrity (e.g., post-maintenance periods, known anomalies, and corrected values).

- Notable end-state events relevant to GIS data products
  - 04/06/09: New net radiometer installed with AWS reprogrammed for AWS_03_JUNE; six channels updated to align with the new radiometer.
  - 03/06/09–04/06/09: Preparatory and installation activities for further net radiometer updates; data collection schedule adjusted accordingly.

- Recommendations for GIS-focused data products
  - Include comprehensive metadata with:
    - Sensor types, mounting heights, and locations.
    - All calibration offsets, transformation equations, and retrospective adjustment notes.
    - Channel mappings between sensors (e.g., Net Rad vs Humidity/Temp channels) and any changes over time.
    - Data quality flags and documented data gaps with their causes.
  - Maintain versioned time-series data to reflect sensor upgrades and recalibrations.
  - Provide data cleaning workflows documenting steps taken to correct readings (offsets, slope adjustments, and unit conversions).
  - When presenting map-based visuals, clearly indicate periods with known data quality issues or missing data to avoid misinterpretation.