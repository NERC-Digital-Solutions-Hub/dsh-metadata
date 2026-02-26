# Drain flow data log

## Overview
- A detailed, timestamped log of drain flow measurements using a tipping bucket (TB) system, including equipment setup, calibration, maintenance, and data quality notes.
- The dataset records changes to recording intervals (from 10-minute to 5-minute), events affecting data integrity, and numerous calibration and repair activities.
- Annotations indicate when data should be ignored or treated with caution (e.g., during calibration, transducer issues, or hardware faults).

## Data collection and instrumentation
- Equipment:
  - Tipping bucket system with a magnet, reed switch, and axle; transducer logger box; weir boxes for drain flow measurement; TinyTag battery and desiccant.
- Recording intervals:
  - Initial interval reset from 10-minute to 5-minute; occasional adjustments noted.
- Calibration and measurement specifics:
  - Calibrations conducted (e.g., 07/06/07: pouring ~30 L to obtain 11 tips; tips ~2.91 L each).
  - Noted adjustments to tip volume over time (linear incremental change after 6 months).
  - Periodic calibration readings and data corrections following cleaning or reconfiguration.
- Data handling and quality controls:
  - Data discarded or flagged during calibration, after sensor issues, or when buckets/tubes were not properly aligned.
  - Corrections for time stamps when GMT/BST changes occurred.
  - Instances of gunk buildup, bucket dislodgements, and leaks addressed through reinstallation and cleaning.
- Maintenance and issues:
  - Battery failures, weir box and TB connection repairs, magnet reattachment, waterproofing adjustments, and sensor reinstallation.
  - Occasional detection of “ignore” periods during calibration, reinstallation, or transient anomalies.

## Data quality and processing notes
- Data exclusions:
  - Multiple periods explicitly marked to be ignored due to calibration, reconfiguration, or sensor problems.
  - Anomalous readings during calibration or when equipment was not functioning correctly.
- Time alignment and corrections:
  - Documented time stamp issues and corrections (particularly GMT to BST transitions).
- Calibration and data correction:
  - TB tip volume recalibrations and the application of a linear incremental adjustment to account for differences between calibration events.
  - Recalibration events redefined the basis for converting tips to volume (e.g., 30 L → 11 tips, 2.79–2.91 L per tip range).
- Data integrity notes:
  - Clear records of when data are considered invalid (e.g., “drain not flowing,” TB misalignment, or leaks).
  - Regular data downloads and device checks (weir box cleaning, sediment removal) to maintain data quality.

## Data governance implications
- Provenance and auditability:
  - Extensive maintenance and calibration logs enable traceability of data quality, sensor changes, and data exclusions.
  - Metadata should capture all calibration events, device replacements, time zone adjustments, and data exclusions to support reproducibility.
- Metadata requirements:
  - Include device identifiers, calibration dates and methods, tip volume per calibration, time zone handling, and periods to ignore.
- Data availability and stewardship:
  - Regular updates and clear flags for data validity aid discoverability and appropriate reuse.
  - Documentation of anomalies and corrections improves transparency for data users and downstream analyses.

## Key events chronology (highlights)
- 22/02/05: Time interval reset to 5-minute intervals.
- 09/11/05 – 01/02/06: Evidence of incomplete drainage or flow anomalies; icicle formation affecting TB tipping.
- 17/02/06 – 23/02/06: TB mechanical issues (bolt), testing period.
- 11/04/06 – 21/04/06: Weir box installed; calibration-related data adjustments and setup notes.
- 29/06/06 – 21/08/06: Data downloaded; weir box/bucket issues and battery failures addressed; system restarted.
- 03/10/06 – 05/10/06: Interval reset; early signs of high drain flow events relative to TB capacity.
- 07/06/07: Calibration check with 30 L → 11 tips; magnet dislodgement noted and repaired (08/2007).
- 19/02/08 – 12/06/08: Multiple maintenance events; PT checks and weir box work.
- 24/10/08 – 31/10/08 – 14/11/08: Weir box calibrations, data diversion for calibration; significant recalibration notes.
- 07/01/09 – 25/02/09: System freeze (01/2009); pipe reinstallation and timestamp adjustments (BST/GMT).
- 22/04/09 – 29/04/09 – 10/06/09 – 15/07/09: Cleaning, anomaly notes, data periods to ignore; TB reinstallation and final suitability statement.
- 15/07/09: Data considered suitable for use; additional minor adjustments noted.

## Gaps, issues, and recommendations
- Gaps and reliability:
  - Recurrent calibration events, sensor replacements, and periods of ignored data introduce discontinuities; careful metadata is required to maintain continuity.
- Timekeeping:
  - GPT/BST transitions necessitate explicit timestamps and consistent time zone handling to ensure accurate temporal analyses.
- Data quality management:
  - Maintain a separate calibration log as part of dataset metadata; document the exact TB tip volume at each calibration and any linear adjustments applied later.
- Recommendations for future stewardship:
  - Attach a comprehensive provenance file to the dataset detailing all hardware changes, calibration events, ignored data intervals, and anomaly conditions.
  - Provide a standardized flagging scheme for data points affected by calibration, sensor fault, or maintenance to facilitate downstream analyses.
  - Ensure ongoing monitoring of equipment (magnet integrity, battery health, leaks) and automate logging of maintenance events to improve data discoverability and reuse.