# Quarry Rain gauge

## Summary
- A 0.2 mm tipping bucket rain gauge (RG2) at the Quarry, Tyn y Bryn Farm, has a long-running maintenance and data-quality log from 2005–2009.
- The record shows frequent operational issues (flooding, blockages, sensor/tiny tag failures, timestamp drift) and significant data quality concerns (discrepancies between tipping bucket and storage gauge, dodgy months, and possible short circuits).
- Numerous maintenance actions were performed to address reliability and accuracy, including cleaning, rebalancing, component replacements, and drainage improvements.
- The notes illustrate challenges in maintaining a small-precision rain-gauge dataset within an open-field environment, with implications for data provenance, validation, and governance.

## Data System and Measurements
- Instrumentation: 0.2 mm tipping bucket rain gauge with a storage gauge adjacent; data logged by a logger with a tinytag sensor.
- Observations cover both measurement integrity and timing (e.g., logger timing drift by ~52 minutes on 03/10/06).
- Cross-checks mentioned between tipping bucket data and storage gauge readings (noting notable divergences).

## Key Data Quality Issues Observed
- 2005: Pit flooding around installation; funnel blockages and recurring blockages.
- 05/11/05: Tiny tag failure; replacement on 30/11/05.
- Feb 2006: Large discrepancy between tipping bucket and adjacent storage gauge (189.2 mm vs 92.5 mm); questioned data quality.
- 24/03/06: Test after dodgy February data; rainfall test showed discrepancies; report of possible short circuit during a flood event affecting readings.
- 02/08/2006–03/10/2006: Data downloaded and cleaned; logger time drift noted.
- Feb 2007: February data dodgy due to significant snowfall.
- 01/03/2007: Storage gauge recorded far higher rainfall (499 mm); leaf collector gauze missing; blockage issues observed in TB gauge.
- 06/03/2007 and 03/04/2007: TB gauge blocked; discrepancies between TB and storage gauge; suspected corrosion and submersion of connections; drainage issues suspected.
- 12/04/2007: Potential TB measurement problem; pit drainage concerns; drainage channel considered.
- 17/04/2007: TB hole cleaned; 30/04/2007: battery, seal, desiccant replaced.
- 29/01/2008–01/04/2008: Repeated TB blockages and cleaning; timestamps and timing issues noted.
- 12/06/2008: Rebalanced TB gauge; 03/11/2008: timestamp problems recur.
- 02/12/2008 and 26/10/2009: Additional blockages and data integrity concerns.

## Maintenance and Interventions
- Regular cleaning and debris removal from the TB funnel and connections.
- Rebalancing of the tipping bucket and adjustments to drainage around the gauge pit.
- Replacements of components:
  - Tiny tag replacements (05/11/2005; 30/11/2005).
  - Leaf collector gauze replacement (01/03/2007).
  - Battery, seal, and desiccant changes (30/04/2007; 29/01/2008; 01/04/2008).
- Drainage improvements to prevent submersion and improve drainage around the measurement pit (e.g., digging drainage channel; spiking surrounding soil; drainage drainage adjustments).
- Tests to verify system integrity:
  - 24/03/2006: 1 L test and manual tip-count to verify logger recordings.
  - Timely integrity checks when data appeared dodgy or when floods occurred.

## Data Quality outcomes and Gaps
- Persistent gaps and questionable months (notably February 2006, February 2007).
- Recurrent discrepancies between tipping bucket readings and the storage gauge (occasional large differences; potential short circuits or submersion effects).
- Timestamp drift and occasional logger corrections indicating reliability concerns for time-series analyses.
- Snow events and wind-related measurement losses impacting data capture.

## Lessons for Data Leaders
- Importance of data provenance and cross-validation: compare tipping bucket data with a storage gauge to flag anomalies.
- Need for robust timestamping and synchronization to ensure temporal alignment of observations.
- Field maintenance and environmental mitigation (drainage, moisture control) directly affect data quality.
- Regular, documented calibration tests (e.g., controlled water additions, known-volume tests) are essential to validate measurement integrity.
- Clear data quality flags and metadata are critical when data quality is compromised or uncertain.

## Recommendations for Data Leadership
- Implement formal data quality controls and automated flags for:
  - Timestamp drift
  - Large between-gauge discrepancies
  - Frequent blockages or sensor failures
  - Missing leaf/collection components
- Maintain comprehensive maintenance-and-operations logs tied to data records for traceability.
- Integrate redundancy checks by cross-validating tipping bucket data with an adjacent storage gauge or independent sensor.
- Establish preventative maintenance and drainage management to minimize data loss from flooding and submersion.
- Develop standardized data validation procedures (e.g., periodic 1 L or calibration tests; routine checks following extreme weather).
- Document metadata clearly (sensor IDs, calibration, replacement dates, data corrections) to support data discoverability and reuse.