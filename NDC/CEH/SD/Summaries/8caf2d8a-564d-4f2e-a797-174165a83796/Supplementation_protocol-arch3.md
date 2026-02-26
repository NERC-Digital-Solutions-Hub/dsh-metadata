# The_seed_set_of_supplemented_and_pollinator_exposed_E.californica_flowers.csv

## Overview
- Details the number of seeds produced by pollinator-exposed versus supplemented (outcrossed pollen) Eschscholzia californica flowers located in habitats with different floral cover.
- Collected in June 2015 at the Hillesden estate, Buckinghamshire, UK.
- Experimental arrays comprised of three plants each, arranged in triangles; 16 arrays across four 100 ha replicate blocks.
- Within each block, four arrays were placed along a 150 m transect crossing the boundary between florally rich and florally poor habitats (two per habitat type).
- Seed set from field-exposed flowers is compared to seed set from supplemented flowers to quantify pollen limitation in relation to habitat context.
- Part of a larger experiment on how floral resources influence pollination services to isolated plants; dataset complete and interpreted by Evans, T.M.

## Experimental design
- In June 2015, Eschscholzia californica plants (grown from seed) formed experimental arrays: three plants per array, 1 m apart, arranged triangularly.
- Sixteen arrays created across four 100 ha replicate blocks, each >500 m apart.
- At the center of each block, four arrays positioned at 50 m intervals along a 150 m transect running across the boundary between an established wildflower patch and bare fallow or grazed grassland (two arrays in florally rich habitat, two in florally poor habitat).

## Collection and treatment methods
- All open flowers removed from 48 plants before placement in the field.
- Field exposure lasted 16 days to ensure full anthesis and multiple pollination events.
- From each of the 48 plants, one flower was supplemented with outcrossed pollen (via transfer of dehiscing anthers from a donor plant onto the receptive stigma).
- Supplied flowers were protected with fine muslin to prevent windborne transfer from the glasshouse air-conditioning system.
- Plants were collected and stored under controlled glasshouse conditions (day 20°C, night 15°C; 12:12 light:dark).
- Upon fruit maturation, the number of filled seeds per fruit was counted.
- Pollen limitation was expressed as the ratio of mean seed set from field-exposed flowers to the seed set from supplemented flowers.

## Data structure and units
- All data are stored in one CSV file: The_seed_set_of_supplemented_and_pollinator_exposed_E.californica_flowers.csv.
- Key columns:
  - Block: replicate block identifier (4 blocks).
  - Experimental_array: array identifier within a block (4 arrays per block; total of 16).
  - Plant_identification_number: plant ID assigned before field transfer.
  - Habitat: florally rich vs florally poor habitat context.
  - Treatment: field-exposed vs supplemented with outcrossed pollen.
  - Mean_number_of_seeds_from_field_exposed_flowers: average seeds per fruit for field-exposed flowers.
  - Number_of_fruits: number of fruits from which seed counts were averaged.
  - Number_of_seeds_from_supplemented_flowers: seeds per fruit for supplemented flowers.
- Note: 'NA' indicates supplemented flowers that did not survive.

## Study context and provenance
- The dataset is part of a broader investigation into how floral resources affect pollination services to isolated plants.
- Data collection and interpretation were conducted by Evans, T.M.

## Uses for monitoring and policy
- Provides a quantified measure of pollen limitation across habitat contexts, informing habitat restoration and floral resource management policies.
- Enables comparison of pollination success in florally rich versus poor environments, supporting decisions on plantings, habitat mosaics, and pollinator support strategies.
- The explicit treatment structure and replicates support monitoring of changes over time or under different management scenarios.

## Data quality, metadata, and governance considerations
- Comprehensive metadata is included in the dataset description (experimental design, collection methods, and variable definitions).
- Shortcomings to anticipate in monitoring contexts:
  - Potential data gaps if supplemented flowers fail to survive (NA values present).
  - The need for ongoing quality assurance (QA) to ensure consistent pollen transfer and accurate seed counts.
  - Data sharing and openness requirements may impose barriers if raw data or full metadata are not publicly accessible; this dataset demonstrates explicit sharing of underlying data and processing details.
- For monitoring frameworks: emphasize clear documentation of metadata, data provenance, data cleaning steps, and governance around data storage and updates to maintain data usefulness over time.