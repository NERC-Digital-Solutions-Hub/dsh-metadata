# PennedSheepWithTags.csv

## What this dataset is
- Urine collection study with five Welsh Mountain ewes (n=5) using Daily Diary (DD) accelerometer tags to predict urine volume from squat duration.
- Goal: determine if squat time correlates with urine volume and use the relationship to estimate volume in field deployments.

## Data collection and devices
- Setting: urine collection pens; feed provided in pens.
- Devices: triaxial accelerometers (X, Y, Z) at 40 Hz, 12-bit resolution, gluing DD tags to a shorn hind area.
- Observations: approximate start time of squatting during urination; volume of each urine event measured.
- Analysis: data from DD tags analyzed blind with an algorithm to identify squatting duration; no false positives or negatives reported in this dataset.

## Data structure and variables
- Sheep_ID: 1–5 (replicate sheep).
- Time: urination event start time (hh:mm:ss).
- Date: date of urination event (dd/mm/yyyy).
- SquatTime: squatting duration as identified by the algorithm (in seconds).
- MeasuredVol: observed urine volume for each event (in ml).
- EstimatedVol: urine volume estimated from squat duration using the regression relationship (in ml).

## Analysis and key findings
- There is a linear relationship between squatting duration and measured urine volume.
- A regression equation was derived and used to estimate urine volume from squat time for field deployments.
- The algorithm reliably detected squatting duration with no misclassifications in this dataset.

## Data quality, provenance, and governance
- Project: Uplands-N2O, grant NE/M015351/1.
- Authors: list of researchers provided.
- Data reuse note: “If data are reused please ensure it is fully cited.”
- Limitations: small sample size (n=5) and controlled environment; applicability to broader populations or field conditions should be considered; measurement relies on device placement and the identified squatting duration.

## Metadata, accessibility, and reuse guidance
- Data headers and units are specified, facilitating discoverability and integration with other data assets.
- Clear linkage between observed measurements (MeasuredVol) and model-based estimates (EstimatedVol) supports data product development.
- For reuse, ensure proper citation of the original project and dataset.