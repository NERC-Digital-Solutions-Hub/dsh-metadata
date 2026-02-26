# Nature and Units of recorded values, Calibration and Quality control

- Overview
  - Documents the nature and units of recorded values across six CSV files related to isolation of novel Bacteroides host groups and the use of this marker set with established fecal indicators in drinking water contexts.
  - File 1–5 focus on isolation processes; File 6 covers detection of fecal indicator bacteria (FIB) and MS markers in drinking water and wastewater effluents.
  - Includes calibration details for instruments and quality control procedures.

- Files and their recorded units

  - File 1: LocationOfFaecalSampling.csv
    - Units relate to sampling locations: latitude and longitude in decimal degrees; altitude in metres.

  - File 2: IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
    - Location coordinates: latitude, longitude (decimal degrees); altitude (metres).
    - CFU data from diluted faecal samples.
    - Master faecal solution composition and dilution context:
      - Master solution described as mixtures of faecal material and Ringers solution.
      - Volume-to-faeces relationships (e.g., 1 mL of master solution corresponds to 0.1 g faeces; additional dilution steps noted with corresponding faeces masses).
      - TNTC indicates samples Too Numerous To Count.
    - Key figures:
      - Limit of detection: 1 CFU per 0.0001 g faeces.
      - Maximum detected: 16 CFU per 0.001 g faeces.

  - File 3: IsolationBacteroidesHostsWeek10-6-18StepB.csv
    - Contains CFU data with confirmation criteria (CFU recorded for positive/negative esculin reaction and aerobic/anaerobic conditions).
    - Note: In this step, numbers of CFU were not used in the analysis.

  - File 4: IsolationBacteroidesHostsWeek17-6-18StepA.csv
    - Similar criteria to File 2 Step A (location coords and CFU data with the master-solution methodology).

  - File 5: IsolationBacteroidesHostsweek17-6-18StepB.csv
    - Similar criteria to File 3 Step B (CFU-related confirmation data).

  - File 6: DetectionOfFIB&MSTmarkers.csv
    - FIB and MS markers in water and wastewater samples:
      - FIB: intestinal enterococci, total coliforms, Escherichia coli.
      - Markers measured as CFU per 100 mL (for FIB) and plaque-forming units per mL (PFU/mL) for phages.
      - Units:
        - CFU/100 mL (FIB markers).
        - PFU/1 mL (phages, including those targeting Bacteroides fragilis GB124 and new hosts).
      - Reported ranges:
        - FIB: lowest detected 1 CFU/100 mL; maximum detected 720,000 CFU/100 mL; TNTC when too numerous to count.
        - Phages: lowest 1 PFU/1 mL; maximum 740 PFU/1 mL; TNTC when too numerous to count.

- Calibration
  - Instrumentation and calibration dates (Feb 2017 and Feb 2018) include:
    - Incubators (Orbital incubator; Stuart SI500) — with serial numbers and calibration dates.
    - Vortex mixer (Fisher Scientific) — serial number; calibration noted as brand new.
    - Autoclave (Sterilmatic STMEX) — serial number; calibration dates.
    - Centrifuge (Thermo Scientific Sorval ST 40) — serial number; calibration dates.
    - Vacuum pump (Thomas) — serial number; calibration date.
    - Spectrophotometer (HACH DR/2500) — serial number; calibration dates.
    - Water bath (Fisher Scientific) — serial number; calibration dates.

- Quality control
  - Use of sample blanks: sterile distilled water run on all microbiological tests.
  - Consistency: the same group of analysts performed individual tests during each sampling campaign to reduce inter- and intra-campaign variation.

- Data handling notes for data support
  - The document provides explicit unit definitions and replication/quality controls essential for cleaning, combining, and validating datasets.
  - Enables creation of self-serve data products (e.g., location-based sampling maps, CFU/PFU dashboards) with clear provenance from sampling to analysis and calibration steps.
  - Highlights potential data integration points across files (location data, CFU counts, dilution factors, and calibration metadata) and the need to harmonize units (CFU/100 mL, CFU/g, CFU per sample) for cross-file analyses.