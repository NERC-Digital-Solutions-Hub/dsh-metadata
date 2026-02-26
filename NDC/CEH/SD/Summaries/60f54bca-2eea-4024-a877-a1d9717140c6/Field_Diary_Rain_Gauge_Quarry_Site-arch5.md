# Quarry Rain gauge

- Overview
  - Rain gauge: 0.2 mm tipping bucket gauge located at ground level at the Quarry (RG2).
  - Adjacent storage gauge used for cross-checking measurements.
  - Logs cover maintenance, calibration, data issues, and system checks from 2005 onward.

- Data quality observations and anomalies
  - 31/03/05 to 24/06/05: pit flooding occurred; water was bailed; funnel occasionally blocked; minor maintenance.
  - 05/11/05 onward: tiny tag failures; replacement on 30/11/05.
  - Feb 2006: storage gauge showed 92.5 mm vs tipping bucket 189.2 mm, raising questions about data quality for February.
  - Mar 2006: test on 24/03/06 after dodgy February data; 1 L test yielded correct tip count, but subsequent period showed questionable values; pit flooding noted and potential short-circuiting when submerged.
  - 04/05/06: additional questionable results; investigation planned.
  - 02/08/06 onward: data downloaded and cleaned; storage gauge reading noted.
  - Feb 2007: significant snow noted; data timing issues suspected.
  - 01/03/07: storage gauge read 499 mm; leaf collector gauze lost; 06/03/07 TB gauge blocked and water-filled; corrective actions included replacing the leaf collector and addressing water contact at connections (stone placed to raise above water).
  - 03/04/07 and 12/04/07: large discrepancies between TB and storage gauges; rusty connection suspected; drainage improvements suggested and implemented (drainage channel considerations).
  - 17/04/07: drainage cleaning to improve drainage and prevent submersion.
  - 30/04/07: battery, seal, and desiccant replacement; TB-related issues persist.
  - 01/04/08 and 02/12/08: TB blocked by soil or debris; data impacted; partial clearing performed.
  - 12/06/08: rebalancing performed; 26/10/09: TB blocked again; data quality concerns for preceding period noted; partial measurement recorded.
  - Throughout: occasional timestamp drift (e.g., last record in one session read 1000 GMT but actual was later); logs reference checking RG2.xls for details.

- Maintenance actions and data handling
  - Regular cleaning, recalibration, and rebalancing of TB gauge and storage gauge.
  - Replacements: tiny tags, leaf collector, batteries, seals, desiccants.
  - Drainage improvements: identifying and mitigating submersion risks; digging or enhancing drainage channels; stabilizing sensor connections to prevent short circuits.
  - Data validation efforts: cross-checks between TB and storage gauges; 1 L water tests to verify tip counts; logging of anomalies and times when data appeared dodgy.
  - Timestamp issues: occurrences of clock drift; manual resets or calibrations of the logger to realign time.

- Data governance implications for Data Stewards
  - Data integrity risks due to frequent blockages, flooding, timestamp drift, and discrepancies between TB and storage gauges.
  - Requirement for thorough metadata about sensor status, maintenance events, and data quality flags.
  - Necessity to document calibration and maintenance actions to support provenance and reproducibility.
  - Importance of timely data transfers and reconciliation between field logs and central datasets (references to RG2.xls for details).

- Recommendations for ongoing stewardship
  - Implement automated data quality checks to flag TB/storage gauge mismatches and timestamp drift.
  - Standardize metadata schema for sensor status, anomalies, maintenance performed, and outcomes.
  - Establish a formal maintenance log template with fields for date, issue, action, and data impact.
  - Ensure robust drainage protection and regular inspections to minimize data loss due to flooding or blockages.
  - Align timekeeping across loggers and implement periodic synchronization to prevent timestamp issues.