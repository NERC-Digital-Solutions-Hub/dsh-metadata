# PennedSheepWithTags.csv

## Project context
- Project: Uplands-N2O
- Grant number: NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Harris, I.M., Mick J Whelan, Sophie Webb, Andrew J King, Rory P Wilson, Davey L Jones, Alice F Charteris, Laura M Cardenas, Dave R Chadwick
- Data reuse note: If data are reused please ensure it is fully cited

## Data description and collection
- Subjects: Welsh Mountain ewes (n = 5)
- Setting: Urine collection pens
- Equipment: Daily Diary (DD) tags (triaxial accelerometers) from Wildbyte Technologies Ltd., UK
- Sensors: 3-axis acceleration (X = surge, Y = sway, Z = heave), 12-bit, ±8 g, 40 Hz
- Objective: Determine whether squat duration during urination predicts urine volume per event
- Protocol: Feed carried to sheep; urination events observed with corresponding start times of squatting; urine volume per event recorded
- Data processing: DD tag data analyzed blind with a Boolean algorithm to determine squatting duration
- Validation: All observed urine events were detected by the algorithm; no false positives or false negatives in this dataset
- Field deployment: Regression of squatting duration against measured urine volume used to estimate urine volume from squat time in the field

## Data processing and results
- Analysis: Linear regression of squatting duration vs. urine volume across all sheep
- Outcome: Linear relationship identified
- Application: Equation from the regression used to estimate urine volume from squat duration for field deployments

## Data structure and fields
- Sheep_ID: Identifier for each replicate sheep (1–5)
- Time: Time of observed urination posture (hh:mm:ss)
- Date: Date of urination event (dd/mm/yyyy)
- SquatTime: Squatting duration as identified by the algorithm (seconds) [note: described as boolean in text; units indicate seconds]
- MeasuredVol: Measured urine volume per event (ml)
- EstimatedVol: Estimated urine volume based on squat time (ml)

## Data quality, metadata, and governance considerations
- Metadata clarity: Clear field definitions and units provided, though there is an inconsistency in describing SquatTime as a boolean versus seconds
- Data quality: Direct observation corroborated by automated detection; high internal validity within the controlled setting
- Reuse governance: Data should be cited fully when reused; provenance and methods are documented to support reproducibility
- Access and sharing: Not specified; consider data sharing and public availability in line with data governance standards and metadata completeness

## Relevance for monitoring frameworks
- Demonstrates integration of sensor-derived metrics (accelerometer data) with traditional measurements (urine volume) to derive a scalable estimator
- Illustrates workflow for validating a proxy measure (squat duration) and deploying an estimator in field conditions
- Highlights data management considerations (metadata clarity, provenance, and citation) relevant to monitoring datasets used for policy evaluation and decisionmaking