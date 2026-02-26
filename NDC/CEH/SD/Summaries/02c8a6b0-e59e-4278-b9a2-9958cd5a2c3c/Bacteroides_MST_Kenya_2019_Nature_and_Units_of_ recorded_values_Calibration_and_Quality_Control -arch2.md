# Nature and Units of recorded values, Calibration and Quality control

- Purpose and scope
  - Describes the data types, measurement units, calibration, and quality control for studies isolating novel Bacteroides hosts to assess faecal contamination in water sources, and for integrating these markers with established indicators (GB124, somatic coliphages, and faecal indicator bacteria) in drinking water and wastewater contexts.

- File 1: LocationOfFaecalSampling.csv
  - Units relate to sampling locations: latitude and longitude in decimal degrees; altitude in metres.

- File 2: IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Units include sampling location (latitude, longitude, altitude) and colony-forming units (CFU) recovered from diluted faecal samples.
  - Master faecal solution composition and weight-to-volume relationships provided (5 g faecal sample + 5 mL Ringer’s solution; dilution scheme with explicit mass-to-volume conversions).
  - Key performance metrics:
    - Limit of detection (LOD): 1 CFU per 0.0001 g faeces
    - Maximum detected: 16 CFU per 0.001 g faeces
    - TNTC indicates Too Numerous To Count

- File 3: IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Units: CFU (colony forming units) used as a confirmatory step; CFU counts not recorded for this step.
  - Data categories based on:
    - Esulin (esculin) reaction: Positive/Negative
    - Oxygen tolerance: Anaerobic/Aerobic

- File 4: IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Similar structure and criteria as File 2 (Step A) with location data and CFU-related measurements.

- File 5: IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Similar structure and criteria as File 3 (Step B) with qualitative confirmations (Positive/Negative esculin, Aerobic/Anaerobic).

- File 6: DetectionOfFIB&MSTmarkers.csv
  - Faecal indicator bacteria (FIB): intestinal enterococci, total coliforms, Escherichia coli
    - Measured in CFU per 100 mL (CFU/100 mL)
    - Range: lowest detected 1 CFU/100 mL; maximum detected 720,000 CFU/100 mL
    - TNTC indicates Too Numerous To Count
  - Somatic coliphages and Bacteroides GB124 phages, plus phages infecting the new candidate Bacteroides hosts
    - Measured in plaque-forming units per millilitre (PFU/mL)
    - Range: lowest detected 1 PFU/mL; maximum detected 740 PFU/mL
    - TNTC indicates Too Numerous To Count

- Calibration
  - Instruments and calibration dates:
    - Incubator (Orbital incubator, Stuart SI500) – calibration dates: February 2017 & 2018
    - Vortex mixer (Mini vortex mixer) – calibration: brand new
    - Autoclave (Sterilmatic STMEX) – calibration dates: February 2017 & 2018
    - Centrifuge (Thermo Scientific Sorval ST 40) – calibration dates: February 2017 & 2018
    - Vacuum pump (Thomas) – calibration: brand new
    - Spectrophotometer (DR/2500, HACH) – calibration dates: March 2017 & 2018
    - Water bath (Fisher Scientific) – calibration dates: March 2017
  - Notes:
    - Calibration dates indicate routine checks across campaigns within the study period.

- Quality control
  - Use of sample blanks: sterile distilled water included in all microbiological tests
  - Consistency approach: the same group of analysts conducts individual tests within a sampling campaign to reduce inter-operator variation

- Data handling and aims for analysts monitoring the environment
  - Data are stored with clear geographic context (sampling locations) and method-specific measurements (CFU/CFU per g, CFU/100 mL, PFU/mL)
  - Calibration and QC information supports data quality assessment and traceability for environmental health monitoring over time
  - The structure enables integration of novel Bacteroides hosts with established faecal contamination indicators to evaluate water quality and policy performance.