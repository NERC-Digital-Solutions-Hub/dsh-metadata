# Long-term multisite Scots pine trial, Scotland: cone and seed phenotypes, 2024

## Overview
- Data from one site of a long-term multisite provenance-progeny trial in the Scottish Borders.
- Seeds collected in March 2007 from eight mother trees for each of 21 native Scots pine populations; populations cover the species range in Scotland with three populations per seed zone.
- Experimental design: complete randomised block with four blocks of eight rows; trees spaced 3 x 3 m with a guard row.
- Trial dataset: 672 trees from 168 families, with four replicates per family; trees from the same mother tree are considered half-siblings (family).

## Study design and sampling
- Sampling occurred in late February 2024 for cone abundance (count of visible cones on the southern-facing half of each tree).
- Five cones were sampled per tree from previous-year whorl branches; if fewer than five cones were available, cones were sampled from anywhere on the tree.
- Cones sampled from different branches at varying heights up to 3 m.
- Storage: cones stored at 4°C in a cool room at the UK Centre for Ecology & Hydrology, Penicuik.
- Cone and seed phenotyping conducted between May and July 2024.

## Measurements and data collected
- Cone traits measured on all cones:
  - Cone_length, Cone_width, Stalk_length, Scale_length, Scale_width, Scale_number, Cone_ratio, Cone_Angle
  - Hue, Value, Chroma (colour scored using Munsell charts; units NA)
  - Profile (scale flatness; 1–4)
  - Openness (cone openness after drying; 1–4; 1 = closed, 4 = very open)
- Seeds measured for seven populations (subset due to time constraints):
  - Seed_number, Filled_seed_number, Seed_viability (ratio of filled seeds to total seeds)
- Measurement methods:
  - Length/width with digital calipers; colour with Munsell charts; cone drying at 35°C prior to seed extraction.
- Date of data collection: 2024; data collection window May–July 2024 for cone/seed traits.

## Data file structure and contents
- Data file: Scots_pine_cone_data.csv (single file comprising the dataset).
- Key columns include:
  - Order (tree order in the trial)
  - Block (randomised block code)
  - Id (tree identification code)
  - Fam (family code; two-letter population code plus mother tree number)
  - Cone_number (number of cones on the southern side)
  - Cone_id (cone identification code)
  - Cone_length, Cone_width, Stalk_length, Scale_length, Scale_width, Scale_number
  - Cone_ratio, Cone_Angle
  - Hue, Value, Chroma (colour scores; NA units)
  - Profile (1–4)
  - Openness (1–4)
  - Seed_number, Filled_seed_number, Seed_viability (for seven populations)
- Units provided for numeric traits (e.g., mm for lengths; ratio for Cone_ratio; NA for colour fields).
- Data dictionary and field descriptions accompany the file, clarifying each column and its measurement context.

## Provenance, handling, and storage
- Field sampling location: Scottish Borders (coordinates provided for the site).
- Trial site coordinates and broader trial context linked to Beaton et al. 2022.
- Specimens and data managed at the James Hutton Institute ( Aberdeen) for initial growth and at UK Centre for Ecology & Hydrology, Penicuik for storage.
- Data collected with standardized measurement approaches (calipers, Munsell colour charts) and recorded with explicit field descriptors.

## Data governance, quality, and limitations
- Metadata richness: detailed column descriptions, units, and measurement methods embedded in the dataset.
- Reproducibility: clear documentation of sampling strategy, replication structure, and family-level coding (Fam).
- Limitations to note for stewardship:
  - Seed measurements limited to seven populations due to time constraints.
  - Cone measurements limited to cones on the southern-facing half; sampling from other parts of the tree if fewer than five cones were available.
  - Some fields use NA for non-applicable measurements (e.g., Hue/Value/Chroma).
- References for broader context and dataset provenance:
  - Beaton, J., Perry, A., Cottrell, J., Iason, G., Stockan, J., Cavers, S. 2022. Phenotypic trait variation in a long-term multisite common garden experiment of Scots pine in Scotland. Sci Data. 9, 671.

## Availability and citation
- Dataset comprises a single CSV file (Scots_pine_cone_data.csv) linked to a broader long-term multi-site experiment.
- Primary reference for context and provenance: Beaton et al. 2022 (Sci Data).