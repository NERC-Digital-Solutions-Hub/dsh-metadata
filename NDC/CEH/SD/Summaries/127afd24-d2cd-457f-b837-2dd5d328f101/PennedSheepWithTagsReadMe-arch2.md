# PennedSheepWithTags.csv

- Project: Uplands-N2O, Grant NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Harris, I.M., Mick J Whelan, Sophie Webb, Andrew J King, Rory P Wilson, Davey L Jones, Alice F Charteris, Laura M Cardenas, Dave R Chadwick
- Data purpose: Assess whether squatting duration during urination in sheep can predict urine volume per event; to support standardized environmental monitoring data practices.

## Data collection and methods

- Subjects: Five Welsh Mountain ewes housed in urine collection pens.
- Sensors: Daily Diary (DD) tri-axial accelerometers glued to a shorn hind area; measures acceleration along X (surge), Y (sway), Z (heave) at 40 Hz, 12-bit resolution (-8 to 8 g).
- Procedure: Feed delivered in pens; urination events observed with approximate start of squatting; urine volume for each event recorded.
- Analysis: Accelerometer data analyzed blind with a Boolean/ duration algorithm to identify squatting duration (SquatTime in seconds).
- Model: Linear regression between SquatTime and measured urine volume (MeasuredVol in ml); used to estimate urine volume (EstimatedVol in ml) from squat time for field deployments.
- Outcome: The algorithm detected all urine events with no false positives or negatives in this dataset.

## Data fields and units

- Sheep_ID: Identifier for each sheep (1–5).
- Time: Observation time of urination posture (hh:mm:ss).
- Date: Date of urination event (dd/mm/yyyy).
- SquatTime: Squatting duration identified by the algorithm (seconds).
- MeasuredVol: Actual urine volume per event (ml).
- EstimatedVol: Predicted urine volume from squat time (ml).

## Key findings

- A linear relationship exists between squatting duration and urine volume across all five sheep.
- The derived regression equation enables estimation of urine volume from squat time for field use.
- No false positives or negatives reported for urination events in the controlled dataset.

## Data reuse and accessibility

- Data described with clear headers and units; proper citation required if reused.
- Dataset supports standardized, reproducible analyses and can be integrated into broader monitoring efforts.

## Implications for environmental monitoring

- Demonstrates how behavioral accelerometer data can proxy an environmental-relevant biological process (urine production) that influences waste and nutrient flux.
- Provides a pathway to combine animal-behavioral data with environmental datasets for standardized monitoring and policy evaluation.
- Highlights value in storing and sharing datasets with transparent metadata to enable downstream analysis and cross-study comparability.

## Considerations and limitations

- Small sample size (n=5) and controlled pen setting; caution when generalizing to larger or field conditions.
- Field deployment would require validation of the squat-urine volume relationship under varying conditions and across populations.