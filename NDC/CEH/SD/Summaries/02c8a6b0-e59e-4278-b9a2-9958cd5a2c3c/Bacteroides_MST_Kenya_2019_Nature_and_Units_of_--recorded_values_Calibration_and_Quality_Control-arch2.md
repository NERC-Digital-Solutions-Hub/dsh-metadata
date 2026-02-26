# Nature and Units of recorded values, Calibration and Quality control

- Purpose and scope
  - Describes nature and units of recorded values for six CSV files related to isolating novel Bacteroides spp. hosts and using them with established markers (Bacteroides fragilis GB124, somatic coliphages, and faecal indicator bacteria) to assess faecal contamination in water sources.
  - Supports monitoring environmental water quality and enables comparison across campaigns with standardized data definitions.

- File 1: LocationOfFaecalSampling
  - Units: geographic coordinates and altitude
    - Latitude: decimal degrees
    - Longitude: decimal degrees
    - Altitude: metres

- File 2: IsolationOfBacteroidesHostsWeek10-6-18StepA
  - Units: location coordinates (lat, lon, alt) and bacterial counts
    - Latitude, Longitude: decimal degrees
    - Altitude: metres
    - Colony forming units (CFU) recovered from diluted faecal samples
  - Master faecal solution details
    - Composition described (master solution made from faecal material and Ringer’s solution) and dilution scheme
  - Key quantitative notes
    - Limit of detection (LOD): 1 CFU per 0.0001 g faeces
    - Maximum detected value: 16 CFU per 0.001 g faeces
    - TNTC: Too Numerous To Count

- File 3: IsolationBacteroidesHostsWeek10-6-18StepB
  - Units: CFU with categorical esculin reaction and oxygen condition
    - Positive/Negative Esculin reaction
    - Anaerobic or Aerobic environments
  - Purpose: confirmatory step for isolation of suitable Bacteroides hosts; CFU counts recorded but not treated as quantitative in this step

- File 4: IsolationBacteroidesHostsWeek17-6-18StepA
  - Similar units and criteria as Week10-6-18 StepA

- File 5: IsolationBacteroidesHostsweek17-6-18StepB
  - Similar units and criteria as Week10-6-18 StepB

- File 6: DetectionOfFIB&MSTmarkers
  - Faecal indicator bacteria (FIB) and phage markers
    - FIB: intestinal enterococci, total coliforms, Escherichia coli
    - Markers: somatic coliphages; phages infecting Bacteroides fragilis GB124; phages infecting novel Bacteroides hosts
  - Measurement units
    - FIB: CFU per 100 mL (CFU/100 mL) in drinking water and WWTP effluents
    - Phages: plaque forming units per 1 mL (PFU/1 mL)
  - Data ranges
    - FIB: lowest 1 CFU/100 mL; maximum detected 720,000 CFU/100 mL; TNTC when counts are too numerous
    - Phages: lowest 1 PFU/1 mL; maximum detected 740 PFU/1 mL; TNTC when plaque-forming units are too numerous to count

- Calibration
  - Instruments and calibration dates
    - Incubator (Orbital, Stuart SI500, serial R00100407): calibrated February 2017 & 2018
    - Vortex mixer (Mini vortex): calibration July 2016 (listed as brand new elsewhere; used as reference)
    - Autoclave (Sterilmatic STMEX): calibrated February 2017 & 2018
    - Centrifuge (Thermo Scientific Sorval ST 40): calibrated February 2017 & 2018
    - Vacuum pump (Thomas, 230V): brand new calibration noted
    - Spectrophoto metre (DR/2500, HACH): calibrated March 2017 & 2018
    - Water bath (Fisher Scientific): calibrated March 2017
  - Purpose: ensure consistency and accuracy of analytical measurements across campaigns

- Quality control
  - Blanks: sample blanks using sterile distilled water included in all microbiological tests
  - Consistency: same group of analysts conducts individual tests within each sampling campaign to reduce inter-operator variation

- Data management and usage notes
  - Emphasis on storing and uploading generated datasets to appropriate portals to preserve data accessibility and reuse
  - Data are organized to support standardized reporting of environmental health and policy performance over time through consistent units, calibration, and QA practices