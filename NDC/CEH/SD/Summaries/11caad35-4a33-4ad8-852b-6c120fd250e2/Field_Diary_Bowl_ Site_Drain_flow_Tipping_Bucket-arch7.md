# Drain flow data log and tipping bucket events

- This document is a chronological log of drain flow measurement activities, focusing on tipping bucket (TB) systems, weir boxes, transducers, and calibration events from 2005 to 2009. It records interval settings, maintenance, data quality notes, and adjustments applied to measurement data, with attention to data exclusions during calibrations and sensor issues.

## Key changes and events

- 22/02/05: Recording interval changed from 10 minutes to 5 minutes to align with overland flow trap.
- 09/11/05 – 01/02/06: Indications of incomplete drain flow to TB and physical issues (track from drain emerges; icicle blocking TB; TB bolt issue affecting tipping quantity).
- 23/02/06 – 11/04/06: TB removed for testing; weir box installed for drain flow measurement; transducer alignment problems noted (water inside logger box; need improved mounting).
- 21/04/06 – 29/06/06: Weir/tb connections recalibrated; some data marked as invalid (e.g., “Last 3 entries from drain flow data incorrect – no tips”).
- 05/07/06: TBs calibrated; specific time window (13:30–14:30) ignored during calibration.
- 02/08/06 – 21/08/06: Weather-related TB activity; battery failures in weir boxes; weir box/TB connections repaired.
- 31/10/08 – 31/10/08: Time stamp issue suspected; later data flagged as resolved.
- 14/11/08 – 17/11/08: Weir box calibration conducted; TB cleaning; calibration adjustments documented; note of growing gunk in TB necessitating cleaning.
- 07/01/09 – 07/01/09: System frozen.
- 20/02/09 – 25/02/09: Pipe removal for zero-flow determination; pipe reinstalled; subsequent data adjustments noted (DST/GMT considerations).
- 04/06/09 – 15/07/09: Periods where drain inflow pipe not properly reinstalled; data from this period marked as not suitable; later re-installations and corrections followed.

## Calibration and tipping bucket specifics

- Early calibration (07/06/07): 30 L through TB produced 10 tips with 0.9 L remaining; concluded tip volume ≈ 2.91 L per tip.
- Later calibration (14/11/08): 30.04 L produced 11 tips; tip volume ≈ 2.79 L per tip.
- 15/08/07: Magnet replacement on TB; tipping accuracy subsequently improved.
- 17/11/08: A linear incremental adjustment to TB tip volume applied to reconcile differences between the 07/06/07 and 14/11/08 calibrations, effectively treating the change as a gradual update over six months.

## Data quality, exclusions, and processing notes

- Data flagged as unreliable or to be ignored during calibration events (e.g., 21/04/06, 05/07/06).
- Transducer-related issues documented (misalignment, water ingress, tube seating) with corrective actions.
- Time stamp and DST issues documented (GMT vs BST) with explicit notes on accounting for these in analysis (e.g., 04/09/2009 period adjustments).
- Data gaps and unusable periods identified (e.g., system freeze, TB dislodgements, calibration periods, and pipe re-installation intervals).
- Occasional data cleaning actions include: discarding data during calibration windows, ignoring certain tips, and re-calibrating TB volume to maintain consistency.

## Implications for GIS data products

- The dataset contains multiple calibration events, maintenance periods, and DST/time zone adjustments that affect temporal alignment and tipping-bucket-derived flow calculations.
- Users should:
  - Incorporate calibration and maintenance events as metadata flags that mark data segments as calibrated, adjusted, or excluded.
  - Apply TB tip-volume corrections (2.91 L initially, to be updated to 2.79 L after 14/11/08) and account for the linear adjustment period noted in 17/11/08.
  - Treat data around DST/GMT transitions with caution and ensure consistent time standard across the dataset.
  - Exclude data during documented invalid periods (e.g., “ignore tips” windows, weir box recalibrations, and periods with TB or pipe installation issues).
  - Document sensor and hardware issues (weir boxes, TB magnet, transducer mounting) to inform future data quality assessments.

## Practical takeaways for GIS analysts

- Build a metadata layer capturing:
  - Calibration events and their effect on tip volume.
  - Time period flags for data confidence (calibration, maintenance, DST issues, and data exclusions).
  - Equipment issues and their remediation (TB magnet, mounting, weir box maintenance, battery changes).
- When generating map-based visualizations, consider layering data by quality flag and annotation of calibration events to aid end-user interpretation.
- Ensure consistent temporal resolution (5-minute interval) and standardize time references across the dataset, applying DST corrections where appropriate.

## End notes

- The log provides a comprehensive record of operational challenges, calibrations, and corrective actions that influence the reliability and interpretation of drain flow measurements for GIS-based analysis and visualization.