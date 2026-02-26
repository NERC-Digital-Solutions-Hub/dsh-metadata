# Rhos1: Notes from field visits for tensiometers and OLF

## Overview
- Longitudinal field log from 2005–2009 recording tensiometer and overland flow (OLF) trap monitoring at Rhos1.
- Focus on data collection, sensor maintenance, calibration, data quality, and provenance to support usable datasets.
- Entries include operational events, data quality flags, maintenance actions, and notes on data reliability.

## Data Collected and Sensors Involved
- Instruments:
  - Tensiometers at multiple depths and plots (e.g., M1.1, M1.2, M1.3; 10 cm, 30 cm, 50 cm).
  - OLF traps with tipping buckets, float switches, and associated gutters/pits.
  - Delta T loggers, batteries, desiccants; tinytags for logging times/conditions.
- Data types:
  - Sensor readings from tensiometers (degassed, de-gassed, stability concerns).
  - Tipping bucket counts/recordings and calibration data.
  - Tinytag timestamps and log intervals.
  - Observations on pump operation, pit/water status, and gutter conditions.
- Location/identifiers:
  - plots (e.g., plot 1.1, plot 1.2, plot 1.3), rhos 1, and specific trap components.

## Data Quality, Provenance, and QC Processes
- Data quality flags and cautions:
  - Storms/electrical events causing non-sensible readings; data flagged as suspect.
  - Periods where “tips should be ignored” or data between certain times deemed unreliable (e.g., mornings on specific dates; multistage events around 14:30–15:00).
  - Recurrent issues with pumps, reed switches, float switches, and wiring leading to data gaps or false recordings.
- Maintenance and calibration actions:
  - Regular degassing and grass-cutting; desiccant changes; battery changes; desiccant replacement noted.
  - Recalibration of tipping buckets; adjustments for reed switch orientation and calibration sheets referenced.
  - Repairs to OLF components (gutters, covers), external battery installations, and installation tweaks to ensure data flows.
- Data cleaning/handling notes:
  - Explicit notes to disregard certain data during maintenance windows or when hardware issues were present (e.g., “ignore tips,” “data downloaded,” “calibration checks”).
  - Instances of data reconciliation after hardware fixes (e.g., recalibrations after reed switch corrections).
- Metadata and provenance cues:
  - Frequent explicit timestamps for actions (degassing, battery changes, recalibration, component replacements).
  - Serial numbers/locations documented (e.g., end-of-report listing M1.1, M1.2, M1.3 with corresponding depths and readings).
  - Documentation of work performed on datasets and specific plots, enabling audit trails and future QC.

## Data Management and Sharing Considerations
- Data availability and update protocols implied:
  - Ongoing field monitoring with periodic data downloads and updates; frequent maintenance suggests need for clear versioning and update schedules.
  - Notes emphasize ensuring data quality before sharing (e.g., data from problematic periods may be flagged or excluded).
- Metadata needs highlighted by the notes:
  - Necessity to capture device IDs, locations, depths, and calibration events.
  - Importance of including maintenance history, sensor failures, and justification for excluding or downgrading data segments.
- Documentation practices:
  - The logs themselves serve as an audit trail; best practice would be to convert these notes into structured metadata and QC flags within a dataset catalog or portal.

## Key Challenges and Recommendations for Data Stewards
- Challenges evidenced by the notes:
  - Incomplete picture of user needs and priorities may hinder timely, standardized data sharing.
  - Timely receipt of data and coordination with data creators for standards and metadata.
  - Intermittent data integrity due to multiple hardware faults across different systems and formats.
  - Large datasets with high maintenance demands and bespoke, non-interoperable fixes.
- Recommendations:
  - Implement structured QC metadata fields (flags for storm-related anomalies, ignored tip periods, calibration status, sensor health).
  - Maintain a formal audit log linked to each dataset version, including device IDs, locations, depths, and maintenance actions.
  - Standardize data formats and schemas across plots and devices to improve interoperability.
  - Establish clear data acceptance criteria and update procedures to handle interim data versus finalized QC’ed data.
  - Document provenance comprehensively to support discovery and reuse by data users and systems.

## End-state Observations and Takeaways
- The field notes capture a comprehensive history of hardware configurations, calibrations, and data quality decisions over several years.
- Final entries include detailed sensor serials and locations (e.g., M1.1, M1.2, M1.3 with depths and readings), illustrating an emphasis on traceability.
- The document underscores the importance of robust metadata, QC flags, and maintenance records to ensure the usability and discoverability of the datasets for future analysis.