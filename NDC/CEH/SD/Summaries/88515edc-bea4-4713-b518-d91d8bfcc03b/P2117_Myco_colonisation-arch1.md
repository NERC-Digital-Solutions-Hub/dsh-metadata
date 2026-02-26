# Measurements of nutrient cycling within grassland mycorrhizal mycelial networks

- Background and aims
  - Part of the NERC Soil Biodiversity Thematic Programme (started 1999) studying soil biota and their functional roles in carbon and nutrient cycles.
  - Focuses on two related experiments measuring nitrogen (N) and phosphorus (P) in roots and shoots to understand arbuscular mycorrhizal (AM) mycelial networks and their role in nutrient cycling.
  - Site: Sourhope field site, Scotland; experiments use large intact grassland monoliths transplanted to controlled containers for functional study.

- Field site, design, and core construction
  - Grassland with diverse plant species; soils acidic with low organic matter, developed from local drift on andesitic lava.
  - Cores: ABS tubing (18 mm ID, 22 mm OD, 150 mm long) with four windows exposing about 50% of below-ground surface; nylon mesh (35 μm) to permit AM hyphae entry; some cores without windows to exclude AM hyphae.
  - Provision of a permeable base allowed drainage; rotation of some cores used to disrupt hyphal connections.

- Experimental overview
  - Experiment 1: Effect of hyphal severance on AM colonization of bait plants
    - 42 cores (28 mesh-open, 14 solid) arranged in turfs; bait plants were 2-week-old Trifolium repens seedlings, with herbivory protection.
    - Design included rotating mesh cores to break hyphae in half of the mesh cores; monitored AM colonization and nutrient status after about 10 weeks.
    - Measurements included shoot biomass, total N and P in shoots, AM colonization of roots (including arbuscules and vesicles), and root length via grid intercept method.
    - Additional assessment of AM hyphal lengths after incubation (rotated vs static cores).
  - Experiment 2: Effect of hyphal severance on transfer of 33P from cores to surrounding grassland turfs
    - Plant-free cores in blocks of turf placed into pots; after 12 weeks in-growth of AM mycelium, cores in some pots were rotated to disrupt connections.
    - Injected 33P-labeled phosphate into cores and tracked its distribution with time under rotating vs non-rotating conditions.
    - Harvest schedule spanned up to 201 days post-labeling, with repeated sampling of shoot biomass and total P, plus analysis of soil and plant 33P distribution.

- Data collected and analytical methods
  - AM colonization data
    - Root colonization (% AM) and arbuscule/vesicle presence following established staining and counting methods.
    - Measurements of root length to quantify colonization extent.
  - Plant nutrient content
    - Shoot nitrogen (N) and phosphorus (P) concentrations and contents.
    - Shoot N:P ratio as an indicator of nutrient balance.
  - 33P uptake and distribution
    - 33P content in shoots at multiple harvest times (to assess plant uptake of labeled P).
    - Water-extractable 33P from soils at final harvest to quantify residual or transferred label.
    - Radioactivity measured via liquid scintillation counting; correction for quenching, decay, and background.
  - Additional chemical measures and references
    - Methods include Kjeldahl/N determination, P determination, and AM root colonization assessment per McGonigle et al. (1990), among others.

- Data structure and files
  - Dataset 1: P2117_MYCORRHIZAL_COL_BIO_1.csv
    - Mycorrhizal colonisation of Agrostis capillaris bioassay plants grown in turves from control, lime, nitrogen, and combined lime+n dorms plots.
    - Key fields: SAMPLE_ID, SAMPLING_DATE, BLOCK, TREATMENT, TOTAL_ROOT_COL, SHOOT_N_CONC, SHOOT_P_CONC, SHOOT_RATIO_N_P, SHOOT_N_CONTENT, SHOOT_P_CONTENT, ARBUSCULES, VESICLES.
  - Dataset 2: P2117_MYCORRHIZAL_COL_BIO_2.csv
    - Mycorrhizal colonisation of Trifolium repens roots grown in sand-filled mesh cores in turves.
    - Key fields: SAMPLE_ID, AREA, TOTAL_ROOT_COL, SHOOT_N_CONC, SHOOT_P_CONC, SHOOT_RATIO_N_P, SHOOT_N_CONTENT, SHOOT_P_CONTENT, ARBUSCULES, VESICLES.
  - Dataset 3: P2117_PLANT_UPTAKE_PHOS_33.csv
    - Measurement of phosphorus-33 uptake from turfs by AM mycelium using mesh cores with soil injected with 33P; includes static vs rotated core comparisons.
    - Key fields: SAMPLE_ID, MESH_CORE, DAYS_POST_LABEL, SOIL_PME (phosphomonoesterase measurement), plus related identifiers.

- Quality control and limitations
  - Quality assurance included numeric range checks, formatting checks, and logical integrity checks.
  - Data are provided with no warranty of accuracy or fitness for a particular use; liability for use is disclaimed.

- Potential analyses and questions for researchers/analysts
  - How hyphal severance (rotation vs static cores) influences AM colonization metrics (total colonization, arbuscule/vesicle abundance) and shoot N/P status.
  - Relationships between AM colonization intensity and plant nutrient content (N, P, N:P ratio) across treatments.
  - Temporal dynamics of 33P uptake into shoots and its relation to core rotation, in-growth timing, and AM network connectivity.
  - Cross-dataset integration to quantify how AM network activity correlates with nutrient transfer from soil to plants under different treatments and over time.
  - Meta-analyses comparing the two plant species (Agrostis capillaris vs Trifolium repens) in AM colonization and nutrient uptake responses.