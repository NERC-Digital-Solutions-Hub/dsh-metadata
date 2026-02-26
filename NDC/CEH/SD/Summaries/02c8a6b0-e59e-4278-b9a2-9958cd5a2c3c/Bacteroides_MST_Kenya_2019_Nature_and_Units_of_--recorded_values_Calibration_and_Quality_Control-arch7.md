# Nature and Units of recorded values, Calibration and Quality control

- Purpose and scope
  - Describes processes for isolating novel Bacteroides spp. hosts to assess faecal contamination of water sources.
  - Includes six CSV files: five dealing with isolation of Bacteroides hosts (Steps A/B across two weeks) and one integrating FIB (faecal indicator bacteria) and MST markers with viral indicators.
  - Emphasizes measurement units, calibration of equipment, and quality control.

- Data Files and Units
  - File 1: LocationOfFaecalSampling.csv
    - Units relate to sampling locations.
    - Latitude and Longitude: decimal degrees; altitude: metres.
  - File 2: IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
    - Location coordinates: decimal degrees (lat/long); altitude (metres).
    - Bacterial counts reported as colony forming units (CFU) from diluted faecal samples.
    - Table 1: Master faecal solution composition (5 g faeces + 5 mL Ringer’s solution; detailed weight-volume conversions).
    - Quantitative notes:
      - Limit of detection (LOD): 1 CFU per 0.0001 g faeces.
      - Maximum detected: 16 CFU per 0.001 g faeces.
      - TNTC: Too Numerous To Count.
  - File 3: IsolationBacteroidesHostsWeek10-6-18StepB.csv
    - CFU units; confirmatory step for host isolation.
    - Categories: Positive/Negative Esculin reaction and Aerobic/ Anaerobic conditions.
  - File 4: IsolationBacteroidesHostsWeek17-6-18StepA.csv
    - Similar criteria and units as StepA in File 2.
  - File 5: IsolationBacteroidesHostsweek17-6-18StepB.csv
    - Similar to StepB criteria as in File 3.
  - File 6: DetectionOfFIB&MSTmarkers.csv
    - Faecal indicator bacteria (FIB): intestinal enterococci, total coliforms, Escherichia coli.
    - Measured in CFU per 100 mL; range: lowest 1 CFU/100 mL to max 720,000 CFU/100 mL; TNTC indicates too numerous to count.
    - Viral indicators: somatic coliphages; phages infecting Bacteroides fragilis GB124 and new Bacteroides hosts; measured in plaque forming units per mL (PFU/mL); range: 1 PFU/mL to 740 PFU/mL; TNTC as above.

- Calibration
  - Table 2 details instrument types and calibration dates (Feb 2017 & 2018 for multiple instruments).
  - Instruments and examples: incubator, vortex mixer, autoclave, centrifuge, vacuum pump, spectrophotometer (DR/2500), and water bath.
  - Calibration ensures accuracy of the microbiological measurements and associated quantitative data.

- Quality Control
  - Use of sample blanks: sterile distilled water run on all microbiological tests.
  - Consistent analysts across a sampling campaign to reduce variability.

- GIS and data integration relevance
  - Spatial data: coordinates (latitude/longitude) and altitude enable geospatial mapping of sampling sites.
  - Multimodal measurements: CFU counts (faecal bacteria) and PFU counts (phages) across water and faecal samples allow spatial analysis of contamination indicators.
  - Data harmonization considerations: varying resolutions and multiple tables/units (CFU per sample weight, CFU per 100 mL, PFU per mL); need standardization for map-based visualization and cross-dataset comparisons.
  - Metadata needs: clear ties between sample IDs, locations, dates, and measurement units to enable robust GIS analyses.