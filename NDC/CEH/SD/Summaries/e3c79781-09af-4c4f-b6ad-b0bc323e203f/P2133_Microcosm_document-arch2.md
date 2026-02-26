# Plant biomass, soil conditions and stable isotope concentrations in soil, roots and shoots from a microcosm experiment [NERC Soil Biodiversity Programme]

- Overview:
  - Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on soil biodiversity and functional roles of soil organisms.
  - Large-scale field experiment at Sourhope, Scotland; 24 research projects studied soil structure, processes (C and N cycles), and faunal roles across microfauna, mesofauna, and macrofauna.
  - Data collection aimed at understanding how soil biota diversity and composition influence microbial abundance and plant–microbe interactions, particularly for organic nitrogen.

- Experimental design (Materials and methods):
  - Microcosms: 7 cm diameter × 6 cm depth pots with defaunated Sourhope soil, re-inoculated with microbes; maintained at 60% moisture.
  - Plant system: Agrostis capillaris grown in a 2:1:1 mix with added phosphorus source; AM fungal inoculum included.
  - Faunal manipulations: eight single-species treatments and diverse communities (two, four, eight species); species selected from Sourhope site and lab cultures; included two oribatid mites, several collembolans, and a predatory mite.
  - Biomass and sampling: plants partially harvested during the experiment and at final harvest; 190 microcosms in randomized block design; repeated watering to maintain weight.
  - Isotopic labelling: after 4 months, a pulse of glycine labelled with 15N and 13C was applied to trace N and C transfer to plants and microbial biomass; control treatments received unlabelled glycine.
  - Harvest and analysis timing: destructive harvest after 50 hours post-labelling to assess plant–microbe competition for organic nitrogen.

- Measurements and outputs (plant, soil, and microbial assessments):
  - Plant biomass: shoot dry weight and root biomass; shoot samples dried for isotopic analysis.
  - Mycorrhizal assessment: percentage root length colonised by AM fungi via staining and microscopy.
  - Soil and microbial biomass: microbial biomass carbon (MBC) and nitrogen (MBN) via fumigation-extraction; total soil nitrogen and carbon components.
  - Nutrient pools: soil extractable ammonia, nitrate, and phosphate.
  - Isotopic analyses: 15N and 13C ratios in roots, shoots, and soil; δ-notation used; analyses via isotope ratio mass spectrometry and elemental analysis.
  - Additional measurements: total organic carbon in extracts; AM colonisation scoring; multiple quality checks to ensure data integrity.

- Data structure and content (Dataset 1049: Microcosm nitrogen pulse P2133_MICROCOSM_N_PULSE.csv):
  - Key columns include:
    - POT_NUMBER: microcosm identifier.
    - GLYCENE_LABELED: whether glycine was labelled or unlabelled (control).
    - WATER_TREATMENT: watered or drought conditions.
    - BLOCK: experimental block number (1–5).
    - Presence/absence indicators for faunal taxa (e.g., ONYCH for Protaphorura armata; SCHEL for Scheloribates laevigatus; ISOT for Isotoma anglicana; MESA for Mesaphorura macrochaeta; PLATY for Platynothrus peltifer; PSEU for Pseudosinella alba; HYPO for Hypoaspis aculeifer; FOLS for Folsomia quadrioculata; PRED for the predatory mite Hypoaspis aculeifer).
    - PERCENT_RLC: mycorrhizal abundance – root length colonised (%).
    - Shoots and roots biomass: CUT1_SHOOT_1, CUT2_SHOOT_1, CUT3_SHOOT_0 with units (g); ROOT biomass.
    - MBC and MBN: microbial biomass carbon and nitrogen (mg/g).
    - AMMONIA, NITRATE, PHOSPHATE: soil extractable nutrient amounts (mg/g).
    - ISOT, ROOT_D15N, ROOT_PERCEN T_TOTAL_C, ROOT_D13C, SHOOT_PERCEN T_TOTAL_N, SHOOT_D15N, PERCENT_SOIL_TOTAL_N, SOIL_D15N, and related isotope-related fields for soil, root, and shoot samples.
    - Various derived isotopic measurements for non-fumigated and fumigated samples (e.g., MGN_UNFUMIGATED_SAMPLE, D15N_UNFUMIGATED_SAMPLE, MGN_FUMIGATED_SAMPLE, D15N_FUMIGATED_SAMPLE).
  - Data format: comma-separated values with explicit field descriptions, data types, units, and provenance notes.
  - Laboratories and provenance: isotopic analyses conducted at the Stable Isotope Facility (Centre for Ecology & Hydrology Merlewood) and related laboratories; plant and soil measurements performed at soil ecology laboratories (Lancaster University, etc.).

- Quality assurance and limitations:
  - Quality control included numeric range checks, data formatting checks, and logical integrity checks.
  - Data are subject to QA procedures but not guaranteed to be accurate; not liable for fitness for a particular use.
  - Datasets are provided as-is, with caveats on accuracy and suitability for end-use investigations.

- Context and references:
  - Related publications and methodological references underpinning the study, including work on plant–microbe competition for nitrogen and soil faunal influences on microbial abundance.
  - Data accessibility notes reference the SOURHOPE FIELD DATA HANDBOOK and related UK soil biodiversity literature for context and metadata.

- Relevance for environmental monitoring and analysis:
  - Demonstrates standardised, traceable data collection and analysis on soil biodiversity, plant–microbe interactions, and soil nutrient cycling.
  - Provides a comprehensive, multi-taxa microcosm dataset with robust QA practices and detailed metadata for cross-study comparability.
  - Aligns with monitoring aims to document environmental health and policy performance through consistent data formats, clear outputs (biomass, nutrient pools, isotopic tracers), and accessible data structures for reuse and integration.