# Nature and Units of recorded values, Calibration and Quality control

## Overview
- Document describes the nature and units of recorded values across six CSV files related to isolating novel Bacteroides spp. hosts for assessing faecal contamination in water, plus the use of these markers with established indicators (faecal indicator bacteria and somatic coliphages).
- Includes calibration details for laboratory instruments and quality control procedures.

## Data files and their units
- 1. LocationOfFaecalSampling.csv
  - Location of faecal sample collection.
  - Latitude and Longitude: decimal degrees; Altitude: metres.
- 2. IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Location coordinates (latitude/longitude/altitude) and CFU counts from diluted faecal samples.
  - Master faecal solution composition and weight data:
    - Master solution: 5 g faeces + 5 mL Ringers’ solution.
    - Dilution scheme notes: 1 mL master solution corresponds to 0.1 g faeces; 0.01 g per 0.1 mL; etc.
  - Additional notes include: limit of detection (1 CFU per 0.0001 g faeces); maximum detected value (16 CFU per 0.001 g faeces); TNTC.
- 3. IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - CFU data for confirmatory step with detection of growth.
  - Categories: Positive/Negative Esculin reaction; Anaerobic/Aerobic conditions; CFU values.
- 4. IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Similar structure and criteria to StepA above (location, CFU, etc.).
- 5. IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Similar structure to StepB above (positive/negative Esculin; anaerobic/aerobic; CFU).
- 6. DetectionOfFIB&MSTmarkers.csv
  - Faecal indicator bacteria (FIB): Enterococci, Total Coliforms, E. coli.
  - Measured units: CFU per 100 mL; range from 1 to 720,000 CFU/100 mL; TNTC when too numerous to count.
  - Viral markers: plaque-forming units (PFU) per mL for somatic coliphages, GB124 phages, and phages for new Bacteroides hosts (range 1 to 740 PFU/mL; TNTC when necessary).

## Calibration and instruments
- Table of instruments and calibration dates:
  - Incubator (Orbital), Make: Stuart, Model: SI500, S/N: R00100407, Calibration: Feb 2017 & 2018.
  - Vortex mixer (Brand new), Make: Fisher Scientific, Serial: 16070506.
  - Autoclave (Sterilmatic), Model: STMEX, S/N: 212637, Calibration: Feb 2017 & 2018.
  - Centrifuge (Thermo Scientific Sorval ST 40), S/N: 41035124, Calibration: Feb 2017 & 2018.
  - Vacuum pump (Brand new), Model: 7100561, Serial: 0100000070.
  - Spectrophotometer (DR/2500), Make: HACH, S/N: 03070005726, Calibration: Mar 2017 & 2018.
  - Water bath (Fisher Scientific), Model: FB60301, S/N: 9A1050005, Calibration: Mar 2017.
- Calibration dates cover multiple instruments across 2017 and 2018.

## Quality control and procedures
- Use of sterile distilled water blanks as quality controls for all microbiological tests.
- Consistent assignment of tests to the same group of analysts within each sampling campaign to reduce variability.

## Data management implications for data leaders
- Clear definition of data units and measurement scales across multiple related files enhances discoverability and interoperability.
- Documentation of master solution composition, dilution factors, and detection limits supports reproducibility and traceability of results.
- Calibration records and QC practices strengthen data reliability and auditability.
- The presence of TNTC indicators and defined maximums highlights the need for consistent handling of overflow data in analyses.
- Fragmented data across six files with similar data structures suggests opportunities for integrated metadata schemas and unified data governance to address data standardization and discoverability.