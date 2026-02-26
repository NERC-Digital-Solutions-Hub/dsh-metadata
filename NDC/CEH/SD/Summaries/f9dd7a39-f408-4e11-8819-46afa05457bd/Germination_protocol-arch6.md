# The germination rates of seeds from Eschscholzia californica plants located within habitats comprising habitats with different floral cover

## Overview
- Datasets germination rates of Eschscholzia californica seeds from field-exposed plants across habitats with different floral cover.
- Collected in June 2015 at Hillesden estate, Buckinghamshire, UK.
- Part of a larger experiment examining how floral resources affect pollination services to isolated plants.
- Dataset is complete and was collected and interpreted by Evans, T.M.
- Supporting documentation exists for the dataset.

## Experimental design
- Experimental arrays: 16 arrays across four replicate blocks (each 100 ha) spaced >500 m apart.
- Within blocks: central arrangement along a 150 m transect crossing the boundary between florally rich and florally poor habitats; two arrays in each habitat type per block.
- Each array comprises three Eschscholzia californica plants, spaced 1 m apart in a triangular formation.
- Blocks arranged so arrays are located across habitat contrasts to assess effects of floral cover.

## Collection methods
- All open flowers removed from the 48 plants before field placement.
- Field exposure lasted 16 days to ensure full anthesis and multiple pollination events.
- Fruits tagged to ensure only period-specific fruit development is analyzed.
- Plants collected and stored under controlled glasshouse conditions (day:night 20°C:15°C; light:dark 12:12 h).
- At maturity, 20 seeds from each of the 48 plants sown into compost and kept under glasshouse conditions.
- Germination recorded daily for 30 days; seeds not germinating by 90 days treated as non-viable.
- Germination success expressed as the ratio of germinated seeds to seeds sown for each plant.

## Data structure and variable definitions
- Data file: Germination_rates_of_Eschscholzia_californica_seeds.csv (single CSV).
- Key columns:
  - Block: replicate block ID (4 blocks)
  - Experimental_array: array ID within a block (4 arrays per block)
  - Plant_identification_number: plant ID assigned before field transfer
  - Habitat: location category ( florally rich vs florally poor)
  - Treatment: contextual factor (defined in dataset; details not expanded in summary)
  - Number_of_seeds_germinated: count of germinated seeds per plant
  - Total_number_of_seeds_sown: seeds sown per plant (20 per plant)
- Total observations: 48 plants (one per array), yielding 960 seeds seeded; dataset described as complete.

## Dataset provenance and completeness
- The dataset is part of a larger study on floral resource effects on pollination services.
- Completed and interpreted by Evans, T.M.
- Supporting documentation explicitly titled: “The germination rates of seeds from Eschscholzia californica plants located within habitats comprising habitats with different floral cover.”

## Potential analyses and data-use guidance for data support
- Compute per-plant germination rates (Number_of_seeds_germinated / Total_number_of_seeds_sown) and compare across Habitats (rich vs poor) and Treatments.
- Assess block and array-level variation to evaluate spatial effects and experimental design robustness.
- Integrate with related data on pollination services to link germination outcomes with pollination metrics.
- Create dashboards or pivot views to enable self-serve exploration of germination outcomes across habitat contexts.
- Use the complete dataset to promote data reuse, replication, and sharing of early prototypes for broader applications.