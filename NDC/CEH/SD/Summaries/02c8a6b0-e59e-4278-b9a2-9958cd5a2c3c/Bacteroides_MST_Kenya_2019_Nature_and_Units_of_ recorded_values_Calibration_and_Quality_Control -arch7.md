# Nature and Units of recorded values, Calibration and Quality control

- Overview
  - Describes the nature and units of recorded values across six CSV files related to isolation of novel Bacteroides hosts to assess faecal contamination of water sources, plus the use of FIB and viral indicators.
  - Includes calibration details for instruments and quality control procedures.

- Data files and their units
  - File 1: LocationOfFaecalSampling.csv
    - Units pertain to sampling locations: Latitude and Longitude in decimal degrees; altitude in metres.
  - File 2: IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
    - Units include sampling location coordinates (Latitude/Longitude in decimal degrees; altitude in metres).
    - CFU-related data from diluted faecal samples; references to Master faecal solution preparation.
    - Master solution: 5 g faecal sample + 5 mL Ringers; conversion scales (e.g., 1 mL master = 0.1 g faeces, etc.).
    - Detection metrics: Limit of detection = 1 CFU per 0.0001 g faeces; Maximum detected = 16 CFU per 0.001 g faeces; TNTC (Too Numerous To Count).
  - File 3: IsolationBacteroidesHostsWeek10-6-18StepB.csv
    - Units: CFU (colony forming units); counts used for confirmatory step are not further quantified here.
    - Categorical results by combination of Esculin reaction (positive/negative) and Oxygen (Anaerobic/Aerobic), with corresponding CFU entries.
  - File 4: IsolationBacteroidesHostsWeek17-6-18StepA.csv
    - Similar structure and criteria as File 2 StepA.
  - File 5: IsolationBacteroidesHostsweek17-6-18StepB.csv
    - Similar structure and criteria as File 3 StepB.
  - File 6: DetectionOfFIB&MSTmarkers.csv
    - Faecal indicator bacteria (FIB): Intestinal enterococci, Total coliforms, Escherichia coli are given in CFU per 100 mL.
    - Range: Lowest detected 1 CFU/100 mL; Maximum detected 720,000 CFU/100 mL; TNTC possible.
    - Viral indicators: Somatic coliphages; Bacteroides fragilis GB124 phages; and phages for new Bacteroides hosts; measured in plaque forming units (PFU) per 1 mL.
    - Viral data ranges: Lowest detected 1 PFU/1 mL; Maximum 740 PFU/1 mL; TNTC possible.

- Calibration
  - Table 2 provides instruments and calibration details used in the study.
  - Instruments include: incubator, vortex mixer, autoclave, centrifuge, vacuum pump, spectrophotometer (DR/2500), and water bath.
  - Calibration dates: February 2017 and February 2018 for multiple items; some equipment listed as brand new (e.g., vortex); serial numbers and models provided as part of the calibration records.
  - Purpose: ensure measurement accuracy and consistency across microbiological and analytical procedures.

- Quality control
  - Sample blanks consisted of sterile distilled water and were included in all microbiological tests.
  - To reduce variability, the same group of analysts performed individual tests within each sampling campaign.

- GIS and data integration considerations
  - Spatial data are captured as latitude, longitude (decimal degrees), and altitude (metres) for sampling locations, enabling map-based visualization of sampling sites.
  - Data involve multiple measurement types (CFU, PFU) and multiple units (CFU/100 mL, PFU/mL), requiring standardization for cross-file comparisons.
  - Detection limits and TNTC notes affect how values are represented in maps and analyses (e.g., censoring or marking as TNTC).
  - Calibration information supports assessment of data reliability; important for conveying confidence in map products.
  - Fragmentation across six files means careful data stitching is needed to build coherent maps of sampling events, hosts isolation results, and FIB/marker concentrations.