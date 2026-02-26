# PennedSheepWithTags.csv

## Overview
- Dataset from a urine collection study with five Welsh Mountain ewes housed in urine collection pens.
- Aim: determine if squatting duration (squat time) during urination can predict the volume of urine produced per event.
- Devices: Daily Diary (DD) tri-axial accelerometer tags attached to the hind, measuring X (surge), Y (sway), and Z (heave) at 40 Hz with 12-bit resolution (-8 to 8 g).

## Experimental setup and subjects
- Subjects: Welsh Mountain ewes (n = 5).
- Location: urine collection pens.
- Procedure: feed brought to sheep; urination events observed and start time of squatting recorded; urine event volumes measured.

## Data collection and processing
- Data collected per urination event:
  - SquatTime: squatting duration identified by a Boolean algorithm on DD tag data (in seconds).
  - MeasuredVol: actual urine volume per event (in milliliters, ml).
  - Time and Date: timestamp of the urination event (hh:mm:ss and dd/mm/yyyy).
  - Sheep_ID: identifier for each replicate sheep (1–5).
- Data processing: accelerometer data analyzed blind to determine squatting duration; the algorithm detected all events with no false positives or negatives in this dataset.

## Modeling and application
- Analysis: linear regression of SquatTime versus MeasuredVol across all sheep.
- Outcome: a linear relationship enabling estimation of urine volume from squat time alone.
- Field deployment: use the derived equation to estimate urine volume from squat time in field deployments.

## Data fields and units
- Sheep_ID: 1–5
- Time: hh:mm:ss
- Date: dd/mm/yyyy
- SquatTime: seconds (as identified by the algorithm)
- MeasuredVol: milliliters (ml)
- EstimatedVol: milliliters (ml) derived from squat time using the regression relationship

## Reuse and citation
- Note: If data are reused, ensure the dataset is fully cited.
- Project context: Project Uplands-N2O, Grant NE/M015351/1.
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Harris, I.M., Mick J Whelan, Sophie Webb, Andrew J King, Rory P Wilson, Davey L Jones, Alice F Charteris, Laura M Cardenas, Dave R Chadwick.