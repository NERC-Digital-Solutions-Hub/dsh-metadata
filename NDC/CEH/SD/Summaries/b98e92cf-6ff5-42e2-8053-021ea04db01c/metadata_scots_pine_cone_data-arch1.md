# Long-term multisite Scots pine trial, Scotland: cone and seed phenotypes, 2024

## Overview
- A single-site measurement within a long-term multisite provenance-progeny trial of Pinus sylvestris in the Scottish Borders.
- Seeds from 8 mother trees across 21 native populations, spanning all species range in Scotland with three populations from each of seven seed zones.
- Field establishment: seeds germinated in 2007, saplings planted in 2012; 672 trees from 168 families (4 replicates per family) in a complete randomized block design (4 blocks; 8 rows per block).
- Trees spaced 3x3 m; guard row around the site to limit edge effects.
- Aims to capture cone and seed phenotypes for genetic and provenance-based analyses.

## Experimental design and sampling
- Cone abundance recorded in February 2024 as counts of visible cones on the southern-facing half of each tree.
- Cone sampling: five cones per tree from previous-year whorl branches; prioritized southern-facing cones but sampled from anywhere if fewer than five available; sampled from varying heights up to 3 m.
- Cones stored at 4°C at the UK Centre for Ecology & Hydrology (Penicuik) before analysis (May–July 2024).

## Traits measured
- Cone morphology on all sampled cones: 
  - Cone_length, Cone_width, Stalk_length, Scale_length, Scale_width, Scale_number, Cone_ratio, Cone_Angle.
  - Colour metrics: Hue (Munsell basis), Value, Chroma (scored; Hue/Value/Chroma provided but may be NA for some entries).
  - Profile: scale flatness scored as 1 (flat) to 4 (very raised).
  - Openness: cone openness after drying, scored 1 (closed) to 4 (very open).
- Seed traits (measured May–July 2024) limited to seven populations (one from each seed zone):
  - Seed_number, Filled_seed_number, Seed_viability (calculated as Filled_seed_number / Seed_number).
- Data collection focuses on phenotypic variation in cone structure, colour, and openness, with seed traits providing reproductive output measures.

## Dataset structure
- Single data file: Scots_pine_cone_data.csv.
- Key fields include:
  - Experimental identifiers: Order (tree order in trial), Block (randomized block code), Id (tree ID), Fam (family code; two-letter population code + mother tree number).
  - Cone-level descriptors: Cone_number, Cone_id, Cone_length, Cone_width, Stalk_length, Scale_length, Scale_width, Scale_number, Cone_ratio, Cone_Angle, Profile, Openness.
  - Colour metrics: Hue, Value, Chroma.
  - Seed-level descriptors (where measured): Seed_number, Filled_seed_number, Seed_viability.
  - Date fields: Date of data collection.
- Notes: Hue/Value/Chroma may be NA for some entries; seed trait measurements exist only for seven populations.

## Data collection and quality considerations
- Field sampling constraints led to sampling from the southern-facing half where possible; deviations occur if cone counts were insufficient.
- Seed traits limited to a subset of populations due to time constraints.
- Data are organized to support cross-population, cross-family, and site-wide comparisons with replicates, enabling mixed-model analyses of genetic vs environmental effects.

## Source and reference
- Beaton, J., Perry, A., Cottrell, J., Iason, G., Stockan, J., Cavers, S. 2022. Phenotypic trait variation in a long-term multisite common garden experiment of Scots pine in Scotland. Sci Data. 9, 671. https://doi.org/10.1038/s41597-022-01791-8

## Potential analytical applications
- Assess correlations among cone traits (length, width, scale metrics, colour, profile) and seed metrics (seed_number, filled_seed_number, viability).
- Partition phenotypic variation by population, family, and environmental (site/block) factors using hierarchical models.
- Explore heritability and genetic correlations of cone morphology traits across seed zones.
- Inform breeding, provenance selection, and conservation strategies by identifying trait patterns linked to reproductive success and cone openness.