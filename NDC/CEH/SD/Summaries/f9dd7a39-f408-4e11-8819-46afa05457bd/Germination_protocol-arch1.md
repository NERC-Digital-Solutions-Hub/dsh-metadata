# Germination_rates_of_Eschscholzia_californica_seeds.csv

- Purpose and context
  - Dataset details germination rates of Eschscholzia californica seeds from plants introduced to habitats with different floral cover.
  - Part of a larger experiment examining how floral resources influence pollination services to isolated plants.
  - Collected in June 2015 on the Hillesden estate, Buckinghamshire, UK.

- Experimental design
  - Four replicate blocks (each ~100 ha) with 16 experimental arrays in total.
  - Each array contains three E. californica plants spaced 1 m apart in a triangular arrangement.
  - In each block, four arrays placed along a 150 m transect that spans the boundary between a florally rich wildflower patch and florally poor habitats (bare/fallow or grazed grassland); two arrays in florally rich, two in florally poor.
  - Blocks separated by more than 500 m to ensure independent replicates.

- Collection and processing
  - All open flowers removed before field placement; plants remained in the field for 16 days to complete anthesis and allow multiple pollination events.
  - Fruits tagged to ensure only development from the field period was included.
  - Plants collected and grown under controlled glasshouse conditions (light/dark cycle 12:12; 20°C day / 15°C night) until fruit maturation.
  - At maturation, 20 seeds from each of the 48 field-exposed plants sown into compost under glasshouse conditions.
  - Germination recorded daily for 30 days; seeds not germinating by 90 days counted as non-viable.
  - Germination rate expressed as the ratio of germinated seeds to total seeds sown for each plant.

- Data structure and units
  - Single CSV file: Germination_rates_of_Eschscholzia_californica_seeds.csv
  - Key columns:
    - Block: replicate block ID (1–4)
    - Experimental_array: array ID within block (1–4)
    - Plant_identification_number: plant ID assigned before field transfer
    - Habitat: florally rich vs florally poor location
    - Treatment: specific treatment/placement within habitat context
    - Number_of_seeds_germinated: count of germinated seeds per plant
    - Total_number_of_seeds_sown: seeds sown per plant (20 per plant)
  - Each of the 48 field-exposed plants contributes 20 seeds, enabling per-plant germination rate calculations.

- Location, timing, and authorship
  - Hillesden estate, Buckinghamshire, UK; June 2015.
  - Experimental design, collection, and interpretation conducted by T.M. Evans.

- Supporting documentation
  - Title: The germination rates of seeds from Eschscholzia californica plants located within habitats comprising habitats with different floral cover (dataset description and context).