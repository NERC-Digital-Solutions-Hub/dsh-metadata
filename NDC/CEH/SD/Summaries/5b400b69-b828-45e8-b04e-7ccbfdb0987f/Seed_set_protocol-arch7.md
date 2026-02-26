# The seed set of Eschscholzia californica plants introduced into habitats comprising different floral cover

## Overview
- Dataset of seed counts for Eschscholzia californica plants introduced into habitats with varying floral cover.
- Collected in June 2015 at Hillesden estate, Buckinghamshire, UK.
- Experimental arrays: three plants per array, 1 m apart, arranged in a triangular formation.
- 16 arrays across four 100 ha replicate blocks, each >500 m apart.
- Arrays positioned along a 150 m transect crossing the boundary between a wildflower patch and bare/fallow grassland, with two arrays in florally rich habitat and two in florally poor habitat.
- Each plant experienced both pollinator-exposed and pollinator-excluded (muslin-covered bud) conditions to assess habitat effects on reproduction.

## Experimental design and spatial arrangement
- Four replicate blocks (each ~100 ha).
- Within each block: four experimental arrays (3 plants each) arranged along a 150 m transect at 50 m intervals.
- Arrays span across habitat types: florally rich vs florally poor.
- Spatial setup supports exploration of habitat context on plant reproduction and pollination services.

## Data collection methods
- Before placement, all open flowers removed from the 48 plants; one bud per plant covered to create a pollinator-excluded condition.
- Field period: 16 days to achieve full anthesis and multiple pollination events.
- After 16 days, fruits were tagged to ensure only fruit from the field period were analyzed.
- Fruits collected and stored under controlled glasshouse conditions until maturation.
- Upon maturation, the number of filled seeds per fruit was counted to quantify seed set.

## Data structure and fields
- Data stored in a single CSV file: Eschscholzia_californica_seed_set.csv.
- Key columns:
  - Block: replicate block identification.
  - Experimental array: array identification within each block (3 plants per array).
  - Plant identification number: unique ID for each plant prior to field transfer.
  - Sample type: whether the flower was exposed to pollinators or excluded.
  - Fruit number: identifier for each analyzed fruit per plant.
  - Habitat: location category of the array (habitat type).
  - Treatment: contextual treatment related to pollinator exposure.

## Location and temporal coverage
- Location: Hillesden estate, Buckinghamshire, UK.
- Timeframe: June 2015.
- Layout: four 100 ha replicate blocks; 16 arrays in total; four arrays per block (two in florally rich habitat, two in florally poor habitat).

## GIS relevance and use
- Spatially explicit layout information (blocks, arrays, transect positions, habitat context) supports map-based visualization of experimental design.
- Data can be mapped by block, array, habitat type, and pollination treatment to analyze spatial patterns in seed set.
- Distances and spatial relationships (50 m array spacing, 150 m transect, habitat boundaries) facilitate integration with other spatial layers (wildflower patches, bare ground, grazed areas).
- CSV format enables straightforward import into GIS for visualization and spatial analysis of reproductive outcomes across habitat contexts.

## Quality, scope, and provenance
- Dataset is complete and self-contained within the single CSV file.
- Part of a larger experiment examining the effect of floral resources on pollination services to isolated plants.
- Collected and interpreted by Evans, T.M.