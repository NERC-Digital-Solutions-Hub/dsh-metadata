# Experimental Design and Laboratory Incubation Method

- Purpose: Assess microbial metabolic activity in riverine sediments using a resazurin-resorufin tracer, across different sediment substrates and incubation temperatures; generate a dataset suitable for analysis of gas production (CO2, CH4), resorufin production, and dissolved oxygen.

- Sampling and substrates
  - Sediment collection: upper 10 cm from two rivers in September 2015:
    - River Lambourn (Chalk geology)
    - River Tern (Sandstone geology)
  - Sampling details: three samples per river from three areas per site
  - Substrate treatments (six total): Chalk fine, Chalk medium, Chalk coarse, Sandstone fine, Sandstone medium, Sandstone coarse
  - Control: 500 mL ultrapure water in jars (no sediment)
  - Sample preparation: homogenised, sieved (0.8 cm for fine; 1.6 cm for medium and coarse)

- Incubation design
  - Temperature treatments: 5, 9, 15, 21, 26°C
  - Incubation setup: 300 mL sediment + 500 mL ultrapure water per jar, sealed in 1 L amber jars
  - Replication: triplicate for each substrate treatment plus controls (7 substrate treatments total), resulting in 21 observations per temperature, 105 observations overall
  - Time points: 0 hours and 5 hours
  - Jar labeling: 1–21; Substrate_Type column indicates corresponding treatment (Chalk fine, Chalk medium, Chalk coarse, Sandstone fine, Sandstone medium, Sandstone coarse) across triplicates

- Measurements and tracers
  - Microbial activity tracer: resazurin-resorufin system; resorufin production serves as proxy for activity
  - Sampling protocol: measure initial (0 h) resorufin concentration and dissolved oxygen; collect headspace gas sample; repeat after 5 hours
  - Post-incubation: jars dried to determine sediment properties

- Instruments and calibrations
  - Gas analysis: CO2 and CH4 with Agilent 7890A GC-FID
    - Calibration: daily four-point standards (CO2: 0, 1051, 525.5, 262.8 ppm; CH4: 0, 9.8, 4.9, 2.5 ppm)
    - Performance checks with external standard and drift correction
  - Resorufin measurements: GGUN-FL30 fluorometer (customized; excitation at 525 nm for resorufin, 570 nm for resazurin)
    - Calibration: weekly three-point (zero, 100 ppb resorufin, resorufin/resazurin mix); standard 93.1 ppb resorufin for performance
    - Detection limit: 1 ppb resorufin
  - Dissolved oxygen: Pyro-science Firesting fixed needle-type sensor
  - DO and gas calibrations performed daily; zero-based and gas-phase checks included

- Data and units
  - Temperature: degrees Celsius
  - Organic matter: percent
  - CO2 production: mg C m^-2 h^-1
  - CH4 production: mg C m^-2 h^-1
  - Resorufin production: ng resorufin per µg resazurin per hour
  - Dissolved oxygen: mg L^-1

- Data structure (file and fields)
  - File: IncubationCO2_CH4_Resorufin_DO.csv
  - Columns:
    - Temperature: incubation temperature (°C)
    - Jar: jar number (1–21)
    - Substrate_Type: Chalk or Sandstone, with fine/medium/coarse classifications
    - Geology: river geology (Chalk or Sandstone); NA for controls
    - Organic_Matter: sediment organic matter content (%)
    - CO2: carbon dioxide production (mg C m^-2 h^-1)
    - CH4: methane production (mg C m^-2 h^-1)
    - Resorufin: resorufin production (ng resorufin per µg resazurin per hour)
    - Dissolved_Oxygen: DO at end of incubation (mg L^-1)

- Notes and references
  - Substrate treatment mapping corresponds to the three Chalk and three Sandstone categories including controls
  - Includes references related to online fluorometry and loss on ignition methodology for context on measurement approaches

- GIS relevance and potential visualizations
  - While the dataset is lab-based, it links sediment type (geology and substrate) with microbial activity metrics that can be spatially contextualized
  - Potential GIS applications:
    - Map microbial activity proxies (CO2/CH4 production, resorufin) by sediment geology and substrate class
    - Overlay with river basin geospatial layers (geology, sediment distribution) to explore spatial patterns
    - Enable policy and public-facing visuals showing environmental implications of sediment type and geology on gas production in streams
    - Integrate with broader hydrological or soil data to create map-based data products for stakeholders

- Quality and provenance
  - Detailed instrumentation and calibration procedures supporting data quality
  - Clear data structure with explicit units and replication scheme for reproducibility and integration with other datasets