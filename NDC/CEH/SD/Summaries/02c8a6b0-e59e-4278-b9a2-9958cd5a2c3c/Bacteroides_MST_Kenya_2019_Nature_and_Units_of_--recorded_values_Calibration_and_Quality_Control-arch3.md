# Nature and Units of recorded values, Calibration and Quality control

- Overview
  - Describes nature and units of data across six CSV files used to assess faecal contamination of water sources using novel Bacteroides spp. hosts, in conjunction with established markers (Bacteroides fragilis GB124, somatic coliphages, and faecal indicator bacteria).
  - Covers sampling location data, isolation procedures, and detection of FIB and viral markers, plus instrument calibration and quality control.

- Data files and their units

  - 1. LocationOfFaecalSampling.csv
    - Units related to sampling locations: latitude and longitude in decimal degrees; altitude in metres.

  - 2. IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
    - Location coordinates: latitude (decimal degrees), longitude (decimal degrees), altitude (metres).
    - Bacterial counts: colony forming units (CFU) recovered from diluted faecal samples.
    - Master faecal solution composition and dilution factors:
      - Master solution: 5 g faeces + 5 mL Ringers’ solution.
      - Serial weight/dilution steps mapping (e.g., 1 mL of master solution = 0.1 g faeces; 10^-1 mL = 0.01 g; 100 µL of 10^-1 mL = 0.001 g, etc.).
    - Detection characteristics: limit of detection = 1 CFU per 0.0001 g faeces; maximum detected = 16 CFU per 0.001 g faeces; TNTC (Too Numerous To Count).

  - 3. IsolationBacteroidesHostsWeek10-6-18StepB.csv
    - Unit: CFU (colony forming units).
    - Confirmation data: esculin reaction (positive/negative) and environment type (aerobic/anaerobic) for CFU counts.

  - 4. IsolationBacteroidesHostsWeek17-6-18StepA.csv
    - Similar structure and criteria to StepA above (location coords, CFU counts, dilutions/definitions).

  - 5. IsolationBacteroidesHostsweek17-6-18StepB.csv
    - Similar to StepB files above (aerobic/anaerobic, esculin reactions, CFU).

  - 6. DetectionOfFIB&MSTmarkers.csv
    - FIB and viral/marker data:
      - Faecal indicator bacteria: intestinal enterococci, total coliforms, Escherichia coli.
      - Units: CFU per 100 mL for water samples and wastewater effluent.
      - Viral markers: somatic coliphages; phages infecting Bacteroides fragilis GB124; phages infecting the novel Bacteroides spp. hosts.
      - Units: plaque forming units per 1 mL (PFU/mL).
    - Detection ranges and qualifiers:
      - FIB: lowest detected 1 CFU/100 mL; maximum detected 720,000 CFU/100 mL; TNTC indicated when too numerous to count.
      - Phages: lowest detected 1 PFU/1 mL; maximum detected 740 PFU/1 mL; TNTC indicated when too numerous to count.

- Calibration
  - Instrument calibration details for quality assurance:
    - Incubator (Orbital incubator, Stuart SI500): calibration dates February 2017 & 2018.
    - Vortex mixer (Fisher Scientific): calibration date brand new (no further date given).
    - Autoclave (Sterilmatic): calibration dates February 2017 & 2018.
    - Centrifuge (Thermo Scientific Sorval ST 40): calibration dates February 2017 & 2018.
    - Vacuum pump (Thomas): calibration date brand new.
    - Spectrophotometer (HACH DR/2500): calibration dates March 2017 & 2018.
    - Water bath (Fisher Scientific): calibration date March 2017.
  - These calibration details support traceability and comparability of measurements across time.

- Quality control
  - Use of sample blanks (sterile distilled water) in all microbiological tests.
  - Consistency in testing: the same group of analysts performed individual tests within a sampling campaign to reduce variability.

- Relevance for monitoring frameworks
  - Provides standardized spatial (latitude/longitude/altitude) and quantitative data (CFU and PFU) in relation to faecal contamination and microbial markers.
  - Combines novel Bacteroides hosts with established markers (GB124, somatic coliphages, FIB) to strengthen environmental health indicators.
  - Detailed metadata support (units, master solution composition, detection limits, TNTC, calibration dates) facilitates data quality, reproducibility, and integration into policy evaluation and future decision-making.

- Considerations and challenges for governance and policy use
  - Data standardization is explicit through defined units and calibration records, aiding transparency and comparability.
  - Complexity of transforming between CFU and PFU and interpreting TNTC results across datasets.
  - The need to manage metadata completeness and access to raw data, given potential barriers to data sharing and data governance requirements.