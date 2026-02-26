# Moth counts on chalk grassland and surrounding arable fields with agri-environment schemes in Hampshire, 2014

- Overview
  - Landscape-scale study in north-west Hampshire, UK, investigating how agri-environment schemes (AES)—specifically 6 m buffer strips and nectar flower mixes—interact with protected chalk grassland habitat.
  - Data collected in 2014 across four landscapes adjacent to chalk grassland SSSI; 180 macro-moth species recorded in the study.
  - All data used in the associated analysis (Alison et al., in press) are included in this dataset.

- Study design and interventions
  - Study area: four landscapes near chalk grassland (CG) patches, each with >50% surrounding arable land up to ~3 km from CG.
  - AES interventions studied:
    - 6 m wide grassland buffer strips (EE3 option, payment ~£340/ha).
    - Nectar flower mixes (EF4 option, payment ~£450/ha).
  - Sampling framework:
    - 18 macro-moth survey locations per landscape (2 on CG habitat; 16 on arable field margins or centres across four field pairs).
    - Within arable fields: treatment margins (AES present) vs control margins (no AES); margins vs field centres (approx. 5 m from boundary vs 45 m from boundary).
    - Survey window: six consecutive good-weather nights per landscape between June 2 and July 22, 2014.
    - 10 light traps deployed each night to sample one survey location per arable field and two CG locations.

- Data collection methods
  - Trapping: Heath style actinic light traps (15 W) with solar sensors; traps recovered and counted at sunrise; on-site identification or photographic verification used.
  - Location sampling: traps positioned to minimize recaptures (≥50 m apart across visits); CG traps placed without margin/centre distinction.
  - Habitat and species data: site management codes (CG habitat, AES intervention margins, control margins, central arable field positions); species were categorized by habitat specialism (CG, grassland, other) based on Waring & Townsend (2009).
  - Geography and instrumentation: trap locations geolocated with GPS; equipment details (batteries, stands, GPS, transport) documented.

- Data structure and variables
  - Core fields include:
    - date: sampling night (YYYYMMDD).
    - landscape: three-letter code (STO, BUR, BRO, DAN) for study landscape.
    - field: five-character code (landscape code + field number + A/B) indicating arable field or CG section and AES treatment status.
    - location: six-character code (field code + 0/1) for specific survey point (0 = 45 m from boundary, 1 = 5 m from boundary on arable fields; CG locations use corresponding identifiers).
    - OS_x / OS_y: Ordnance Survey grid coordinates (metres).
    - management: habitat or AES status (chgr, aesi1, ctrl1, aesi0, ctrl0).
    - connect_CG: connectivity to CG (relative measure, derived).
    - species: scientific names of the 180 macro-moth species recorded.
    - specialism: habitat association category for each species (oth = other, gra = grassland, cgr = CG).
    - count: number of individuals of a species observed in a trap on a given night and location.
  - Data quality and validation notes:
    - Cross-checked by a local moth recorder; three singleton records flagged as unlikely but retained due to uncertainty and rarity.

- Analytical methods and connectivity metric
  - Connectivity to CG:
    - Built a 100×100 m raster of CG habitat coverage using HBIC/NE data.
    - Calculated cell-to-cell connectivity with a negative exponential dispersal kernel: C_i = sum_j A_j * exp(-α d_ij) for j ≠ i, with α = 2 representing a mean dispersal distance of ~1 km.
    - Extracted connectivity values for survey locations, then applied log2 transformation and centered on the landscape mean.
  - Tools:
    - GIS: ArcMap 10.1 for raster creation and landscape processing.
    - Statistical computing: R 3.0.3 for connectivity calculations and downstream analyses.

- Quality control and governance
  - Data verification performed by local experts; flagging of unlikely singleton records while preserving them for transparency.
  - Data sources and supporting information:
    - Natural England and HBIC datasets for CG coverage.
    - Supporting Information and data references provided (DOIs listed in the document) to enable replication and verification.
  - Metadata and data sharing:
    - Emphasis on clear metadata (structure, field definitions, codes) to support reuse; data formats and definitions are explicit, facilitating policy-relevant monitoring and evaluation.

- Relevance for monitoring frameworks and policy insights
  - Demonstrates a replicable, spatially explicit monitoring design to assess AES effects on a targeted insect assemblage.
  - Integrates landscape connectivity as a key ecological metric, linking habitat configuration to species occurrence.
  - Provides a comprehensive data structure and documentation (field codes, management categories, coordinates, species traits) to support governance, data sharing, and transparent reporting.
  - Highlights practical considerations for monitoring frameworks:
    - Benefits of standardized data schemas and metadata to reduce data silos and enable cross-study synthesis.
    - Importance of robust quality control and clear documentation to ensure data quality for policy evaluation.
    - Potential data governance barriers (e.g., data sharing requirements) and how explicit provenance and structure can mitigate them.