# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) plant height on salt marsh sites at Morecambe Bay and Essex

- Purpose and scope
  - Dataset of plant height measurements at salt marsh sites in Morecambe Bay and Essex, part of the CBESS project.
  - Aims to support analysis of coastal biodiversity and ecosystem service sustainability through fine-scale vegetation height data.

- Spatial and temporal coverage
  - Regions: Essex and Morecambe Bay.
  - Sites:
    - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
    - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
  - Coordinates (observations locations):
    - Essex: AH 51°47′N, 0°52′E; FW 51°49′N, 0°58′E; TM 51°41′N, 0°56′E.
    - Morecambe Bay: CS 54°10′N, 3°0′W; WS 54°8′N, 2°48′W; WP (West Plain) coordinates not explicitly listed here.
  - Habitat types: Saltmarsh (SM) and Mudflat (MF).
  - Scale categories: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit).

- Sampling design and methods
  - Sampling period: Winter and Summer 2013.
  - Within-quadrat sampling: Ten direct measurements of plant height (cm) taken randomly within each 1 m × 1 m quadrat using hand and meter rule.
  - Data collection personnel: Hilary Ford.

- Measurements and variables
  - Primary measurement: Plant height (cm) per observation.
  - Derived statistics per quadrat: Mean height (cm), SD (standard deviation), SE (standard error), CoV (coefficient of variation).
  - CoV usage: Used as a vegetation height diversity score (higher CoV indicates greater height diversity).

- Data structure and file formats
  - File format: Excel workbook.
  - Core data fields:
    - Row Number (sorting key)
    - Season (Winter W, Summer S)
    - Location (Morecambe M, Essex E)
    - Site (Essex: AH, FW, TM; Morecambe: CS, WS, WP)
    - Habitat (Mudflat MF, Saltmarsh SM)
    - Quadrat Number (1–22)
    - Scale (A–D)
    - H1–H10 (Plant height measurements in cm)
    - Mean Height (cm)
    - SD
    - SE
    - CoV

- Field descriptions and data schema
  - Row Number: Nominal sort order (Number)
  - Season: Winter (W) or Summer (S) (Text)
  - Location: Morecambe (M) or Essex (E) (Text)
  - Site: CS, WS, WP (Morecambe) or AH, FW, TM (Essex) (Text)
  - Habitat: MF or SM (Text)
  - Quadrat Number: 1–22 (Number)
  - Scale: A, B, C, D (Text)
  - H1–H10: Plant height measurements (cm) (Number)
  - Mean Height (cm): Mean of H1–H10 (Number)
  - SD: Standard deviation of H1–H10 (Number)
  - SE: Standard error of H1–H10 (Number)
  - CoV: Coefficient of variation (%) (Number)

- Quality control and provenance
  - Calibration procedures: None
  - Data checking procedures: Not specified beyond basic description

- Relevance for GIS work
  - Spatially explicit data at multiple salt marsh sites with precise coordinates and habitat context.
  - Enables mapping of plant height distribution and height diversity across sites, habitats, seasons, and scales.
  - Suitable for integration with other CBESS datasets to model vegetation structure and its relation to grazing, soil type, inundation, and ecosystem services.