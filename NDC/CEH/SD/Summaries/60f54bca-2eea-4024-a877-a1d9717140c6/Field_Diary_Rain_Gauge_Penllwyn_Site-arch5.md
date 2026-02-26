# Penllwyn Rain gauge read me document

## Overview
- Log of installation, data issues, maintenance, and adjustments related to the Penllwyn rain gauge using a Tinytag data logger.
- Highlights data quality challenges, timestamp alignment problems, instrument disturbances, and manual corrections noted in an accompanying Excel file.

## Timeline of data issues and maintenance
- 25/01/06: Rain gauge installed.
- 03/10/06: Time drift observed (Pen RG last reading 1349 vs laptop 1441 GMT; ~52 minutes out); reset performed.
- Feb/07: Data deemed dodgy due to snow and wind blowing snow off the gauge, likely causing under-recording.
- 30/04/07: Battery, seal, and desiccant on Tinytag replaced.
- 31/10/07: Wind blew tipping bucket during reading (11:20).
- 30/11/07: Wind blew tipping bucket (10:36); some water present in bucket.
- 22/12/07: Period of ~8 hours with improbably high tipping bucket readings; possible cold-related effects and issues with bowl weirboxes.
- 03/11/07: Time stamp overlap with previous download; time assumed incorrect and adjusted to follow on from last record; adjustment documented in Excel file.

## Data quality and governance implications
- Time stamp accuracy and synchronization issues impacting data integrity.
- External conditions (wind, snow, extreme cold) causing measurement disturbances and outliers.
- Occurrence of data anomalies (impossibly high readings) requiring careful assessment.
- Maintenance events (battery, seals, desiccant) can affect data continuity and quality.
- Corrections and adjustments are currently documented separately (Excel) rather than embedded in the primary data or metadata.
- Need for clear provenance, audit trails, and explicit notes on which data have been corrected or flagged.

## Metadata and provenance recommendations for data stewards
- Capture detailed instrument metadata:
  - Instrument type (Tinytag), sensor specifics, units, site details.
  - Installation and calibration dates.
  - Data logger settings and time zones.
- Maintain comprehensive maintenance logs:
  - Dates and actions (battery/seal/desiccant replacement, repairs).
  - Any environmental disturbances observed (wind events, icing, freezing conditions).
- Document data corrections and adjustments:
  - Original vs corrected timestamps, rationale, and method (e.g., manual alignment, corrected in Excel).
  - Versioned records and links to correction notes.
- Implement explicit data quality flags:
  - Flags for timestamp drift, suspected sensor interference, missing periods, and anomalous spikes.
  - Exposure of caveats for periods affected by maintenance or adverse weather.
- Ensure data sharing readiness:
  - Include a data quality summary in dataset metadata.
  - Provide guidance on data suitability for analyses (e.g., rainfall sums with caveats for flagged periods).

## Actionable recommendations for data sharing and future reliability
- Implement automated timestamp synchronization checks between device time and standard time (GMT/UTC).
- Establish a formal QA workflow to flag and annotate irregular readings and time stamp issues in the primary dataset.
- Move anomaly and correction documentation into the dataset metadata to preserve provenance (avoid reliance on separate Excel files).
- Schedule regular maintenance and record‑keeping to minimize future data gaps and ensure timely data delivery.
- Consider implementing redundant logging or cross-checks during known problematic conditions (high wind, icing) to improve data reliability.
- Create a data user guide detailing known issues, flags, and recommended treatment of questionable data periods.