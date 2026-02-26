# The germination rates of seeds from Eschscholzia californica plants located within habitats comprising habitats with different floral cover

## Overview
- Dataset describes germination rates of Eschscholzia californica seeds following a field exposure across habitats with different floral cover.
- Location and timing: Hillesden estate, Buckinghamshire, UK, June 2015.
- Context: Part of a larger experiment on how floral resources affect pollination services to isolated plants.
- Experimental scope: 48 field-exposed E. californica plants arranged in 16 triangular arrays across four 100-hectare replicate blocks, with arrays positioned along a transect spanning florally rich and florally poor habitats.

## Spatial design and sampling
- Experimental layout:
  - Four replicate blocks (each ~100 ha) with >500 m separation between blocks.
  - Each block contains four experimental arrays; arrays are 50 m apart along a 150 m transect that crosses the boundary between florally rich wildflower patches and florally poor ground (bare/fallow or grazed grassland).
  - Across all blocks, 16 arrays total.
- Array and plant arrangement:
  - Each array comprises three E. californica plants spaced 1 m apart in a triangular configuration.
- Habitat differentiation:
  - Two arrays per block within florally rich habitats and two within florally poor habitats.
- Sampling structure:
  - Each plant is identified individually (Plant_identification_number) and associated with a specific array (Experimental_array) and block (Block).

## Experimental methodology
- Field procedure:
  - All open flowers removed prior to placement; field exposure lasted 16 days to ensure full anthesis and multiple pollination events.
  - Fruit were tagged to ensure analyses included only fruit from the field period.
- Post-field handling:
  - Plants collected and stored under controlled glasshouse conditions (14–16 hr day/night cycle with 20°C/15°C temperatures as specified).
  - At maturity, 20 seeds from each of the 48 plants were sown into compost and maintained under glasshouse conditions.
- Germination recording:
  - Germination tracked daily over a 30-day period.
  - Seeds not germinating by 90 days were recorded as non-viable.
- Metrics:
  - Germination success expressed as the ratio of germinated seeds to seeds sown for each plant.

## Data structure and units
- Data file: Germination_rates_of_Eschscholzia_californica_seeds.csv
- Key columns:
  - Block: replicate block identification (one of four blocks).
  - Experimental_array: identification number for each of the four arrays within a block.
  - Plant_identification_number: unique ID for each plant prior to field transfer.
  - Habitat: location category where the array was positioned ( florally rich vs florally poor).
  - Treatment: experimental condition/location descriptor associated with the array.
  - Number_of_seeds_germinated: count of seeds that germinated for that plant.
  - Total_number_of_seeds_sown: total seeds sown for that plant (20 per plant).
- Notes:
  - 48 plants across 16 arrays (three plants per array) were sampled.
  - The dataset is complete and was interpreted by Evans, T.M.