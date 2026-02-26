# LLYN HIR RAIN GAUGE READ ME DOCUMENT

## Purpose and Scope
- A maintenance and data integrity log for the Llyn Hir storage and tipping bucket rain gauges, documenting installation, temperature and timestamp-related issues, and corrective actions affecting the data record.

## Timeline of Key Events
- 28/09/07: Storage and tipping bucket rain gauges installed.
- 29/11/07 (around 10:55): Wind caused tipping bucket to tip once; base of storage gauge found full of water.
- 30/05/08: Accidental tips of the tipping bucket (TB) rain gauge identified; these tips should be ignored.
- 03/11/08: Time stamp issue suspected; assumed incorrect time stamp; adjusted to follow immediately after the last record from the previous download.
- 27/01/09: Disparity between TB and storage gauge >13%; likely due to freezing conditions; ice present in TB bucket and removed.
- 06/04/09: Time stamp issue suspected due to GMT to BST change; accounted for in the analysed data file.

## Data Quality and Metadata
- Time stamp discrepancies between downloads and between sensors (TB vs storage gauge).
- Anomalies potentially caused by weather conditions (ice in TB bucket) affecting measurements.
- Need to distinguish genuine rainfall records from accidental tips and timestamp adjustments.
- Metadata gaps can hinder verification of data quality and require clear documentation of corrections.

## Data Processing and Corrections
- Ignore identified accidental TB tips.
- Adjust time stamps when discrepancies are detected, maintaining logical sequence with prior records.
- Document and apply corrections (e.g., GMT to BST shift) within the analysed data file.
- Remove ice-related anomalies (ice in TB bucket) and note its impact on disparity.

## Implications for Monitoring Frameworks
- Demonstrates the necessity of robust data provenance: recording installation, maintenance actions, and all data corrections.
- Highlights the importance of metadata quality, including time standards, sensor types, and environmental conditions.
- Underlines challenges in aligning data from multiple sensors (TB vs storage gauge) and across DST transitions.
- Emphasizes keeping an audit trail of decisions to ignore, adjust, or remove data points.

## Recommendations for Monitoring Practice (based on the log)
- Enforce explicit, consistent timekeeping (prefer UTC) and clearly document DST handling.
- Maintain detailed maintenance logs tied to data records to explain anomalies (e.g., ice in a bucket, wind events).
- Implement data flags for dubious records (accidental tips, timestamp anomalies) and track corrective actions.
- Ensure data files include annotations for corrections (timestamps adjustments, data exclusions) with rationale.
- Improve metadata completeness (sensor types, installation dates, calibration status) to enable easier verification and data reuse.