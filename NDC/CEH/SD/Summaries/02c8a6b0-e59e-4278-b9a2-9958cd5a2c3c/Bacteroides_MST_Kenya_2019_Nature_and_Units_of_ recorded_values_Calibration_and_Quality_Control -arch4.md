# Nature and Units of recorded values, Calibration and Quality control

- This document describes the data and methods used to isolate novel Bacteroides hosts for assessing fecal contamination of water, and to evaluate these markers alongside established indicators (Bacteroides fragilis GB124, somatic coliphages, and fecal indicator bacteria).

## Data files and their units

- 1. LocationOfFaecalSampling.csv
  - Units: latitude and longitude in decimal degrees; altitude in metres.

- 2. IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Units: location coordinates (latitude/longitude/altitude) and CFU counts from diluted faecal samples.
  - Additional info: weight-based master faecal solution composition (master solution = 5 g faeces + 5 mL Ringers solution; conversions between master solution and faeces weight provided).
  - Key metrics: limit of detection = 1 CFU per 0.0001 g faeces; maximum detected = 16 CFU per 0.001 g faeces; TNTC.

- 3. IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Units: CFU counts; data organized by positive/negative esculin reaction and by anaerobic/aerobic conditions.

- 4. IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Units: CFU counts; criteria similar to StepA in file 2.

- 5. IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Units: CFU counts; criteria similar to StepB in file 3.

- 6. DetectionOfFIB&MSTmarkers.csv
  - FIB data: faecal indicator bacteria (intestinal enterococci, total coliforms, E. coli) in CFU per 100 mL.
  - MS markers data: somatic coliphages; phages infecting GB124 and new Bacteroides hosts; units in PFU per mL.
  - Measurements: lowest detected 1 CFU/100 mL or 1 PFU/mL; maximum detected 720,000 CFU/100 mL or 740 PFU/mL; TNTC when too numerous to count.

## Calibration details

- Table of instruments and calibration dates:
  - Incubator (orbital), model SI500; calibration dates Feb 2017 & 2018.
  - Vortex mixer (brand new in record); calibration date not specified beyond new.
  - Autoclave (Sterilmatic, STMEX); calibration Feb 2017 & 2018.
  - Centrifuge (Thermo Scientific, Sorval ST 40); calibration Feb 2017 & 2018.
  - Vacuum pump (brand new); calibration date not specified.
  - Spectrophotometer (DR/2500, HACH); calibration March 2017 & 2018.
  - Water bath (Fisher Scientific, FB60301); calibration March 2017.
- These details provide traceability for instrument accuracy across sample processing and measurements.

## Quality control

- Use of sample blanks: sterile distilled water included as blanks in all microbiological tests.
- Consistency: the same group of analysts performed individual tests within each sampling campaign to reduce inter-operator variation.

## Data governance implications for Data Leaders

- Data types and metadata:
  - Multiple interrelated data files capture spatial data, experimental steps (A/B), CFU counts, and marker data; clear unit definitions are provided to ensure consistency and interoperability.
- Data quality and provenance:
  - Explicit LOD/maximum values, TNTC conditions, and calibration records support data quality assessment and reproducibility.
- Standardization and discoverability:
  - Structured naming and explicit unit metadata enable easier integration across datasets and potential alignment with broader water quality data ecosystems.
- Data strategy considerations:
  - To maximize utility, consider consolidating into a central data catalog with dataset-level metadata (sensors/instruments used, calibration history, QA procedures, and data lineage).
  - Address potential data gaps or inconsistencies across files (e.g., incomplete calibration dates for some equipment) and ensure uniform units where applicable.
  - Facilitate co-ownership and collaboration by documenting data collection contexts, methodologies, and thresholds (LOD, maximum detectable values, TNTC) to support reuse by policy colleagues and partners.