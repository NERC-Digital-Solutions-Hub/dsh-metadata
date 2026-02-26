# Moth counts on chalk grassland and surrounding arable fields with agri-environment schemes in Hampshire, 2014

- Study aims and scope
  - Landscape-scale study of interactions between agri-environment schemes (AES) on arable-field margins and long-standing chalk grassland (CG) habitat.
  - Four landscapes in north-west Hampshire near Andover, each adjacent to a large CG patch within an SSSI and with extensive surrounding arable land.
  - Focus on macro-moth communities (180 species) and habitat specialism (CG-associated, grassland-associated, other).

- Experimental design and locations
  - Four study landscapes (a–d) selected; each contains a CG patch and surrounding arable fields.
  - AES interventions studied: 6-meter wide grassland margins (6m buffer strips) and nectar flower mixes.
  - Within landscapes: 18 survey locations (two on CG, 16 on arable fields).
  - Survey layout across arable fields: margins (AES-treated) vs field centers (control) across field pairs; within CG, locations surveyed without margin/centre distinction.
  - Sampling period: June 2 to July 22, 2014; six consecutive good-weather nights per landscape.

- Field sampling and instrumentation
  - Ten Heath-style actinic light traps (15 W) deployed each night, one per survey location across eight arable fields and CG locations.
  - On arable fields: traps alternating between margin (5 m from boundary) and centre (45 m from boundary); CG locations surveyed twice as often as margins/centres.
  - Weather criteria: minimum temperature > 10°C, wind < 20 km/h, precipitation risk < 50%.
  - Specimens identified on-site or via photographs; GPS recorded trap locations; equipment included collapsible wooden stands and SLA batteries.

- Data collected and structure
  - Data fields include:
    - date (YYYYMMDD), landscape (three-letter codes STO, BUR, BRO, DAN), field (landscape code + number + A/B for arable margins vs CG), location (0 = 45 m from boundary; 1 = 5 m from boundary on arable fields; CG locations use a paired coding), OS_x/os_y (GB National Grid), management (chgr, aesi1, ctrl1, aesi0, ctrl0), connect_CG (connectivity metric), species (180 macro-moth taxa), specialism (oth, gra, cgr), count (individuals per trap per night).
  - Data describe 24 nights total (6 per landscape) with counts across 180 moth species, including CG and other grassland specialists.
  - Species and habitat classifications follow Waring & Townsend (2009) for habitat specialism.

- Analytical methods and connectivity metric
  - Connectivity to chalk grassland (CG) estimated using a 100×100 m raster of CG coverage around Hampshire.
  - Connectivity for each cell i computed via a negative exponential dispersal kernel:
    C_i = sum_j A_j * exp(-α d_ij) for j ≠ i,
    where A_j = % CG coverage in cell j, d_ij = Euclidean distance between cell centers, α = 2 (representing mean dispersal ≈ 1 km).
  - Connectivity values extracted for survey locations, then log2-transformed and centered on the landscape mean.
  - Analyses prepared with ArcMap 10.1 and R 3.0.3.

- Data quality and curation
  - Macro-moth records cross-checked by a local moth recorder.
  - Three singleton records flagged as likely incorrect were retained due to uncertainty; overall dataset remains small and transparent about potential misidentifications.
  - Metadata and supporting information linked to data (including methods and GIS sources).

- AES intervention details
  - 6m buffer strips (NE 2012): paid ~£340 per hectare; width 6m; establishment by natural regeneration or grass sowing; annual cutting of the inner 3 m; no fertilisers; targeted herbicides if needed.
  - Nectar flower mix (EF4): paid ~£450 per hectare; width >6 m; establishment by sowing a mix of at least four nectar-rich species; management includes cutting half the strip in summer and the entire strip to 10 cm in autumn; no pesticides or fertilisers; re-establishment if needed.

- Notable features and availability
  - All data used in the associated analysis described by Alison et al. (in press) in the Journal of Applied Ecology.
  - Supporting information and data sources include HBIC/Natural England mapping data, ArcMap, and R tooling.
  - Data designed to be discoverable and reusable with metadata; intended for evaluating how AES design and landscape connectivity influence macro-moth communities and habitat specialists.

- Implications for questions and analyses
  - Enables investigation of: 
    - How AES margin type and location (margin vs centre) influence moth abundance and species richness, particularly CG- and grassland-associated species.
    - The role of connectivity to CG in shaping moth responses to AES.
    - Differences between CG and arable-field moth assemblages across connectivity gradients and AES treatments.
  - Data structure supports species-level analyses, habitat specialization assessments, and landscape-scale ecological questions relevant to practitioners and researchers in conservation planning.