# AWS Calibration and Maintenance Log (2006-2009)

- Overview
  - A detailed log of calibration, maintenance, and data quality issues at an Automatic Weather Station (AWS) measuring soil temperature, air temperature, humidity, net radiometer, pyronometer, wind, and related sensors.
  - Documents frequent recalibrations, program updates, sensor replacements, and physical realignments to ensure data accuracy.
  - Highlights the ongoing need to verify data against calibration standards, adjust historical data when necessary, and maintain clear documentation of changes.

- Key calibration and maintenance actions (by chronology)
  - 2006
    - Soil temperature checks and calibration corrections; air temperature offset adjustments; humidity data flagged as potentially inaccurate but not corrected; Pyronometer and net radiometer readings deemed sensible but not verifiable without calibration kit.
    - Net radiometer and sensor health checked; new logger installed later in the year; several reconfigurations to fix channel wiring issues.
    - Mechanical issues addressed: anemometer screw loss caused misalignment; wind-related sensor maintenance performed.
  - 2007
    - Regular maintenance and recalibrations; net radiometer positioned and aligned; some readings previously misrepresented due to channel conflicts corrected by updating the program.
    - Bundle of tasks including reinstallation/recalibration of Pyronometer and soil temperature probes; data continuity efforts observed but with occasional data gaps.
    - June 2007: multiple notes about installing a new net radiometer and reprogramming; continuing attention to data integrity.
  - 2008
    - Air temperature offset refined (+0.234 C) based on calibration checks; instructions to adjust previous data by a substantial amount (e.g., +4.034 C) to align with calibrated values.
    - Soil temperature probe recalibration and reinstallation at 10 cm depth; calibration checks against calibrated probes performed; later data gaps observed (e.g., 28/04/08–05/05/08).
    - Transition toward new instrumentation: installation and testing of Vaisala humidity/temperature probe; ongoing AWS reprogramming and channel realignment efforts.
  - 2009
    - Replacement of the net radiometer with a new unit; AWS reprogrammed with a new configuration (AWS_03_JUNE).
    - Data gaps noted (e.g., 6–12 January); continued attention to ensuring data continuity and accuracy during sensor transitions.
    - By June 2009, six net radiometer entries indicate a coordinated update and reprogramming across multiple channels.

- Data quality, metadata, and governance notes
  - Frequent need to document offsets, calibration dates, methods, and resulting data corrections to maintain traceable data provenance.
  - Several instances of past data needing retrospective adjustment due to refined calibration offsets or corrected instrumentation measurements.
  - Channel wiring conflicts and programmatic misconfigurations highlight the necessity of robust data lineage and version-controlled configurations.
  - Data gaps caused by sensor damage, power/charging limitations, and data logging interruptions underscored the importance of metadata on data loss events and recovery actions.
  - Some calibration verifications required specialized equipment (calibration kit), underscoring the dependency on external standards for data quality assurance.

- Implications for monitoring frameworks
  - The log exemplifies how calibration and maintenance records underpin data quality assessments used in evaluating policy and informing decisions.
  - Highlights the need for:
    - Comprehensive, time-stamped calibration logs and data correction notes.
    - Clear metadata on sensor configurations, channel mappings, offsets, and calibration methods.
    - Data governance practices that enable traceability, openness of underlying data, and versioned corrections.
    - Coordination to minimize data gaps and document any losses or outages along with recovery steps.

- Conclusion
  - The document provides a concrete view of the practical challenges in maintaining environmental monitoring data quality over several years, emphasizing systematic calibration, transparent metadata, and governance practices essential for effective monitoring frameworks.