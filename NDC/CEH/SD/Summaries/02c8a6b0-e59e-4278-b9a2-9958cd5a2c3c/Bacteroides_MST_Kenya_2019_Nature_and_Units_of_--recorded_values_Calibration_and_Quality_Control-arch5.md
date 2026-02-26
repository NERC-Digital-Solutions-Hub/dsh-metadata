# Nature and Units of recorded values, Calibration and Quality control

## Overview
- Describes the nature and units of recorded values across six CSV files related to isolating novel Bacteroides hosts for faecal contamination assessment of water, and the use of these markers alongside established indicators (FIB and viral indicators).
- Distinguishes between data on sampling/host isolation (files 1–5) and data on FIB/MST markers (file 6).
- Includes calibration details for equipment and quality control procedures.

## Data files and their units

- 1. LocationOfFaecalSampling.csv
  - Units indicate sampling locations: Latitude and Longitude in decimal degrees; Altitude in metres.

- 2. IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Location data: Latitude, Longitude, Altitude (decimal degrees/metres).
  - CFU data: numbers of colony forming units from diluted faecal samples (CFU).
  - Master faecal solution: weight details (e.g., 5 g faeces + 5 mL Ringers’ solution; various dilutions).
  - Conversion/measurement specifics: definitions of sample weights per volume (e.g., 1 mL of master solution equals 0.1 g faeces; 100 µL equals 0.001 g faeces).
  - Analytical limits: Limit of detection = 1 CFU per 0.0001 g faeces; Maximum detected = 16 CFU per 0.001 g faeces.
  - TNTC: Too Numerous To Count.

- 3. IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Unit: CFU (colony forming units) for confirmation step.
  - Notes: numbers not used for final consideration; focuses on presence/absence and reactions (positive/negative Esculin, anaerobic/aerobic) with CFU counts.

- 4. IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Similar structure and criteria to Week10-6-18 StepA file (locations, CFU data, master solution details, and dilution information).

- 5. IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Similar structure to StepB files above (CFU data and reaction criteria).

- 6. DetectionOfFIB&MSTmarkers.csv
  - FIB data: levels of faecal indicator bacteria (Enterococci, Total coliforms, E. coli) in drinking water and wastewater effluents.
  - Units: CFU per 100 mL (CFU/100 mL) with detected range from 1 to 720,000 CFU/100 mL; TNTC when too numerous to count.
  - Viral indicators: somatic coliphages; phages infecting Bacteroides fragilis GB124; phages infecting novel Bacteroides hosts; units are plaque forming units per mL (PFU/mL) with range from 1 to 740 PFU/mL; TNTC when too numerous to count.

## Calibration

- Table details instruments and their calibration dates (February 2017 & 2018 for many items).
  - Incubator: Orbital; Stuart SI500; calibration dates Feb 2017 & 2018.
  - Vortex mixer: Fisher Scientific; calibration date listed as Brand new (no past date specified).
  - Autoclave: Sterilmatic STMEX; calibration Feb 2017 & 2018.
  - Centrifuge: Thermo Scientific Sorval ST 40; calibration Feb 2017 & 2018.
  - Vacuum pump: Brand new; calibration not specified beyond new status.
  - Spectrophotometer: HACH DR/2500; calibration Feb 2017 & 2018.
  - Water bath: Fisher Scientific; calibration March 2017.
- Calibration details support consistency and traceability of measurements across the data files.

## Quality control

- Use of sample blanks: sterile distilled water run on all microbiological tests.
- Consistency in analysis: the same group of analysts performed tests during each sampling campaign to reduce inter-analyst variation.

## Data governance considerations for Data Stewards

- Metadata consistency:
  - Ensure uniform units and reference systems across all files (e.g., decimal degrees for coordinates, metres for altitude, CFU and PFU units with clear definitions).
  - Standardize terminology for TNTC and detection limits; clearly document how non-detects or TNTC are represented.
- Data provenance and lineage:
  - Maintain clear records of sample collection locations, master solution preparation, dilution schemes, and calculation methods used to derive CFU counts (as described in the master solution definitions and weight/volume relationships).
- Measurement standards and calibration:
  - Preserve calibration dates and instrument identifiers to enable traceability and reproducibility.
  - Include instrument make/model and serial numbers where available.
- Data quality and governance:
  - Document QC procedures (blanks, analyst consistency) to inform data quality assessments.
  - Capture information about data processing steps (e.g., steps A/B, confirmatory steps) to enable reproducibility.
- Data sharing and interoperability:
  - Provide sufficient metadata to allow reuse by data users, including both geospatial and microbiological measurement details.
  - When integrating with portals or catalogues, map units and methods to common ontologies or standards to facilitate discovery and interoperability.