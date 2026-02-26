# IPORE Soil Measurements Protocol

## Overview
- Studies soil properties using the W.E.T sensor to measure pore water conductivity (EC), volumetric water content (VWC), and soil temperature across households.
- Sampling occurs within households at three fertility zones: Home (near the house, higher management), Near (between home and far), and Far (furthest from the house, more extensive production).
- Measurements taken at three depth intervals: 0–5 cm, 5–10 cm, and 10–15 cm.
- Field work conducted in two kebeles (Konicha and 1st Choroko) with random placement of samples to capture spatial variability.
- Data quality controlled through replicates, calibration, expert field operation, and lab analyses; data uploaded with metadata for discoverability.

## Experimental design and sampling regime
- Within each household, three fertility zones are sampled.
- Sampling locations: Home, Near, Far within each household; measurements taken across farmers with varying wealth status to ensure diversity.
- Experimental configurations include multi-site and multi-replicate designs:
  - Configuration 1: 36 households, 108 measurement sites, 324 samples.
  - Configuration 2: 36 households, 108 measurement sites, 324 samples.
  - Configuration 3: 72 households, 216 measurement sites, 648 samples.
- Kebeles involved: 2 in configurations 1–2, 4 in configuration 3.
- Soil types: 2 in configurations 1–2, 4 in configuration 3.
- Fertility zones per household: 3 (Home, Near, Far), with 3 replicates per zone in the first two configurations and 6 replicates per zone in the third configuration.

## Collection and field procedure
- Sample positioning: Random, with three replicates within each fertility zone.
- Depths for measurements: 0–5 cm, 5–10 cm, 10–15 cm.
- Equipment: W.E.T sensor calibrated for soil water content, electrical conductivity, and temperature.
- Field operation: Conducted by two experienced soil scientists to ensure consistency and accuracy; data recorded on a tablet with an ODK file to minimize mislabeling or data loss.
- Documentation and labeling: Soil samples labelled and stored; minor loss (<5%) due to label eligibility issues.

## Calibration procedures
- W.E.T sensor calibrations are performed to enable field measurements for the specific soil types encountered.
- Soil water content calibration (two-point method):
  - Collect damp soil, measure sensor permittivity in wet and dry states, derive calibration constants (b0, b1) and enter them into the sensor as a custom soil type (Custom 1).
  - Steps include calculating mass and volume of soil, oven-drying, and deriving the calibration equations.
  - Post-calibration, select Custom 1 as the soil type during measurements.
- Pore water conductivity calibration:
  - Use measured soil and water mixtures to determine EC-related parameters (ECp, soil and pore water permittivity) and derive constants for the sensor.
  - Enter these parameters into the sensor under Custom 1.
  - After calibration, measurements are performed using the Custom 1 soil type setting.
- Calibration notes: Calibration procedures are designed to produce field-ready values without repeated calibration after setup.

## Quality control
- Field sampling includes random, triplicate replicates to account for spatial variability.
- The W.E.T sensor is periodically checked in saline solution to ensure accuracy; device chosen for simultaneous measurement of water content, EC, and temperature and ease of use in Ethiopia.
- Data capture and reduction:
  - Data uploaded immediately to a tablet with an ODK file to prevent mis-location and data loss.
  - Soil samples labeled, stored properly; minor sample loss kept under 5%.
  - Laboratory analyses conducted at the University of Aberdeen with strict SOPs and regular calibration of sensors.
- Data characteristics:
  - Sensor accuracy: ~5% for water content, 1.5°C for temperature, 10 mS/m for EC.
  - Data distribution checked and reported as normal in quality control procedures.

## Data files and structure
- IPORE-Soil EC.csv
  - Columns: S. no., HH no., Kebele (PA), HH ID, Fertility Zone, Top depth, Bottom depth, Replicates, January–July EC values (mS m^-1).
- IPORE-Soil water.csv
  - Columns: S. no., HH no., Kebele (PA), HH ID, Fertility Zone, Top depth, Bottom depth, Replicates, January–July volumetric water content (%).
- IPORE-Soil temperature.csv
  - Columns: S. no., HH no., Kebele (PA), HH ID, Fertility Zone, Top depth, Bottom depth, Replicates, January–July soil temperatures (°C).
- Common structure:
  - Each row includes: sample number, household identifiers, district, fertility zone, depth bounds, replicate number, and monthly measurements from January to July.
- Datasets reflect three configurations with varying scales:
  - Configuration 1: 36 households, 108 measurement sites, 324 samples.
  - Configuration 2: 36 households, 108 measurement sites, 324 samples.
  - Configuration 3: 72 households, 216 measurement sites, 648 samples.