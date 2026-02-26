# Measurements of nutrient cycling within grassland mycorrhizal mycelial networks [NERC Soil Biodiversity Programme]

- Aims and context
  - Part of the NERC Soil Biodiversity Thematic Programme (1999–200?); focused on understanding biological diversity of soil biota and functional roles in carbon and nutrient cycles.
  - Field site: Sourhope, Scotland; large grassland with significant arbuscular mycorrhizal (AM) associations.
  - Objectives: assess nutrient cycling (nitrogen and phosphorus) mediated by AM mycelia and their influence on soil microbial communities and ecosystem functioning.

- Experimental design and site description
  - Core-based setup: large intact grassland turves converted into free-draining plastic boxes; four windowed cores to enable hyphal ingrowth and AM activity, plus identical cores without windows to exclude AM ingress.
  - Two main experiments:
    - Experiment 1: effects of hyphal severance on AM colonization of bait plants and on AM hyphal length.
      - Bioassay plants (Trifolium repens) and Agrostis capillaris trials embedded in cores; rotation of some cores to sever hyphae.
      - Measurements: AM colonization of roots, root and shoot N and P, root length, and hyphal length.
    - Experiment 2: effects of hyphal severance on transfer of 33P from plant-free cores into surrounding grassland turfs.
      - Plant-free cores allowed AM in-growth; isotope labeling with 33P injected into cores; rotation protocols to modulate mycelial connectivity.
      - Measurements: 33P uptake in plant shoots over multiple timepoints and soil-extractable 33P; P transfer dynamics under different hyphal connectivity regimes.
  - Experimental conditions: controlled environment phases for growth and labeling; timescales ranging from weeks to months for sampling.

- Data outputs and structure
  - Dataset 1 (P2117_MYCORRHIZAL_COL_BIO_1.csv): Mycorrhizal colonisation bioassay for Agrostis capillaris.
    - Key fields: SAMPLE_ID, BLOCK, TREATMENT (Control, Lime, Nitrogen, Nitrogen+Lime), TOTAL_ROOT_COL (root AM colonisation), SHOOT_N_CONC, SHOOT_P_CONC, SHOOT_RATIO_N_P, SHOOT_N_CONTENT, SHOOT_P_CONTENT, ARBUSCULES, VESICLES.
  - Dataset 2 (P2117_MYCORRHIZAL_COL_BIO_2.csv): Mycorrhizal colonisation bioassay for Trifolium repens (play area).
    - Key fields: AREA, TOTAL_ROOT_COL, SHOOT_N_CONC, SHOOT_P_CONC, SHOOT_RATIO_N_P, SHOOT_N_CONTENT, SHOOT_P_CONTENT, ARBUSCULES, VESICLES.
  - Dataset 3 (P2117_PLANT_UPTAKE_PHOS_33.csv): Plant uptake of phosphorus-33 (33P) via AM mycelium, with static vs rotated cores.
    - Key fields: SAMPLE_ID, MESH_CORE (static/rotated), DAYS_POST_LABEL, SOIL_PME (PME measurement), and related sampling metadata.
  - Data relationships: three CSV files collectively cover AM colonisation metrics, shoot nutrient content, and 33P uptake, enabling connections between AM morphology, plant nutrient status, and direct isotope tracing.

- Metadata, quality control, and data governance
  - Data provenance and references: multiple methodological references (e.g., McGonigle et al. 1990 for colonisation scoring; Brundrett et al. 1994; Bremner & Mulvaney methods; Scott et al. 2003 Sourhope Field Data Handbook).
  - Quality control: numeric range checks, formatting checks, and logical integrity checks applied; dataset providers disclaim no warranty on accuracy or fitness for a given use.
  - Usage constraints: data are supplied with no liability for accuracy or reliability; users must assess suitability for their purposes.
  - Data structure notes: explicit variable definitions and units included in dataset descriptions; sample identifiers and treatment labels link to the original field design and sampling timeline.
  - Accessibility: datasets organized as CSV files with clear field descriptions to facilitate reuse and integration into analysis workflows.

- Relevance for monitoring frameworks
  - Demonstrates a comprehensive workflow for environmental health monitoring: from field-based experimental design to multi-faceted biological and chemical measurements.
  - Illustrates handling of complex data types (biological colonisation metrics, nutrient concentrations, and radiolabeled tracer data) and linking metadata to analysis-ready outputs.
  - Highlights governance considerations relevant to monitoring work: metadata completeness, data quality assurance, standardization of variables (e.g., AM colonisation metrics, N/P content, and isotope data), and clear disclaimers regarding data accuracy.
  - Provides a model for documenting data structure and sampling design to support transparency, reproducibility, and evidence-based decision-making in policy and programme evaluation.

- References and further reading
  - Key methodological and background sources listed, including methodological handbooks and related NERC publications, for context on AM research, root colonisation scoring, and isotope tracing techniques.