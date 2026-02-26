# The seed set of Eschscholzia californica plants introduced into habitats comprising different floral cover

- This dataset records seed counts (seed set) for Eschscholzia californica plants introduced into habitats with varying floral cover to assess how floral resources influence pollination.
- It is part of a larger experiment examining the effect of floral resources on pollination services to isolated plants, with data collected and interpreted by Evans, T.M.
- Supporting documentation is available as "The seed set of Eschscholzia californica plants introduced into habitats comprising different floral cover."

## Aim
- Quantify seed set per fruit for E. californica under two conditions (flowers exposed to pollinators vs pollinator-excluded) across habitats with different floral cover.
- Contex: determine how habitat floral resources affect pollination services to isolated plants.

## Experimental design
- June 2015, plants grown from seed and arranged into experimental arrays across Hillesden estate, Buckinghamshire, UK.
- Each array: three E. californica plants, 1 m apart, arranged in a triangular formation.
- 16 arrays across four replicate blocks (each 100 ha), blocks separated by >500 m.
- At block centers, four arrays placed along a 150 m transect across the boundary between an established wildflower patch and bare, fallow ground or grazed grassland.
  - Within each block: two arrays in florally rich habitat and two in florally poor habitat.

## Collection methods
- All open flowers removed from the 48 plants before field placement.
- One bud per plant covered with muslin to create a pollinator-excluded flower.
- Field exposure lasted 16 days to ensure full anthesis and multiple pollination events.
- Fruits were tagged to ensure only those from the experimental period were analyzed.
- Plants were then collected and grown in controlled glasshouse conditions (day:night 20°C:15°C; 12:12 h light:dark) until fruit maturation.
- At maturation, the number of filled seeds per fruit was counted to quantify seed set.

## Data structure
- File: Eschscholzia_californica_seed_set.csv
- Key columns:
  - Block: replicate block ID (one of four blocks)
  - Experimental array: array ID within each block (four arrays per block)
  - Plant identification number: ID assigned to each plant prior to field transfer
  - Sample type: whether the flower was exposed to pollinators or excluded
  - Fruit number: identification number for each analyzed fruit per plant
  - Habitat: location type of the array ( florally rich vs florally poor)
  - Treatment: contextual designation related to the array’s placement
- Overall design: 16 arrays × 3 plants per array = 48 plants; data capture per fruit

## Dataset context and notes
- The dataset is complete and intended for analysis of how floral resources in habitat contexts influence pollination outcomes.
- Collected and interpreted by Evans, T.M.
- The dataset supports analyses that relate habitat floral cover and pollinator access to seed production in isolated plants.

## Potential analyses and data considerations for analysts
- Compare seed set between pollinator-exposed and pollinator-excluded treatments to isolate pollination effects.
- Compare across habitats (florally rich vs florally poor) to assess the influence of surrounding floral resources on pollination success.
- Analytical approaches: hierarchical models with Block as a random effect; fixed effects for Habitat and Treatment; response variables could be per-fruit seed counts or proportion of filled seeds per fruit.
- Data considerations: small-scale, controlled experimental design with multiple blocks; ensure proper handling of categorical (Habitat, Treatment) and count data (Fruit number, Seeds per fruit).
- Data provenance and reproducibility: clearly track data sources, experimental IDs, and metadata to enable discoverability and reuse.