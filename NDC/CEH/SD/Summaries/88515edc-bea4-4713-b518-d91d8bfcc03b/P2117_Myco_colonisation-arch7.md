# Measurements of nutrient cycling within grassland mycorrhizal mycelial networks [NERC Soil Biodiversity Programme]

- A data-backed study from the NERC Soil Biodiversity Thematic Programme examining nitrogen (N) and phosphorus (P) dynamics in arbuscular mycorrhizal (AM) networks within grassland.
- Includes two related experiments using in-growth cores and labeled phosphorus to assess AM hyphal connectivity, nutrient transfer, and plant uptake.
- Data are organized into three CSV datasets with metadata on sampling, treatments, and measurements of root colonisation, shoot nutrient contents, and 33P transfer.

## Overview of study aims and context

- Investigates functional roles of soil biota in carbon and nutrient cycling, focusing on AM mycelial networks within a diverse grassland community.
- Aims to understand how AM hyphae influence nutrient transfer between soil and plants and how hyphal severance affects colonisation and nutrient uptake.
- Data support analyses of mycorrhizal colonisation, shoot nitrogen and phosphorus concentrations, and phosphorus-33 uptake over time.

## Site and experimental design

- Location: Sourhope field site, Scotland (NGR: NT 854196; grid reference cited for site monitoring; Sourhope field data handbook referenced for detailed context).
- Grassland: Rich species assemblage with substantial AM associations; soils developed on locally derived drift with acidic brown earth characteristics (pH 4.5–5.0; organic C ~25%).
- Core design: ABS water pipe cores (18 mm ID, 22 mm OD; 150 mm length) with four windows (~50% surface area) and nylon mesh (35 μm) to allow AM hyphae, plus permeable base for drainage. A parallel set of cores without windows served as AM hyphae exclusion controls.
- Two experiments:
  - Experiment 1: Hyphal severance to study AM colonisation of bait plants (Trifolium repens) inside cores; includes rotated vs static cores to disrupt hyphal ingrowth; assessment of AM colonisation and nutrient status after ~10 weeks.
  - Experiment 2: Hyphal severance and transfer of 33P from plant-free, mesh-bound soil cores into surrounding grassland turfs; involves rotation schedules to modulate hyphal connections; multiple harvests over ~201 days.

## Experiments and measurements

- Experiment 1: AM colonisation effects
  - Bioassay setup with trap plants (Trifolium repens) in controlled field turves; 42 cores (mesh vs solid), 5 replicates survived.
  - Measurements: shoot N and P concentrations; total shoot N content and P content; root colonisation (% by McGonigle et al. 1990 scoring); root length via grid intercept method.
  - Hyphal severance assessment: rotating vs static cores; measurement of AM hyphal length in cores after ~11 weeks.
- Experiment 2: 33P transfer dynamics
  - Plant-free cores embedded in turf pots; 12 weeks in-growth to allow AM in-growth; half of cores rotated to break connections.
  - Labeling with 33P (approx. 682 mBq per core) and tracking under different rotational treatments.
  - Harvest schedule: plant shoots harvested at multiple time points (3, 16, 40, 73, 110, 158, 201 days after labeling); analysis included total shoot P, 33P activity in shoots, and soil extractable 33P.
  - Additional measurements: soil phosphomonoesterase (PME) activity as part of soil P cycling assessment.
- Analytical methods (summarised)
  - Nutrient analyses: total N and P in shoots; shoot N:P ratios.
  - AM colonisation: proportion of root length with arbuscules and vesicles.
  - 33P tracing: liquid scintillation counting after appropriate sample digestion; soil extractable 33P measured by water extraction and scintillation counting.
  - Root metrics: root colonisation percentage via established mycorrhiza staining methods; root length estimation.

## Data files and schema (Data Structure)

Three CSV datasets are provided:

- Dataset 1077: Mycorrhizal colonisation bioassay 1.0 Part1
  - Contents: Mycorrhizal colonisation of Agrostis capillaris bioassay plants; shoot N and P concentrations; root colonisation metrics.
  - Key fields:
    - SAMPLE_ID, SAMPLING_DATE, BLOCK, TREATMENT
    - TOTAL_ROOT_COL (AM colonisation %)
    - SHOOT_N_CONC, SHOOT_P_CONC, SHOOT_RATIO_N_P
    - SHOOT_N_CONTENT, SHOOT_P_CONTENT
    - ARBUSCULES, VESICLES
- Dataset 1078: Mycorrhizal colonisation bioassay 1.0 Part2
  - Contents: Mycorrhizal colonisation of Trifolium repens roots and shoot N and P concentrations in sand-filled mesh cores within turves.
  - Key fields:
    - SAMPLE_ID, SAMPLING_DATE, AREA
    - TOTAL_ROOT_COL, SHOOT_N_CONC, SHOOT_P_CONC, SHOOT_RATIO_N_P
    - SHOOT_N_CONTENT, SHOOT_P_CONTENT
    - ARBUSCULES, VESICLES
- Dataset  P2117_PLANT_UPTAKE_PHOS_33.csv
  - Contents: Measurement of plant uptake of phosphorus-33 from Sourhope turfs by AM mycelium using mesh cores with radioactive 33P; comparison of static vs rotated cores.
  - Key fields:
    - SAMPLE_ID, MESH_CORE, SAMPLING_DATE, DAYS_POST_LABEL
    - SOIL_PME (phosphomonoesterase measurement)
  - Note: Data are presented with -999 as missing value indicator.

- Quality and data integrity
  - Quality control steps include numeric range checks, formatting checks, and logical integrity checks.
  - The data have undergone QA procedures, but no warranty on accuracy or fitness for a particular use; no liability for usage or interpretation.

## How this GIS-specialist can use the data

- Spatial and temporal context
  - Georeferenced site context provided (Sourhope, NT grid reference) with block and area identifiers enabling spatial joins to habitat/plot layers.
  - Datasets offer sampling blocks and zones that can be mapped over time to visualize spatial patterns of AM colonisation and nutrient transfer.
- Attribute schema for mapping
  - AM colonisation metrics (TOTAL_ROOT_COL, ARBUSCULES, VESICLES) can be displayed as thematic layers across blocks/areas.
  - Nutrient concentrations (SHOOT_N_CONC, SHOOT_P_CONC, SHOOT_RATIO_N_P) and shoot content (SHOOT_N_CONTENT, SHOOT_P_CONTENT) enable choropleth or graduated symbol maps.
  - 33P uptake data (DAYS_POST_LABEL, MESH_CORE, and related 33P measurements) support time-series visualization of nutrient transfer dynamics.
- Data integration
  - Combine with soil, vegetation, or climate layers to examine drivers of AM-mediated nutrient cycling.
  - Align with the Sourhope Field Data Handbook and related publications for broader context and calibration of spatial units.
- Considerations and caveats
  - Data are specific to experimental cores and controlled rotations; caution with extrapolation to unmanaged field conditions.
  - Missing values and treatment identifiers should be handled according to dataset documentation (e.g., -999 indicators, nulls).

## References and metadata

- Core methodological references include standard methods for mycorrhizal assessment and nutrient analyses (McGonigle et al. 1990; Bremner & Mulvaney 1982; Tennant 1975; Brundrett et al. 1994).
- Related background materials and datasets referenced (SOURHOPE FIELD DATA HANDBOOK 2003; Usher et al. 2006) for broader program context.