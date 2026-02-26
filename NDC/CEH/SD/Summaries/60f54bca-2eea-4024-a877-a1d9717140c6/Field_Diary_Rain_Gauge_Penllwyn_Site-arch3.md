# Penllwyn Rain gauge read me document

## Overview
- A maintenance and data quality log for the Penllwyn rain gauge, documenting installation, maintenance actions, data issues, and timestamp adjustments intended to ensure reliable monitoring data.

## Timeline of key events
- 25/01/06: Rain gauge installed.
- 03/10/06: Last reading discrepancy (Pen RG 1349 vs laptop 1441 GMT); ~52 minutes out; reset.
- Feb/07: Data deemed dodgy due to significant snow; difficulty recording wind-blown snow.
- 30/04/07: Battery, seal, and desiccant replaced.
- 31/10/07: Wind blew tipping bucket at 11:20.
- 30/11/07: Wind blew tipping bucket at 10:36 (some water present in bucket).
- 22/12/07: Period of about 8 hours with impossibly high readings; possible cold-related effect; bowl weirboxes also had issues.
- 03/11/07: Time stamp overlap with previous download; time adjusted to follow last record; corrections noted in the Excel file.

## Data quality issues observed
- Time discrepancies and clock drift between device and data logger.
- Snow and cold weather affecting measurement accuracy.
- Wind causing physical disturbance of the tipping bucket, producing erroneous readings.
- Impossibly high readings during a cold period, with potential issues in ancillary components (bowl weirboxes).
- Time stamp overlaps between downloads requiring post-hoc adjustments.

## Actions and handling
- Resetting measurements when out of sync.
- Replacing batteries and seals; routine maintenance to maintain data integrity.
- Logging and noting issues to guide corrections.
- Adjusting time stamps after downloads and recording these adjustments in the data file (Excel).

## Implications for monitoring frameworks (relevant insights for authors)
- Importance of detailed instrument maintenance logs to support data quality assessments.
- Need for clear metadata on calibration, battery/seal replacements, and environmental disturbances.
- Criticality of timestamp integrity and cross-download alignment; require documented corrections and versioning.
- Environmental interference (wind, snow, cold) must be anticipated and accounted for in data processing and interpretation.
- Data governance considerations: transparency about data adjustments, provenance, and reliability to enable policy scrutiny and future decision-making.

## Practical takeaways for monitoring practice
- Embed instrument maintenance and calibration records within datasets.
- Implement robust timestamp synchronization and keep audit trails of any corrections.
- Develop protocols to flag and adjust data affected by environmental disturbances.
- Ensure metadata is sufficient to verify whether data meet required standards and to support reproducible analyses.