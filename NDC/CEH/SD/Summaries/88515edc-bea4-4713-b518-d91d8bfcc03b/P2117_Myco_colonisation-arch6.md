# Measurements of nutrient cycling within grassland mycorrhizal mycelial networks

- Overview
  - Data from the NERC Soil Biodiversity Thematic Programme (1999–) investigating nutrient cycling and mycorrhizal networks in grassland.
  - Focuses on measurements of nitrogen (N) and phosphorus (P) in roots and shoots to study arbuscular mycorrhizal (AM) mycelia functioning in soil.
  - Dataset output from Project 2117: “The effect of mycorrhizal mycelium on the diversity, biomass and functioning of soil microbial communities and its role in carbon and nutrient cycles.”

- Context and aims
  - The programme aimed to understand soil biota biodiversity and functional roles in key ecological processes (soil structure, carbon/nitrogen cycles, microfauna/flora).
  - The data enable functional studies of AM networks within natural grassland systems.

- Site description
  - Sourhope field site, Scotland: large intact grassland monoliths installed in plastic boxes at the University of Sheffield Experimental Gardens.
  - Grassland is species-rich (24 higher-plant species; 21 with AM associations); soils are acid brown earths (pH 4.5–5.0) with 25% organic carbon.
  - Cores and monoliths designed to maintain a closed turf environment for controlled study.

- Core design and experimental framework
  - Cores: ABS tubes with four window openings (~50% of below-ground surface) covered with 35 μm nylon mesh; permeable base for drainage.
  - Control cores: identical but without windows to exclude AM hyphal in-growth.
  - Two experiments conducted using these cores:
    - Experiment 1: effect of hyphal severance on AM colonization of bait plants inside cores.
    - Experiment 2: effect of severance on transfer of 33P from soil cores to surrounding turf.

- Experiment 1 — experimental design and measurements
  - 42 cores total: 28 with mesh barriers, 14 solid; arranged in a random grid across three turf blocks.
  - Bait plants: Trifolium repens (2-week-old seedlings) established in half of the cores.
  - Monitoring and manipulation: half of mesh cores rotated weekly (~45°) to break penetrating hyphae; plant-free cores used to measure extractable AM mycelium.
  - Duration: May–July 2000 (11 weeks total).
  - Assessments:
    - Mycorrhizal colonization of bait plants (root staining, microscopy) and total root colonisation (%).
    - Shoot analyses: total N and P contents; N:P ratio.
    - Root length measurements (grid intercept method).
    - Hyphal length assessment in rotated vs static cores.

- Experiment 2 — experimental design and measurements
  - Setup: turf blocks in pots with two mesh-bound cores per pot, containing soil, maintained plant-free for 12 weeks for AM in-growth.
  - Labeling: 33P (phosphorus-33) injected into core centers in four pots; rotation applied to some cores to disrupt hyphal connections.
  - Treatment: some cores rotated during the experiment, others left static; rotation resumed after specific harvests.
  - Duration: up to 201 days post-labeling with multiple harvests.
  - Assessments:
    - Plant sampling: live shoot biomass harvested at multiple time points (3, 16, 40, 73, 110, 158, 201 days); shoot N and P contents; total shoot P uptake via 33P tracing.
    - Soil cores: water-extractable 33P at final harvest to determine residual availability.
    - Total 33P in shoots and soils measured via liquid scintillation counting.

- Measurements and analytical methods
  - Nitrogen and phosphorus: digestion and colorimetric methods (salicylic/sulphuric acid-lithium sulphate for N; appropriate procedures for P) with standard references.
  - AM colonization: root clearing, staining (trypan blue), and scoring (McGonigle et al., 1990); root length by grid intercept.
  - Hyphal length: methods following Brundrett et al. (1994).
  - 33P tracing: radioactive counting after sample preparation; apparatus calibrated for quench, decay, and background corrections.
  - PME (phosphomonoesterase) activity: measured in soil as part of 33P uptake assessment.
  - Quality control: numeric range checks, formatting checks, and logical integrity checks applied to data.

- Data structure and files
  - Three CSV data files are provided:
    - P2117_MYCORRHIZAL_COL_BIO_1.csv (Dataset reference 1077): Mycorrhizal colonisation of Agrostis capillaris bioassay plants; variables include SAMPLE_ID, SAMPLING_DATE, BLOCK, TREATMENT, TOTAL_ROOT_COL, SHOOT_N_CONC, SHOOT_P_CONC, SHOOT_RATIO_N_P, SHOOT_N_CONTENT, SHOOT_P_CONTENT, ARBUSCULES, VESICLES, etc.
    - P2117_MYCORRHIZAL_COL_BIO_2.csv (Dataset reference 1078): Mycorrhizal colonisation of Trifolium repens roots; includes AREA, MESH_CORE, and similar nutrient/colonisation variables.
    - P2117_PLANT_UPTAKE_PHOS_33.csv (Dataset reference 1079): Plant uptake of 33P; variables include MESH_CORE, DAYS_POST_LABEL, PME, and related shoot/soil 33P measures.
  - Data notes:
    - Missing values indicated (null or -999 in Part2); sampling dates and units specified; dataset references to Scott et al., 2003 and related sources.
    - Quality control steps described; NERC disclaims liability for data accuracy or fitness for a particular use.

- References and governance
  - Key methodological references for AM research and soil biodiversity methods (e.g., Bremner & Mulvaney; Brundrett et al.; McGonigle et al.; Tennant; Usher et al.).
  - SOURHOPE FIELD DATA HANDBOOK (2003) and related supporting information.
  - Data are provided with QA checks but without guaranteed accuracy; intended for use in further analyses and interpretation of AM nutrient cycling.