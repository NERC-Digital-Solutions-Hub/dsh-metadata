# Rhos 1 Rain gauge read me document

## Summary
- This document is a maintenance and data integrity log for the Rhos 1 rain gauge and its Tinytag data logger, detailing calibration, rebalancing, timing issues, wiring problems, and data adjustments affecting recorded rainfall.
- It highlights how field issues (blockages, snow, wind) and equipment problems (time drift, wiring, battery/seal wear) impacted data quality and necessitated corrections and documentation.

## Timeline of maintenance and data issues
- 03/10/06: Rain gauge blocked; 21 mm collected, but aperture differences make this reading unreliable. Logger about 69 minutes behind actual time; reset performed. Gauge removed due to field unblocking issues.
- 12/10/06: Rebalanced using spirit level; reinstallation at ~09:20.
- Feb 2007: Rebalanced amid significant snowfall; data likely under-recorded due to wind-blown snow.
- 01/05/07: Battery, seal, and desiccant replaced on Tinytag.
- 01/04/08: Rebalanced; wiring issue where wire detached from Tinytag-to-reed-switch connection.
- 02/04/08: Rebalanced; cable between reed switch and Tinytag replaced; system working.
- 21/08/08: Rebalanced; calibration check period (14:25–14:44 GMT) disregarded for data (calibration ongoing); note about calibration-related data handling.
- 03/11/08: Rebalanced; prior month’s data deemed 5 minutes fast; data adjusted in Excel accordingly.

## Data quality and governance implications
- Time synchronization: consistent timekeeping is critical; a 69-minute drift required corrective action.
- Data gaps and reliability: snow, wind, and blockages create known data gaps or inaccuracies.
- Calibration effects: data during calibration windows may be unreliable and require flags or omissions.
- Transparency of corrections: adjustments (e.g., a 5-minute fix) were recorded in an external Excel document, underscoring the need for explicit provenance and audit trails.
- Metadata and accessibility: notes about aperture differences and calibration checks should be captured in metadata to support future data interpretation.
- Field-to-data lineage: maintenance events (battery/seal changes, wiring repairs, rebalancing) should be tied to data quality notes to trace potential causes of anomalies.

## Maintenance components and actions
- Equipment: rain gauge, Tinytag data logger, reed switch, wiring, battery, seal, desiccant.
- Actions: rebalancing with spirit level, time adjustments, replacement of damaged cable/wiring, battery/seal maintenance, and data adjustments to reflect corrected timestamps or readings.

## Recommendations for monitoring framework authors
- Ensure robust metadata to capture: sensor type, calibration times, time synchronization status, data quality flags, and any data adjustments with explicit rationales.
- Implement data provenance: log maintenance events and link them to corresponding data quality impacts.
- Establish clear data governance rules for: when to exclude data during calibration, how to flag unreliable periods, and how to document corrections (preferably within the dataset rather than external spreadsheets).
- Develop time-drift detection and correction workflows to prevent long-running timestamp errors.
- Create guidelines for documenting aperture-related measurement issues and their impact on comparability across gauges.
- Set maintenance schedules and thresholds for acceptable data gaps, with automated alerts for anomalies.