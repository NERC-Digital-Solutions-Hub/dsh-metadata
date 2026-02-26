# PennedSheepWithTags.csv

## Overview
- Dataset from a urine collection study with five Welsh Mountain ewes in urine collection pens.
- Ewes equipped with Daily Diary (DD) triaxial accelerometers measuring X, Y, Z acceleration at 40 Hz (12-bit resolution).
- Objective: determine if squatting duration during urination can predict urine volume per event.
- All urination events were detected by the algorithm with no false positives or negatives in this controlled setting.
- A linear relationship was found between squatting duration and urine volume, used to estimate volume in field deployments.

## Data Collection and Workflow
- Observations occur during feeding in pens; start time of urination squatting is recorded.
- Urine volume for each event is measured.
- DD tag data analyzed blind with an algorithm to determine squatting duration.
- The derived squatting duration is then used to estimate urine volume via the established linear relationship for field use.

## Data Headers and Variables
- Sheep_ID: identifier for each replicate sheep (1–5).
- Time: time of observed urination posture (hh:mm:ss).
- Date: date of the urination event (dd/mm/yyyy).
- SquatTime: squatting duration; described as identified by the algorithm (in seconds) with some documentation wording indicating a boolean, but used as duration here.
- MeasuredVol: actual urine volume per event (ml).
- EstimatedVol: urine volume estimated from squat time using the regression relationship (ml).

## Methodology Highlights
- Triaxial accelerometer data used to detect squatting posture during urination.
- Linear regression performed across all sheep to link SquatTime with MeasuredVol.
- The resulting equation used to estimate urine volume in field deployments based on squat time alone.

## Data Quality and Limitations
- Dataset size: n = 5 sheep, controlled pen environment.
- In controlled conditions, algorithm detected all events with no false positives or negatives.
- Limited generalizability to non-controlled environments; field applicability relies on the regression model.
- Documentation notes a potential inconsistency in how SquatTime is described (duration in seconds vs. boolean identifier) that should be clarified for automated processing.

## GIS and Visualization Opportunities
- Treat each urination event as a geolocated point (once spatial coordinates are available) with attributes:
  - Sheep_ID, Date, Time, SquatTime, MeasuredVol, EstimatedVol.
- Build a time-enabled event layer to analyze patterns over time (e.g., per sheep, per day).
- Integrate with other spatial data (pen layout, feeding areas) to study spatial-temporal behavior and resource use.
- Use EstimatedVol to generate thematic maps of urine volume events across sites or conditions.

## Reuse and Citation
- If data are reused, ensure full citation as indicated: “If data are reused please ensure it is fully cited.”
- Grant reference: NE/M015351/1.