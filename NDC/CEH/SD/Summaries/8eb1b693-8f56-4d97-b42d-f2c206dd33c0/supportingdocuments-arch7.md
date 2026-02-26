# Data structure

- Purpose and setup
  - Study of ECM fungi growth under nutrient variation to create structured, numeric data suitable for analysis and visualization.
  - 7 fungal isolates tested across 9 treatments varying nitrogen (N) and phosphorus (P) sources.

- Fungal isolates and identities
  - Laccaria bicolor (lb101B)
  - Laccaria amethystina (la56)
  - Paxillus involutus (Pi47)
  - Piloderma byssinum (PbUP185)
  - Suillus bovinus (O96)
  - Suillus viscidus (Sv171)
  - Suillus viscidus (SvAFST1)

- Experimental design and culture conditions
  - Fungi cultured at 18°C on 1 L control MMN nutrient agar, pH 5.5, with glucose as carbon source.
  - MMN base supplemented with trace elements (MgSO4·7H2O, CaCl2, FeCl3, NaCl).
  - Nine MMN formulations differed only in N and P sources; other components remained constant.
  - Nitrogen sources: inorganic NH4NO3; organic N glycine, glutamines, glutamic acid, phenylalanine.
  - Phosphorus sources: inorganic KH2PO4; organic phytic acid dipotassium salt.

- Measured variables and data structure
  - Data are numerical continuous variables organized by experimental treatments.
  - Columns described as:
    - Isolate: reference name of the ECM fungal isolate.
    - B: abbreviation for agar composition corresponding to N and P treatment.
    - C: nitrogen treatment category (Inorganic N, Organic N, or NoN).
    - D: phosphorus treatment category (Inorganic P, Organic P, or NoP).
    - E: growth rate over 52 days, measured as millimeters per day.
    - F: biomass, mass of fungal hyphae per unit area (g dry weight per cm^2).
  - Measurements:
    - Colony diameter measured daily over 57 days.
    - Biomass determined by freeze-drying harvested mycelia and weighing.

- Data organization and potential for GIS-ready structures
  - A compact, tabular dataset linking fungal isolate, nutrient treatment, and two response variables (growth rate and biomass).
  - Suitable for multi-criteria visualization or map-based dashboards when combined with metadata (isolate provenance, treatment codes, and measurement timelines).
  - Clear units and standardized categories support integration with other datasets and reproducibility across analyses.

- Notes on interpretation and consistency
  - There is an implied 52-day window for growth-rate calculation, while diameter measurements were taken over 57 days, indicating a potential mismatch to address during data curation.
  - The dataset emphasizes structure and comparability across isolates and nutrient treatments, enabling comparative visualizations of growth dynamics and biomass under different N and P regimes.