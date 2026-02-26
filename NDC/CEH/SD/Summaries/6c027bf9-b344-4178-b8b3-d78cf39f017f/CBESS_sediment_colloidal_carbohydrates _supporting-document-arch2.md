# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment colloidal carbohydrate concentration in saltmarsh and mudflat habitats

- Overview
  - Dataset of colloidal carbohydrate concentration in surface sediments, expressed as glucose equivalents (µg g-1).
  - Focuses on two coastal habitats: saltmarsh and mudflat.
  - Part of the CBESS project, collected during winter and summer 2013.
  - Staff: Jack Maunder.

- Study design and locations
  - Sites: 
    - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
    - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
  - Rationale: Essex and Morecambe Bay sites chosen to represent contrasting habitats and sediment types (clay soils in Essex; sandy soils in Morecambe Bay; differing inundation, creek structure, and vegetation).
  - Habitats sampled: mudflat and saltmarsh at each site.
  - Quadrat layout: 22 random 1 x 1 m quadrats per mudflat and per saltmarsh site, assigned using R to specify four spatial scales.

- Measurements and parameters
  - Primary variable: Colloidal carbohydrate concentration in sediment, reported as µg g-1 (glucose equivalents).
  - Replicates: Five replicates within each quadrat.
  - Seasons: Winter (W) and Summer (S) 2013.

- Sampling and laboratory methods
  - Field collection: contact cores collected; location coordinates and quadrat IDs recorded.
  - Sample processing:
    - Freeze top 2 mm of sediment with liquid nitrogen; store below -80°C.
    - Weigh wet weight; freeze-dry to remove moisture.
    - Sub-sample (50–500 mg) from dried sediment; add known volume of distilled water.
    - Vortex, centrifuge, and extract supernatant.
    - Chemical assay: Dubois Phenol-Sulphuric method with sulfuric acid and phenol (ratio 1:1:5, sample:phenol:acid).
    - Color development for 35 minutes; measure absorbance at 486.5 nm (spectrophotometer).
    - Calculate colloidal carbohydrate concentration using regression standards; report as µg g-1.
  - Detection: zeroes indicate concentrations below detectable level.

- Calibration, quality control and data integrity
  - Calibration: spectrophotometer accuracy checked using known glucose standards.
  - Lab protocols followed for scale calibration and sample processing consistency.
  - Units and data quality: wet and dry weights recorded to enable water content calculations; spectrophotometer readings and standard curves used for concentration calculations; notes on missing data (NA) if quadrats were inaccessible.

- Data structure and formats
  - Data format: CSV (comma-separated values).
  - Key columns:
    - Row Number: sortable identifier.
    - Season: Winter (W) or Summer (S).
    - Location: Essex (E) or Morecambe (M).
    - Site: AH, FW, TM (Essex); CS, WS, WP (Morecambe).
    - Habitat: Mudflat (MF) or Saltmarsh (SM).
    - Quadrat Number: 1–22.
    - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to site maximum).
    - Colloidal Carb (µg g-1): average concentration.
    - StDev: standard deviation of the concentration.
  - Notes: NA indicates missing data due to inaccessible quadrat.

- Temporal scope and updates
  - Sampling occurred during winter and summer 2013; no planned repeat sampling described.

- Accessibility and data management
  - Data are organized for clear interpretation and integration with environmental monitoring outputs (maps, charts, reports).
  - Data management aligns with CBESS practices for storing and sharing monitoring datasets.