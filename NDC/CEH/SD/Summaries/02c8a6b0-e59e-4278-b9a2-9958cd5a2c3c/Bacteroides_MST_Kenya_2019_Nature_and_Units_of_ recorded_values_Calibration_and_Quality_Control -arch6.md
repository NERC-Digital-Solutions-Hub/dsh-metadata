# Nature and Units of recorded values, Calibration and Quality control

## Overview
- Documentation of nature and units for recorded values across six CSV files related to isolating novel Bacteroides hosts and using them with established fecal contamination markers in water.
- Includes definitions of measurement units, calibration information for instruments, and quality control practices to ensure data reliability.

## Files and their units

- 1. LocationOfFaecalSampling.csv
  - Units relate to sampling locations: latitude and longitude in decimal degrees; altitude in metres.

- 2. IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Units include sampling location (latitude, longitude, altitude).
  - Colony forming units (CFU) recovered from diluted faecal samples.
  - Details on master faecal solution weight (e.g., 5 g faecal sample + 5 mL Ringer’s solution) and dilution/volume relationships.
  - Measurement conversions: e.g., various volumes of the master solution correspond to specific gram amounts of faeces.
  - Limits: limit of detection (1 CFU per 0.0001 g faeces); maximum detected value (16 CFU per 0.001 g faeces).
  - TNTC denotes Too Numerous To Count.

- 3. IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Unit: CFU (colony forming units).
  - CFU counts were not always used in this confirmatory step.
  - Records presence/absence of colonies with:
    - Positive/Negative Esculin reaction
    - Anaerobic/Aerobic conditions

- 4. IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Uses similar criteria to StepA in file 2 for data recording.

- 5. IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Uses similar criteria to StepB in file 3 for data recording.

- 6. DetectionOfFIB&MSTmarkers.csv
  - Faecal indicator bacteria (FIB): intestinal enterococci, total coliforms, Escherichia coli.
  - Units: CFU per 100 mL for drinking water sources and wastewater effluents.
  - Range: lowest detected 1 CFU/100 mL; maximum detected 720,000 CFU/100 mL; TNTC when too numerous to count.
  - Also includes bacteriophages:
    - Somatic coliphages; phages infecting Bacteroides fragilis GB124; and phages infecting the new Bacteroides spp. hosts.
    - Units: plaque forming units per 1 mL of water (PFU/mL); range 1 to 740 PFU/mL; TNTC for Too Numerous To Count.

## Calibration

- Table of instruments and calibration dates:
  - Incubator (Orbital), serial R00100407 – calibration Feb 2017 & 2018
  - Vortex mixer (Mini), serial 16070506 – calibration date listed as brand new
  - Autoclave (Sterilmatic), serial STMEX – calibration Feb 2017 & 2018
  - Centrifuge (Thermo Scientific Sorval ST 40), serial 41035124 – calibration Feb 2017 & 2018
  - Vacuum pump (Thomas), serial 0100000070 – calibration date listed as brand new
  - Spectrophotometer (DR/2500, HACH), serial 03070005726 – calibration Mar 2017 & 2018
  - Water bath (Fisher Scientific), serial 9A1050005 – calibration Mar 2017

- Calibration context:
  - Ensures instrument readings are accurate for microbiological assays and quantitative measurements across all six files.

## Quality control

- Use of sample blanks: sterile distilled water included as blanks on all microbiological tests.
- Consistency: the same group of analysts performed the tests within each sampling campaign to reduce inter-analyst variation.

## Notes and clarifications

- TNTC (Too Numerous To Count) used across CFU and PFU measurements to indicate semiquantitative results where counts exceed measurement capacity.
- Some sections describe detailed conversion factors for preparing master solutions and dilutions; these are critical for accurate back-calculation of original faecal sample quantities from CFU counts.
- Data interpretation involves combining results from multiple files (e.g., CFU data with FIB and MS markers) to assess faecal contamination in water sources and treatment plant effluents.