# Quarry Rain gauge

- A 0.2 mm tipping bucket rain gauge located at ground level at the Quarry, Tyn y Bryn Farm (RG2).

## Overview
- Purpose: record rainfall; notes document operational status, data quality, and maintenance actions over time.
- Frequent interactions between the tipping bucket (TB) gauge and an adjacent storage gauge, used for cross-checks and quality assessment.

## Data quality and reliability observations
- Data quality often compromised by environmental and mechanical issues:
  - Pit flooding and water in the system, occasionally not affecting the TB mechanism but prompting maintenance.
  - Blocked collection funnel or TB components leading to under- or over-recorded rainfall.
  - TinyTag (tiny tag sensor) failures requiring replacements.
  - Timestamp irregularities and logger time drift affecting data alignment.
  - Snow events causing dodgy data (e.g., Feb 2007).
- Discrepancies between TB and adjacent storage gauge readings reported (e.g., Feb 2006: storage 92.5 mm vs TB 189.2 mm; question around data quality for February).
- Data quality issues often followed by targeted checks or maintenance to verify system integrity (see validation and maintenance sections).

## Notable incidents and anomalies (selected)
- 31/03/05: Flooding of the pit but not affecting tipping bucket mechanism.
- 24/06/05, 05/11/05: Blocked/flooded funnel; tiny tag failure necessitated replacement.
- Feb 2006: Data quality questioned due to large discrepancy between storage and TB readings.
- 24/03/06: System test conducted; initial data flagged as dodgy; short-duration test suggested possible short-circuiting when the pit was flooded.
- 03/10/06: Last record time drift (logger time offset ~52 minutes); logger reset; TB funnel cleaned.
- Feb 2007: Snow-related data issues; data described as dodgy.
- 01/03/07: Storage gauge read 499 mm; leaf collector gauze lost.
- 06/03/07: TB gauge blocked and water-filled; rusty connection likely from submersion; drainage issues suspected; leaf collector issues.
- 03/04/07: Large TB vs storage discrepancy; rusted connection noted; drainage considerations discussed.
- 12/04/07 & 17/04/07: Indications of ongoing problems with TB; drainage improvements implemented.
- 30/04/07: Battery, seal, and desiccant updated on tinytag.
- 29/01/08, 01/04/08: Recurrent blockages (TB) and soil blockage linked to windy conditions.
- 12/06/08: TB rebalanced; drainage improvements attempted.
- 03/11/08, 02/12/08: Timestamp problems re-emerge; 02/12/08 notes TB blockage and data quality concerns; partial data may be unreliable after blockage.

## Validation, checks, and cross-referencing
- Cross-validation with adjacent storage gauge used to assess TB data quality.
- Targeted tests to verify system (e.g., 1 L input and counting tips) to confirm logger responsiveness.
- Regular data quality assessments triggered by anomalies (e.g., February 2006, February/March 2007) and subsequent maintenance.

## Maintenance actions implemented
- Sensor and component replacements: tiny tag replacement, battery/seal/desiccant changes.
- Mechanical cleaning and refurbishment: clearing blockages, cleaning TB funnel, improving drainage channels.
- Structural adjustments: drainage channel creation and soil spiking to enhance drainage; hole cleaning and repairs.
- Calibration/adjustment: TB rebalancing (e.g., 02/08/06, 12/06/08) to ensure consistent tipping.
- Leaf collector handling: leaf collector gauze replacement and related fixes.
- Timestamp corrections: addressing logger time drift and ensuring accurate timestamps.

## Implications for data use and best practices
- Data from this gauge is subject to periodic quality issues tied to environmental conditions (flooding, blockage, snow) and equipment integrity (tinytag, wiring, rust).
- Regular cross-checks with adjacent storage gauge data are essential to identify and correct anomalies.
- Documentation of maintenance events is crucial for interpreting data quality and potential biases in rainfall estimates.
- Future data analyses should account for periods of known blockage, timestamp drift, or sensor replacements, and consider flagging data segments with suspected reliability issues.