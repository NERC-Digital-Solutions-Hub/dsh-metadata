# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment colloidal carbohydrate concentration in saltmarsh and mudflat habitats

- Purpose: Dataset of colloidal carbohydrate concentration in surface sediments (glucose equivalents) to support understanding of coastal biodiversity and ecosystem service sustainability in saltmarsh and mudflat habitats.

- Observed variable: Colloidal carbohydrate concentration in surface sediments, expressed as glucose equivalents in micrograms per gram of sediment (µg g⁻¹).

- Sampling campaign and period:
  - Part of the CBESS field campaign (winter and summer 2013).
  - No planned repeat sampling.

- Study locations and sites:
  - Essex
    - Abbotts Hall (AH): 51.78°N, 0.87°E
    - Fingringhoe Wick (FW): 51.83°N, 0.97°E
    - Tillingham Marshes (TM): 51.68°N, 0.93°E
  - Morecambe Bay
    - Cartmel Sands (CS): 54.17°N, 3.00°W
    - Warton Sands (WS): 54.13°N, 2.80°W
    - West Plain (WP): 54.15°N, 2.97°W

- Habitat types and site selection rationale:
  - Saltmarsh sites chosen to represent contrasting soil types:
    - Essex: clay soils
    - Morecambe Bay: sandy soils
  - Essex and Morecambe saltmarsh regions also differed in inundation frequency, creek structure, and dominant vegetation.
  - Mudflat sites differed in sediment type:
    - Essex mudflats: cohesive clays, mud, and silt
    - Morecambe Bay mudflats: coarse, mobile sediments

- Sampling design and replicates:
  - Five replicates per quadrat on both mudflat and saltmarsh per season (winter and summer 2013).
  - Quadrats: 22 per site, 1 m x 1 m in size, with random allocation of quadrats.

- Spatial sampling scales and layout:
  - Four spatial scales for quadrat placement:
    - A: 1 quadrat (1 m scale)
    - B: 3 quadrats spaced 1–10 m apart
    - C: 6 quadrats spaced 10–100 m apart
    - D: 12 quadrats spaced 100 m to 1000 m (or site maximum)
  - Scale definitions were calibrated according to laboratory protocols; randomization performed with R.

- Field and laboratory procedures:
  - Core collection: sediment cores collected and processed (top 2 mm frozen with liquid nitrogen; sample stored at -80°C).
  - Preparation: wet weight measured; samples freeze-dried.
  - Analytical method: Dubois Phenol-Sulphuric assay to determine colloidal carbohydrate concentration.
  - Sample processing steps: sub-sample (50–500 mg), add distilled water, vortex, centrifuge, quantify supernatant, add sulfuric acid and 5% phenol, colour development (35 minutes), measure absorbance at 486.5 nm (spectrophotometer).
  - Quantification: concentration calculated from regression standards and expressed as µg g⁻¹.

- Data management and structure:
  - Data format: Comma separated values (.csv).
  - Primary fields (examples):
    - Season: Winter (W) or Summer (S)
    - Location: Morecambe (M) or Essex (E)
    - Site: CS, WS, WP (Morecambe) or AH, FW, TM (Essex)
    - Habitat: Mudflat (MF) or Saltmarsh (SM)
    - Quadrat Number: 1–22
    - Scale: A, B, C, D
    - Colloidal Carb (µg g⁻¹): average concentration
    - StDev: standard deviation of concentration
  - Additional metadata fields:
    - Row Number: nominal sort order
    - Data entries include descriptions of seasons, locations, sites, habitats, scales
  - Missing data: NA indicates missing data due to inaccessibility of the quadrat
  - Measurements include five replicates per quadrat; reported as average concentration with standard deviation

- Data quality and QA considerations:
  - Spectrophotometer accuracy checked using glucose standards.
  - Spatial scales and quadrat placement randomized and documented.
  - Measurement protocol and lab procedures described to support reproducibility.

- GIS-ready considerations:
  - Spatial coverage includes six sites across two regions (Essex and Morecambe Bay) with explicit site coordinates.
  - Data are polygon/area-based in concept (1 m x 1 m quadrats) within each site; exact quadrat coordinates are not provided in the dataset summary and would require reconstruction from the randomization design for precise GIS mapping.
  - Attributes suitable for GIS:
    - Site, Habitat, Season, Quadrat Number, Scale, Colloidal Carb (µg g⁻¹), StDev
  - Potential map products:
    - Quadrats or aggregated scales showing spatial patterns of colloidal carbohydrate concentration.
    - Habitat-specific contrasts (saltmarsh vs mudflat) within and across Essex and Morecambe Bay.
    - Temporal comparison between winter and summer 2013.