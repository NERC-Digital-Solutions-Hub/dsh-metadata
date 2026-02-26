# Nature and Units of recorded values, Calibration and Quality control

- This document describes the nature and units of data collected for isolating novel Bacteroides spp. hosts to assess faecal contamination of water, and its use alongside established markers (Bacteroides fragilis GB124, somatic coliphages, and faecal indicator bacteria).

## Nature and units by file

- LocationOfFaecalSampling.csv
  - Units pertain to sampling locations: latitude and longitude in decimal degrees; altitude in metres.

- IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Units include sampling location coordinates (latitude, longitude, altitude).
  - Bacterial counts reported as CFU (colony forming units) recovered from diluted faecal samples.
  - Master faecal solution composition and weighting details:
    - Master solution: 5 g faeces + 5 mL Ringers solution.
    - Dilution steps with defined mass-to-volume relationships (e.g., 1 mL master solution corresponds to 0.1 g faeces; 100 µL corresponds to 0.001 g faeces; etc.).
  - Analytical performance details:
    - Limit of detection (LOD) = 1 CFU per 0.0001 g faeces.
    - Maximum detected value = 16 CFU per 0.001 g faeces.
    - TNTC = Too Numerous To Count.

- IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Units are CFU (colony forming units); CFU counts were not considered at this step.
  - Data categorize results by esculin reaction (positive/negative) and growth condition (anaerobic/aerobic).

- IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Uses criteria similar to IsolationOfBacteroidesHostsWeek10-6-18StepA.csv.

- IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Uses criteria similar to IsolationBacteroidesHostsWeek10-6-18StepB.csv.

- DetectionOfFIB&MSTmarkers.csv
  - Faecal indicator bacteria (FIB): enterococci, total coliforms, Escherichia coli.
  - Measured units: CFU per 100 mL for water samples.
  - Somatic coliphages and Bacteroides fragilis GB124 phages; and phages for new hosts: measured in PFU per mL.
  - Ranges:
    - FIB: lowest 1 CFU/100 mL; maximum 720,000 CFU/100 mL; TNTC when numerous.
    - Phages: lowest 1 PFU/1 mL; maximum 740 PFU/1 mL; TNTC when numerous.
  - Note: Data reflect testing in drinking water sources and effluents from wastewater treatment plants.

## Calibration details

- Instrumentation and calibration dates are provided to ensure data quality and comparability:
  - Incubator (Orbital), Stuart SI500, SN R00100407 — Calibration dates: February 2017 & 2018.
  - Vortex mixer (Mini vortex), Fisher Scientific — Calibration date: Brand new.
  - Autoclave (Sterilmatic, STMEX) — Calibration dates: February 2017 & 2018.
  - Centrifuge (Thermo Scientific, Sorval ST 40) — Calibration dates: February 2017 & 2018.
  - Vacuum pump (Thomas) — Calibration date: Brand new.
  - Spectrophotometer (DR/2500, HACH) — Calibration dates: March 2017 & 2018.
  - Water bath (Fisher Scientific) — Calibration date: March 2017.
- These calibration details accompany the instrument set used for the analyses.

## Quality control

- Sample blanks consisted of sterile distilled water and were run on all microbiological tests.
- To reduce variability, the same group of analysts performed the individual tests during each sampling campaign.

## Data interpretation and analysis notes

- Data are spread across multiple files with differing units (CFU per gram faeces, CFU per 100 mL, PFU per mL), requiring careful standardization for cross-file analyses.
- Detection limits and TNTC statuses are explicitly defined, affecting downstream statistical handling and interpretation of low-abundance signals.
- Master solution composition and dilution mechanics are described, enabling reproducibility and traceability of CFU calculations from sample to final counts.