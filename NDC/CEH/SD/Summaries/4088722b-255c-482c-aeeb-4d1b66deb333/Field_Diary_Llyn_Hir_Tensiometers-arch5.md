# Llyn Hir tensiometes

## Overview
- A maintenance and data-logging log for a tension measurement device at Llyn Hir, detailing timestamps, adjustments, maintenance actions, and data quality issues observed between 2008 and 2009.

## Data provenance and timestamps
- 16/10/08: Data downloaded; downloaded time shown as 1 = Downloaded from tensios; logger time reads 14/10/08 00:17, suggesting potential need to adjust dataset timestamps.
- 25/11/08: Offset corrected from -4.8 to 0 on the logger; note indicates original offset was -4.8 cm H2O and data were adjusted to account for this.
- 28/11/08: Correction documented again; offset should be +4.8 cm H2O, data adjusted accordingly.

## Data Corrections and Processing
- Offsets and calibration:
  - Original offset -4.8 cm H2O corrected to +4.8 cm H2O; dataset adjustments applied to reflect this.
- Data preparation:
  - Degassed tensio data after download to ensure cleaner measurements.
  - Indicated removal or reduction of gas-related artifacts post-download.
- Sampling schedule changes:
  - 02/09/09: Time sampling interval changed from 10 minutes to 15 minutes to reduce site visitation frequency (targeting monthly visits).

## Operational Issues and Maintenance
- 31/07/09: Logger failed to respond; batteries replaced but no response.
- 12/08/09: Tension logger stopped logging; required reset and restart.
- 03/07/09: Irregular blips appeared in data at unpredictable times, causing data loss around those periods; suspected logger issue; data stops earlier than expected (26/08 instead of 02/09).

## Data Quality, Gaps, and Integrity
- Noted irregular blips and data losses around early July 2009, likely due to logger issues rather than environmental factors.
- Data stops earlier than planned, indicating interruptions in continuous logging.
- Multiple maintenance events (offset corrections, degassing, battery changes, restarts) influence data consistency and require thorough metadata to document these changes.

## Data Governance, Documentation, and Accessibility
- This log serves as a metadata record of data processing steps, calibration changes, and hardware issues.
- Highlights the need for explicit documentation of:
  - Calibration/offset changes and their impact on historical data.
  - Data cleaning steps (degassing) and rationale.
  - Equipment health and maintenance events (battery changes, resets, restarts).
  - Known data gaps and their causes to inform users and data catalogs.

## Implications for Data Stewards
- Timeliness and completeness are at risk due to logger reliability and infrequent maintenance.
- Accurate metadata is essential to interpret corrected offsets, sampling changes, and gaps.
- When sharing or cataloging datasets, include comprehensive notes on:
  - Timestamp alignment issues between logger and downloads.
  - All calibration adjustments and how they were applied.
  - Any data cleaning steps (e.g., degassing) and their effects on measurements.
  - Maintenance events that may affect data continuity and quality.

## Recommendations for Future Stewardship
- Maintain an explicit, versioned log of all calibrations, corrections, and maintenance actions.
- Ensure metadata includes:
  - Original vs. corrected offsets, with justification and method of adjustment.
  - Sampling interval changes and their effective dates.
  - Dates and causes of data gaps or interruptions, plus remediation steps taken.
- Implement routine checks for logger health and data continuity; establish alert thresholds for unexpected data patterns.
- Document environmental and operational context to support data reuse by others with clear expectations about data quality and limitations.