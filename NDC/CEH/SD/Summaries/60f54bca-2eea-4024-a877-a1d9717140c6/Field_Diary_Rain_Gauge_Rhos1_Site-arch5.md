# Rhos 1 Rain gauge read me document

## Overview
- Maintenance and data quality log for the Rhos1 rain gauge (timestamped notes from 2006–2008).
- Key focus: apparatus maintenance, data accuracy issues, timekeeping, and adjustments to recorded data.

## Data Quality and Measurement Issues
- Gauge blockage encountered (03/10/06); initial measurements affected by differing aperture sizes.
- Time drift: last sample 16:10 GMT vs laptop time 17:19 GMT; logger behind by ~69 minutes; led to a reset.
- In-field blockage issues prevented on-site unblocking; instrument removed to Bangor.
- Snow events (Feb 2007) caused unreliable data due to wind-removal of snow from the gauge.
- Calibration and data integrity concerns noted (14:25–14:44 GMT on 21/08/08; tip count noted as 400 during calibration).
- Data inaccuracy adjustments: last month’s data deemed 5 minutes fast and adjustments recorded in an Excel document.
- Aperture differences between gauges affect comparability of measurements (21 mm reading not directly comparable to others).

## Maintenance and Corrective Actions
- 03/10/06: Rebalanced with spirit level; gauge blocked; removal to Bangor.
- 12/10/06: Rebalanced and reinstalled (~09:20).
- Feb 2007: Noted data dodgy due to snow and wind effects.
- 01/05/07: Rebalanced; battery, seal, and desiccant on Tinytag replaced.
- 01/04/08: Rebalanced; Tinytag wiring issue discovered (wire disconnected from reed switch) after download; 02/04/08 fixed by replacing cable.
- 21/08/08: Rebalanced; calibration check led to disregard of tips 14:25–14:44 GMT.
- 03/11/08: Rebalanced; recognition that last month’s data were 5 minutes fast; corrections made in the Excel record.

## Data Provenance and Documentation
- Sequential maintenance notes tied to specific dates, with timestamps and actions.
- Data corrections and adjustments explicitly documented (e.g., time shifts, calibration notes) in an Excel document.
- Acknowledgement of non-interoperable issues (aperture differences) affecting cross-dataset comparability.

## Risks and Limitations
- Timeliness of data submission from field operations.
- Dependence on field personnel for block/unblock and rebalancing activities.
- Timekeeping drift and calibration uncertainties affecting data reliability.
- Hardware reliability issues (Tinytag wiring, reed switch connection) impacting data capture continuity.

## Recommendations for Data Stewards
- Ensure rigorous, auditable metadata for all maintenance and data corrections (include date, rationale, and method for each change).
- Implement precise time synchronization and log any clock drift with corresponding data adjustments; document in metadata.
- Record sensor-specific characteristics (e.g., aperture differences) and maintain versioned datasets to preserve comparability notes.
- Use robust, machine-readable formats for provenance and corrections (preferable to ad hoc Excel logs; consider CSV/JSON with embedded metadata).
- Maintain a formal data quality rubric that flags periods affected by blockage, snow effects, calibration events, or hardware issues.
- Establish a clear workflow for field data gaps and remediation, including when data should be considered untrustworthy and when corrections are accepted.
- Archive and reference all corrective actions to facilitate reproducibility and future audits.