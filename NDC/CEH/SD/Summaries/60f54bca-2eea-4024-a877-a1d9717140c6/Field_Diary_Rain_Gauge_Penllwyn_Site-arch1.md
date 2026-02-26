# Penllwyn Rain gauge read me document

## Summary
- Rain gauge installed on 25/01/2006; ongoing data quality issues noted throughout 2006–2007.
- Key events affecting data:
  - 03/10/2006: last reading 1349 when laptop showed 1441 GMT; approximately 52 minutes out; reset performed.
  - Feb/2007: data considered dodgy due to heavy snowfall and wind blowing snow off the gauge, potentially under-recording precipitation.
  - 30/04/2007: battery, seal, and desiccant replaced on the Tinytag.
  - 31/10/2007 and 30/11/2007: wind blew the tipping bucket, causing readings to be unreliable at the indicated times (11:20 and 10:36, respectively; water present in the bucket in the latter event).
  - 22/12/2007: period of about 8 hours with impossibly high readings; possible cold-related effects; bowl weirboxes also had a problem during this time.
  - 03/11/2007: time-stamp issue with overlap from the previous download; time assumed incorrect and adjusted to follow immediately after the last record from the prior download; adjustments documented in the Excel file.
- The document serves as a log of installation, maintenance, data anomalies, and data corrections.

## Timeline of events and issues
- 25/01/2006: Rain gauge installed.
- 03/10/2006: Last reading discrepancy (1349 vs 1441 GMT); ~52 minutes out; reset performed.
- Feb/2007: Data quality concerns due to heavy snow and wind; snow blown off gauge affecting record integrity.
- 30/04/2007: Battery, seal, and desiccant replaced on Tinytag.
- 31/10/2007: Wind blew tipping bucket (11:20) disrupting readings.
- 30/11/2007: Wind blew tipping bucket (10:36); some water in bucket noted.
- 22/12/2007: ~8 hours with impossibly high readings; cold-related effects suspected; bowl weirboxes problem observed.
- 03/11/2007: Time-stamp overlap detected; time adjusted to follow previous download; corrections noted in Excel file.

## Data quality and instrument issues
- Time alignment problems: occasional mismatches between gauge readings and laptop time; required resets and post-hoc corrections.
- Environmental interference: wind events causing tipping bucket misreads; snow affecting precipitation capture; cold temperatures potentially causing anomalous high readings.
- Equipment-related issues: battery, seals, desiccants maintenance; Tinytag and tipping bucket mechanics susceptible to wind and weather.
- Data anomalies: periods with impossibly high readings; bowl weirbox issues contributing to data unreliability.
- Metadata gaps: corrections and adjustments are documented separately (Excel file) to maintain traceability.

## Data handling and corrections
- Corrective actions documented in the dataset:
  - Time stamps adjusted where misalignment was identified (e.g., 03/11/07 issue).
  - Corrections verified against prior records and subsequent data sequences; adjustments reflected in the Excel file.
- Maintenance log maintained to support data quality and reproducibility:
  - Battery, seal, and desiccant replacements recorded (30/04/2007).
- Purpose of corrections: ensure chronologically consistent time series and improve data reliability for subsequent analysis.

## Implications for analysis
- Expect gaps and anomalies in the time series due to environmental and mechanical factors.
- Necessity to flag or remove periods affected by wind disturbances, snow effects, or implausible readings (e.g., 22/12/2007).
- Time-stamp corrections mean provenance and traceability are essential; ensure metadata accompanies any analyses.
- Ongoing maintenance and data cleaning are important to maintain data quality for model development or trend analysis.