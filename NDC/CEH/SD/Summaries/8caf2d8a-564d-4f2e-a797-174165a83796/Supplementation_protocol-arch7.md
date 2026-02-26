# The seed set of supplemented and pollinator exposed flowers from Eschscholzia californica plants located within habitats comprising different floral cover.

## Overview
- Dataset on seed production from pollinator-exposed and supplemented Eschscholzia californica plants.
- Collected in June 2015 at Hillesden estate, Buckinghamshire, UK.
- Experimental design includes 16 arrays across four 100 ha replicate blocks, with arrays placed along transects at habitat boundaries.
- Aim: compare seed set between field-exposed (pollinator-visited) and supplemented (outcrossed pollen) flowers to assess pollen limitation across habitat contexts.
- Part of a broader experiment on how floral resources influence pollination services to isolated plants.
- Dataset is complete and prepared by Evans, T.M.

## Experimental design
- Plants grown from seed and arranged into arrays of three plants each, 1 m apart in a triangular formation.
- 16 arrays across four replicate 100 ha blocks (>500 m apart between blocks).
- At block centers, four arrays placed along a 150 m transect crossing the boundary between florally rich and florally poor habitats (two arrays per habitat type).

## Collection methods
- All open flowers removed before field placement.
- Field period: 16 days to ensure full anthesis and multiple pollination events.
- One flower per plant supplemented with outcrossed pollen by transferring four dehiscing anthers from a donor plant to the stigma.
- Fruits tagged; supplemented flowers protected with fine muslin to prevent windborne pollen transfer.
- Post-field, plants stored under controlled glasshouse conditions (20/15 C; 12:12 hr light:dark) until fruit maturation.
- Seed set quantified as the number of filled seeds per fruit; pollen limitation expressed as the ratio of mean seeds from field-exposed flowers to seeds from supplemented flowers.

## Data structure and units
- Data file: The_seed_set_of_supplemented_and_pollinator_exposed_E.californica_flowers.csv
- Key columns:
  - Block: replicate block identifier (4 blocks)
  - Experimental_array: array identifier within a block (4 arrays per block)
  - Plant_identification_number: plant ID prior to field transfer
  - Habitat: habitat type of the array location
  - Treatment: whether the array is field-exposed or supplemented
  - Mean_number_of_seeds_from_field_exposed_flowers: average seeds per field-exposed fruit
  - Number_of_fruits: number of fruits used to calculate the mean
  - Number_of_seeds_from_supplemented_flowers: seeds per supplemented flower
- NA entries indicate supplemented flowers did not survive.

## Spatial context and GIS relevance
- Spatial design features: four replicate blocks with transect-aligned arrays; habitat context includes florally rich vs florally poor areas.
- Attributes suitable for GIS: Block, Experimental_array, Habitat, Treatment, and seed-set metrics.
- Use cases: mapping pollen limitation trends across habitat contexts; integrating with habitat and floral-resource layers to analyze spatial patterns in pollination services.
- Limitations for GIS: no explicit geographic coordinates provided; analysis at block/array level rather than precise point locations without supplementary site geography data.

## Quality, provenance, and notes
- Dataset described as complete; collected and interpreted by Evans, T.M.
- NA values indicate compromised supplementation (flower did not survive).