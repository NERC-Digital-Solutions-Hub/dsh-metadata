# The_seed_set_of_supplemented_and_pollinator_exposed_E.californica_flowers.csv

- Purpose: Dataset documenting seed production for Eschscholzia californica under pollinator-exposed versus pollen-supplemented conditions across habitats with different floral cover to quantify pollen limitation.
- Location and timing: Hillesden estate, Buckinghamshire, UK; collected in June 2015.
- Context: Part of a broader study on how floral resources affect pollination services to isolated plants.

## Experimental design and habitat context

- Experimental arrays: 16 arrays across four replicate blocks (each >100 ha, separated by >500 m).
- Array composition: each array contains three E. californica plants spaced 1 m apart in a triangular formation.
- Block layout: center of each block contains four arrays arranged along a 150 m transect, spanning the boundary between a florally rich wildflower patch and florally poor habitats (bare/fallow ground or grazed grassland).
- Habitat treatment: within each block, two arrays in florally rich habitat and two in florally poor habitat.

## Data collection and treatments

- Field exposure: open flowers removed before placement; plants in the field for 16 days to allow full anthesis and multiple pollination events.
- Pollen treatment: after 16 days, one flower per plant across 48 plants was supplemented with outcrossed pollen by transferring four dehiscing anthers from a donor plant to the receptive stigma; supplemented flowers were protected with muslin nets.
- Post-harvest handling: fruits collected when matured; stored under controlled glasshouse conditions (day 20°C, night 15°C; 12:12 h light:dark) until seed analysis.
- Seed measurement: counted filled seeds per fruit; data used to derive mean seed set per field-exposed plant and compare to the supplemented (potential) seed set.

## Data structure and key variables

- File: The_seed_set_of_supplemented_and_pollinator_exposed_E.californica_flowers.csv
- Key columns:
  - Block: replicate block ID (1–4)
  - Experimental_array: array ID within a block (1–4)
  - Plant_identification_number: unique plant ID before field placement
  - Habitat: florally rich or florally poor
  - Treatment: pollinator-exposed or supplemented
  - Mean_number_of_seeds_from_field_exposed_flowers: average seeds per fruit for field-exposed flowers
  - Number_of_fruits: count of fruits used to compute the mean
  - Number_of_seeds_from_supplemented_flowers: seeds per fruit from supplemented flowers
- Missing data: NA indicates supplemented flowers did not survive

## Measurement and interpretation

- Pollen limitation metric: ratio of mean seeds from field-exposed flowers to seeds from supplemented flowers (per block/array/plant as applicable).
- Contextual insight: enables analysis of how floral resource context (habitat quality) influences pollination success and seed set in isolated plants.

## Supplemental and provenance information

- Supporting documentation: “The seed set of supplemented and pollinator exposed flowers from Eschscholzia californica plants located within habitats comprising different floral cover.”
- Data provenance: complete dataset, collected and interpreted by Evans, T.M.
- Relation to broader study: part of a larger experiment examining the effect of floral resources on pollination services.