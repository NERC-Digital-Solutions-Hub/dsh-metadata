# PennedSheepWithTags.csv

## Overview
- Dataset from a urine collection study with five Welsh Mountain ewes (n=5) housed in urine collection pens.
- Daily Diary (DD) tri-axial accelerometer tags (Wildbyte Technologies Ltd., UK) measured acceleration (X, Y, Z) at 40 Hz to detect squatting during urination.
- Objective: determine if squatting duration (SquatTime) predicts urine volume per urination event; a linear relationship was found and used to estimate field urine volume from squat time.
- Data includes observed urination events, measured urine volumes, and estimated volumes based on the squat-time model.
- Publication and reuse require full citation of the dataset (Data reuse citation requested).

## Data collection, instrumentation, and study design
- Sheep: Welsh Mountain ewes in controlled pens; five individuals identified by Sheep_ID (1–5).
- Instrumentation: Daily Diary triaxial accelerometers with 12-bit resolution (-8 to 8 g) operating at 40 Hz.
- Procedure: Feed provided in pens; urination events observed and start time of squatting recorded; urine volume measured for each event.
- Data processing: A blind, Boolean-style algorithm analyzed DD tag data to determine squatting duration (SquatTime, in seconds) for each event.
- Outcome: All observed urine events were detected by the algorithm with no false positives or negatives in this dataset.

## Data structure and metadata (headers and units)
- Sheep_ID: Identifier for each replicate sheep (1–5).
- Time: Time of urination posture observed (hh:mm:ss).
- Date: Date of the urination event (dd/mm/yyyy).
- SquatTime: Squatting duration detected by the algorithm (seconds) [derived from DD tag data].
- MeasuredVol: Volume of urine for the event as measured (milliliters, ml).
- EstimatedVol: Urine volume estimated from squat time using the linear relationship (ml).

## Data processing, quality assurance, and lineage
- Processing: SquatTime derived from a blinded analysis of DD tag accelerometer data; MeasuredVol used to establish the squat-volume relationship.
- Modeling: Linear regression between SquatTime and MeasuredVol to obtain an equation used to estimate Vol for field deployments.
- QA notes: The study reports no misclassifications (no false positives/negatives) for the detected urination events within this dataset.

## Provenance, documentation, and reuse
- Project: Uplands-N2O; Grant NE/M015351/1.
- Authors: Karina A. Marsden, Lucy Lush, Jon A Holmberg, Harris, I.M., Mick J Whelan, Sophie Webb, Andrew J King, Rory P Wilson, Davey L Jones, Alice F Charteris, Laura M Cardenas, Dave R Chadwick.
- Data availability and description accompany the file; users should cite the dataset fully if reused.
- File format: CSV (PennedSheepWithTags.csv) with clearly defined headers and units.

## Use considerations, limitations, and governance
- Limitations: Small sample size (n=5) and controlled pen environment; results may not generalize to broader field conditions without validation.
- Data governance: Clear metadata and variable definitions support discovery and reuse; dataset is designed to be both machine- and human-readable.
- Citation and attribution: Full dataset citation required for reuse; ensure proper acknowledgment of authors and grant.

## Practical implications for data stewardship
- The dataset demonstrates a well-documented data collection and processing workflow, including an explicit data dictionary (headers, units) and a transparent transformation (SquatTime to EstimatedVol).
- Suitable for benchmarking data governance practices around standard metadata, data provenance, and reproducible analysis workflows.
- Recommend retaining the linkage between observed measures (MeasuredVol) and model-based estimates (EstimatedVol) for traceability and future updates.