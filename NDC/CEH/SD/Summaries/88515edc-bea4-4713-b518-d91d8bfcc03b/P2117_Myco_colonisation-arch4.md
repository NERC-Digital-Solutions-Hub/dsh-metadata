# Measurements of nutrient cycling within grassland mycorrhizal mycelial networks

## Overview and purpose
- Part of the NERC Soil Biodiversity Thematic Programme (1999–present) focusing on understanding soil biota diversity and functional roles in key ecological processes.
- Data describe measurements of nitrogen (N) and phosphorus (P) in roots and shoots to study arbuscular mycorrhizal (AM) mycelia function within grassland ecosystems.
- Two related experiments within the Sourhope field site aimed at linking AM networks to nutrient cycling and carbon cycling in soil microbial communities.
- Site and design: large intact monoliths of a diverse, AM-associated grassland were moved to controlled conditions at the University of Sheffield for functional studies.

## Context and site description
- Field site: Sourhope, Scotland; 24 higher-plant species (21 AM-forming), British Vegetation Classification U4d sub-community.
- Soils: acid brown earths (pH 4.5–5.0) with ~25% organic carbon, derived from local drift.
- Experimental setup: monolith cores (45 x 35 x 30 cm) installed in plastic boxes with a permeable base for drainage; four windows per core allowed AM hyphae in-growth except in exclusion cores.

## Experimental design and methods
- Core design and treatments:
  - Cores with mesh barriers to allow AM hyphae; some cores without windows to exclude AM hyphae.
  - Bait plants (Trifolium repens) introduced into half of the mesh cores.
  - Rotation of some mesh cores (~45° weekly) to disrupt hyphal connections; other cores remained static.
- Experiment 1: AM colonization of bait plants
  - Autoclaved sand substrate in cores; 42 cores (28 mesh, 14 solid) arranged in turf blocks.
  - Growth period: 11 weeks outdoors with supplementary watering; bioassay plants harvested after 10 weeks for analysis.
  - Measurements: AM colonization (root lengths, arbuscules/vesicles), root and shoot N and P concentrations, shoot/N and shoot P content.
- Experiment 2: transfer of 33P from soil cores to surrounding grasses
  - Plant-free soil cores established in pots, then allowed to in-grow AM networks for 12 weeks.
  - Radioactive 33P label injected into cores, with half the cores rotated to modulate hyphal transfer; the rest remained undisturbed.
  - Harvest schedule spanning 201 days post-labeling; measurements of 33P uptake in plant shoots and 33P in soils, plus plant P content.
- Analytical methods
  - Nutrient analyses (N and P) on shoots and roots.
  - Mycorrhizal assessment on roots (colonization percentage, arbuscules, vesicles).
  - 33P radioactivity measurements in shoots and soil extracts.
  - Hyphal length assessment and other AM metrics as per referenced methodologies.

## Data files and structure
Three CSV data files (Dataset references 1077–1078) accompany the study, with additional plant uptake data:
- P2117_MYCORRHIZAL_COL_BIO_1.csv
  - Mycorrhizal colonisation data for Agrostis capillaris bioassay plants in turves.
  - Key fields: SAMPLE_ID, BLOCK, TREATMENT, TOTAL_ROOT_COL, SHOOT_N_CONC, SHOOT_P_CONC, SHOOT_RATIO_N_P, SHOOT_N_CONTENT, SHOOT_P_CONTENT, ARBUSCULES, VESICLES, sampling date, etc.
- P2117_MYCORRHIZAL_COL_BIO_2.csv
  - Mycorrhizal colonisation data for Trifolium repens roots grown in sand-filled mesh cores.
  - Key fields: SAMPLE_ID, AREA, TOTAL_ROOT_COL, SHOOT_N_CONC, SHOOT_P_CONC, SHOOT_RATIO_N_P, SHOOT_N_CONTENT, SHOOT_P_CONTENT, ARBUSCULES, VESICLES, sampling date, etc.
- P2117_PLANT_UPTAKE_PHOS_33.csv
  - Measurement of phosphorus-33 uptake from turfs via AM networks.
  - Key fields: SAMPLE_ID, MESH_CORE (static or rotated), DAYS_POST_LABEL, SOIL_PME (phosphomonoesterase), etc.
- Data quality and metadata
  - Missing values and placeholder conventions noted (e.g., nulls, -999 in Part 2 dataset).
  - Data dictionaries outline variable definitions, units, and data types for each file.
  - Documentation references include Scott et al. (2003) Sourhope Field Data Handbook and related methodological sources.

## Provenance, quality control, and limitations
- Quality control steps performed: numeric range checks, formatting checks, and logical integrity checks.
- Data providers (NERC) do not warrant accuracy or fitness for a particular use; liability for data use is disclaimed.
- Metadata and provenance links available to support data discovery and integration, with cross-references to related literature and methodological standards.

## Relevance for data leadership and data strategy
- Demonstrates end-to-end data lifecycle: site description, experimental design, data collection, laboratory analysis, and structured data outputs.
- Highlights the importance of rich metadata, dataset references, and data dictionaries for discoverability and reusability.
- Illustrates challenges and practices relevant to data stewardship: handling specialized experimental data, rotational vs static treatments, and multi-omics-like measurements (root colonization, nutrient content, and isotope tracing).
- Provides a model for integrating niche ecological measurements into a broader data system with clear data assets, access points, and quality disclosures.