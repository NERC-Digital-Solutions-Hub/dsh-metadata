# Nature and Units of recorded values, Calibration and Quality control

- Scope of the dataset
  - Files 1–5 cover the isolation and characterization of novel Bacteroides spp. hosts from faecal samples for assessing faecal contamination of water sources.
  - File 6 combines these novel markers with established markers (Bacteroides fragilis GB124, somatic coliphages, and faecal indicator bacteria) to assess water quality in drinking water sources and wastewater effluents.

- File 1: LocationOfFaecalSampling
  - Units for sampling locations: latitude and longitude in decimal degrees; altitude in metres.

- File 2: IsolationOfBacteroidesHostsWeek10-6-18StepA
  - Location coordinates: latitude and longitude in decimal degrees; altitude in metres.
  - Bacterial counts: colony forming units (CFU) recovered from diluted faecal samples.
  - Master faecal solution details: composition and dilution relationships described (master solution = 5 g faecal sample + 5 mL Ringers solution; specific dilutions equate to defined gram amounts).
  - Key measurement references: limits like limit of detection (1 CFU per 0.0001 g faeces) and maximum detected value (16 CFU per 0.001 g faeces); TNTC (Too Numerous To Count).

- File 3: IsolationBacteroidesHostsWeek10-6-18StepB
  - Units: CFU (colony forming units).
  - Notes: CFU counts used as a confirmatory step and not all counts are considered in final tally.
  - Criteria for colony typing: positive/negative esculin reaction, and aerobic/anaerobic conditions.

- File 4: IsolationBacteroidesHostsWeek17-6-18StepA
  - Similar structure and criteria to Week10-6-18 StepA file.

- File 5: IsolationBacteroidesHostsweek17-6-18StepB
  - Similar structure and criteria to Week10-6-18 StepB file.

- File 6: DetectionOfFIB&MSTmarkers
  - Faecal indicator bacteria (FIB): intestinal enterococci, total coliforms, Escherichia coli measured as CFU per 100 mL.
  - Viral/phage markers: somatic coliphages and phages targeting Bacteroides fragilis GB124 and novel hosts, measured as plaque forming units (PFU) per mL.
  - Detection ranges and TNTC: CFU/100 mL range from 1 to 720,000; PFU/mL up to 740; TNTC indicates too numerous to count.

- Calibration details
  - Instruments and calibration dates:
    - Incubator (orbital): calibrated February 2017 & 2018.
    - Vortex mixer: calibration date listed as brand new.
    - Autoclave (Sterilmatic): calibrated February 2017 & 2018.
    - Centrifuge (Thermo Scientific Sorval ST 40): calibrated February 2017 & 2018.
    - Vacuum pump (Thomas): calibration date listed as brand new.
    - Spectrophoto meter (HACH DR/2500): calibrated March 2017 & 2018.
    - Water bath (Fisher Scientific): calibrated March 2017.
  - Note: Calibration details are provided per instrument including type, make/model, serial numbers, and calibration dates to ensure traceability.

- Quality control
  - Use of sample blanks: sterile distilled water included as blanks in all microbiological tests.
  - Consistency in analysis: the same group of analysts performed individual tests within each sampling campaign to reduce inter-operator variability.

- Data governance implications for Data Stewards
  - The dataset provides explicit units, measurement methods, and calibration history, supporting metadata completeness and auditability.
  - Clear definitions of detection limits, maximum values, and TNTC conditions aid in reproducibility and proper data interpretation.
  - Location data with precise geographic coordinates enables accurate spatial discovery and re-use.
  - QA practices (blanks and consistent analysts) strengthen data quality and trustworthiness across datasets.

- Notes on forward use
  - When sharing or cataloguing, ensure accompanying metadata captures file-specific units, calibration records, QA procedures, and any TNTC handling decisions to maintain interoperability across systems and formats.