# Measurements of nutrient cycling within grassland mycorrhizal mycelial networks [NERC Soil Biodiversity Programme]

- Aim
  - Document measurements of nitrogen (N) and phosphorus (P) cycling within arbuscular mycorrhizal (AM) mycelial networks in grassland.
  - Part of the NERC Soil Biodiversity Thematic Programme (1999) focused on linking soil biodiversity with key ecological processes such as carbon and nutrient cycling.
  - Data produced to enable standardized assessment of environmental health and functional roles of soil biota, with potential for integration with other monitoring data.

- Context and site
  - Field site: Sourhope, Scotland (NGR NT 854196) within the NERC Soil Biodiversity Thematic Programme.
  - Grassland community: 24 higher-plant species; 21 typically form AM associations; soil developed on local drift from andesitic lavas; acid brown earths (pH 4.5–5.0) with ~25% organic carbon.
  - Experimental setup used large intact grassland monoliths installed in free-draining plastic boxes for controlled assessment.

- Core design and experimental setup
  - Cores constructed from ABS plastic (18 mm ID, 22 mm OD, 150 mm length) with four windows (~50% of below-ground surface area) covered by nylon mesh (35 μm) to permit AM hyphae while controlling in-growth.
  - Some cores included identical tubing without windows to exclude AM hyphae (control for hyphal in-growth).
  - Provision of a permeable base enabled free drainage of soil water.
  - Cores placed in turf plots; rotation of certain cores used to break hyphal connections and test connectivity effects.

- Experiments
  - Experiment 1: Effects of hyphal severance on AM colonization and nutrient transfer
    - Bioassay plants: Trifolium repens L. in bait-core setups; 42 cores (28 mesh-enabled, 14 solid) arranged in turfs.
    - Treatments: some cores rotated weekly to disrupt hyphae; some bait plants excluded from cores; plant growth period ~10 weeks.
    - Measurements: AM colonization of bioassay plant roots; shoot and root N and P content; root length via grid intercept; hyphal length in cores.
  - Experiment 2: Effects of hyphal severance on transfer of 33P from soil to surrounding turf
    - Setup: turf blocks placed in pots with mesh-bound cores inserted; cores allowed 12 weeks for AM in-growth before labeling.
    - Labeling: 33P orthophosphoric acid (~682 mBq per core) injected into cores; cores rotated intermittently to disrupt connections in half of the pots.
    - Harvests: multiple time points up to ~201 days post-label; comparison between rotated and static cores.
    - Measurements: 33P content in shoots and soils; total shoot P; phosphorus uptake dynamics; PMEs (phosphomonoesterase) in soil.

- Measurements and analyses collected
  - Plant and root metrics
    - AM colonization of roots (arbuscules and vesicles) using established scoring (McGonigle et al., 1990) and root length measurements.
    - Shoot and root nitrogen (N) and phosphorus (P) concentrations; N:P ratios; total N and P contents in shoots.
  - Hyphal and network metrics
    - AM hyphal lengths within cores (rotated vs static) to assess connectivity.
  - Isotopic tracing
    - 33P uptake measured in plant shoots at set intervals; soil 33P extracted at final harvest to determine distribution.
  - Soil and enzyme metrics
    - Soil phosphomonoesterase (PME) activity measured as a proxy for phosphorus mineralization dynamics.

- Data products and structure
  - Dataset 1077: Mycorrhizal colonisation bioassay 1.0 Part 1
    - Contents: Mycorrhizal colonisation of Agrostis capillaris bioassay plants; shoot N and P concentrations; root colonisation metrics; ARBUSCULES and VESICLES; N and P contents; treatment and sampling metadata.
    - Key fields include SAMPLE_ID, SAMPLING_DATE, BLOCK, TREATMENT, TOTAL_ROOT_COL, SHOOT_N_CONC, SHOOT_P_CONC, SHOOT_RATIO_N_P, SHOOT_N_CONTENT, SHOOT_P_CONTENT, ARBUSCULES, VESICLES, etc.
  - Dataset 1078: Mycorrhizal colonisation bioassay 1.0 Part 2
    - Contents: Mycorrhizal colonisation in Trifolium repens roots; shoot N and P concentrations; root colonisation metrics; AREA, MESH_CORE, DAYS_POST_LABEL, and related variables for static vs rotated cores.
    - Key fields similar to Part 1, plus mesh/core status and sampling area details.
  - Dataset 1079: PLANT_UPTAKE_PHOS_33.csv
    - Contents: 33P content in plant shoots and soils; tracked via days post label; MESH_CORE status (static/rotated); PME measurements in soil.
    - Key fields include SAMPLE_ID, MESH_CORE, DAYS_POST_LABEL, and PME as well as 33P-related measurements.

- Quality control and limitations
  - Quality assurance included numeric range checks, formatting conformity, and logical integrity checks.
  - Despite QA, data accuracy for all end-use applications cannot be guaranteed; no liability accepted by NERC for data fitness or use outcomes.
  - Data users should consider the experimental design limitations (e.g., core-based mesocosm setup) when integrating with broader monitoring datasets.

- Relevance for environmental monitoring and data stewardship
  - Provides standardized, well-documented measurements of nutrient cycling and AM network function in a grassland system.
  - Datasets are prepared for integration with broader environmental monitoring data to assess ecosystem health, nutrient dynamics, and microbial-plant interactions over time.
  - Emphasizes data provenance, metadata completeness, and availability of underlying data for reuse, aligning with monitoring goals to increase data value and accessibility.