# The seed set of Eschscholzia californica plants introduced into habitats comprising different floral cover

## Overview
- Dataset of seed counts (seed set) for Eschscholzia californica plants introduced to experimental arrays across habitats with varying floral cover.
- Collected in June 2015 at the Hillesden estate, Buckinghamshire, UK.
- Experimental design: 16 arrays across four 100-hectare replicate blocks; each block contains four arrays (three plants per array, arranged in a triangle, 1 m apart).
- Arrays positioned along a 150 m transect centered on the boundary between florally rich patches and florally poor habitats (bare/fallow or grazed grassland), with two arrays in each habitat type per block.
- Purpose: assess effects of habitat context and pollinator access on plant reproduction as part of a larger study on floral resources and pollination services to isolated plants.
- Dataset is complete and was collected and interpreted by Evans, T.M.

## Experimental design
- In each of four replicate blocks, four experimental arrays were established (total of 16 arrays).
- Each array comprised three Eschscholzia californica plants, separated by 1 m in a triangular formation.
- Center of each block includes arrays at 50 m intervals along a 150 m transect crossing habitat boundaries.
- Habitat context: two arrays per block in florally rich habitat and two in florally poor habitat.

## Collection methods
- All open flowers removed from 48 plants prior to field placement; one bud on each plant covered with muslin to create a pollinator-excluded flower.
- Field exposure lasted 16 days to allow full anthesis and multiple pollination events.
- After 16 days, fruits were tagged to attribute development to the field period.
- Plants were collected and stored under controlled glasshouse conditions (day:night 20°C:15°C; photoperiod 12:12 h) until fruit maturation.
- At maturation, the number of filled seeds per fruit was counted to quantify seed set.

## Data structure and content
- File: Eschscholia_californica_seed_set.csv (CSV format).
- Key columns:
  - Block: replicate block identifier.
  - Experimental array: identifier for each array within a block (three plants per array).
  - Plant identification number: pre-field plant ID used in the broader project.
  - Sample type: whether the flower was exposed to pollinators or excluded (muslin-covered).
  - Fruit number: identifier for each fruit analyzed per plant.
  - Habitat: location context of the array (habitat type).
  - Treatment: experimental condition related to exposure (pollinator access).

- Data captured: seed set per fruit (number of filled seeds), enabling analyses of how habitat context and pollinator exposure influence reproductive success.

## Provenance, completeness, and documentation
- The dataset is complete and bound to a single dataset focused on seed set measurements.
- Collected and interpreted by Evans, T.M.
- Supporting documentation explicitly notes the dataset title: The seed set of Eschscholzia californica plants introduced into habitats comprising different floral cover.
- Part of a larger experiment examining the effect of floral resources on pollination services to isolated plants.

## Data quality and governance considerations for Data Stewards
- Clear experimental protocol with replicates, defined habitats, and controlled collection conditions support reproducibility.
- Metadata within the file structure (Block, Experimental array, Plant ID, Sample type, Habitat, Treatment) facilitates data discovery and reuse, including filtering by habitat type or pollination exposure.
- Ensure data versioning and provenance: link CSV to related documentation and broader project dataset(s) for complete context.
- Standardize unit interpretation: seed set is given as the number of filled seeds per fruit; confirm units and calculations when integrating with other datasets.

## Usage and potential considerations for reuse
- Suitable for analyses of how habitat context and pollinator access affect seed production in an isolated plant system.
- Useful for meta-analyses on pollination services and habitat fragmentation effects when combined with other datasets.
- Users should reference the collection date (June 2015) and location (Hillesden estate, Buckinghamshire) and acknowledge Evans, T.M. as the interpreter of the data.