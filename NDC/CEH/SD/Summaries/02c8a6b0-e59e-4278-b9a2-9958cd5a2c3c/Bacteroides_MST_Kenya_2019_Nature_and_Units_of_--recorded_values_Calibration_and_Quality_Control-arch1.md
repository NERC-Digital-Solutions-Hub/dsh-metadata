# Nature and Units of recorded values, Calibration and Quality control

## Overview
- Describes the nature, units, calibration, and quality control for data generated while isolating novel Bacteroides spp. hosts to assess faecal contamination of water sources.
- Also covers the use of these novel markers alongside established markers (Bacteroides fragilis GB124, somatic coliphages, and faecal indicator bacteria - FIB: total coliforms, E. coli, enterococci).
- Emphasizes how data are collected, stored, calibrated, and quality-checked across multiple steps and files.

## Data files and their units

- 1. LocationOfFaecalSampling.csv
  - Units relate to sampling locations: Latitude and Longitude in decimal degrees; altitude in metres.

- 2. IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Location units (as above: decimal degrees; altitude in metres).
  - Bacterial data: colony forming units (CFU) recovered from diluted faecal samples.
  - Master faecal solution details and dilution scheme (e.g., 5 g faeces + 5 mL Ringer’s solution; conversions such as 1 mL master solution = 0.1 g faeces; etc.).
  - Specific quantitative notes:
    - Limit of detection: 1 CFU per 0.0001 g faeces.
    - Maximum detected: 16 CFU per 0.001 g faeces.
    - TNTC = Too Numerous To Count.

- 3. IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Units: CFU (colony forming units).
  - Purpose: confirmatory step to verify growth in described environments; CFU recorded by combinations of Es–/Anaerobic/Aerobic and positive/negative esculin reactions.

- 4. IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Similar structure and criteria as Step A above.

- 5. IsolationBacteroidesHostsWeek17-6-18StepB.csv
  - Similar structure and criteria as Step B above.

- 6. DetectionOfFIB&MSTmarkers.csv
  - FIB data: enterococci, total coliforms, E. coli.
  - Units: CFU per 100 mL for water samples.
  - Viral markers: somatic coliphages and phages infecting B. fragilis GB124 and novel Bacteroides hosts.
  - Units for viral markers: plaque forming units per 1 mL (PFU/mL).
  - Data ranges: 1 to 720,000 CFU/100 mL for FIB; 1 to 740 PFU/mL for viral markers.
  - TNTC indicates too numerous to count.

## Calibration

- Table of instruments and calibration dates:
  - Incubator (Orbital incubator; Stuart SI500) – calibration dates February 2017 & 2018.
  - Vortex mixer (Fisher Scientific) – calibration: brand new.
  - Autoclave (Sterilmatic STMEX) – calibration dates February 2017 & 2018.
  - Centrifuge (Thermo Scientific Sorval ST 40) – calibration dates February 2017 & 2018.
  - Vacuum pump (Thomas) – calibration: brand new.
  - Spectrophotometer (DR/2500, HACH) – calibration dates March 2017 & 2018.
  - Water bath (Fisher Scientific) – calibration dates March 2017.
- Calibration ensures instrument accuracy for the various culture, measurement, and detection steps used in the study.

## Quality control

- Sample blanks: sterile distilled water included and run on all microbiological tests.
- Consistency: the same group of analysts performed individual tests during each sampling campaign to reduce inter-operator variation.
- Purpose: to ensure reliability and comparability of CFU and PFU measurements across samples and timepoints.

## Key data considerations for analysts

- Data provenance and linkage: multiple files track location, isolation steps, and detection markers, enabling integrated analyses of host isolation data with faecal markers in water and effluent samples.
- Units and conversions: clear conversion factors and dilution schemes are provided (e.g., master faecal solution composition and corresponding CFU detection limits).
- Detection limits and TNTC: explicit limits and “Too Numerous To Count” notes guide interpretation of low vs. high counts.
- Scale and accessibility: data include geographic coordinates and altitude, facilitating spatial analyses and alignment with environmental datasets.
- Data quality: documented calibration dates and QA procedures support reliability and reproducibility of results.