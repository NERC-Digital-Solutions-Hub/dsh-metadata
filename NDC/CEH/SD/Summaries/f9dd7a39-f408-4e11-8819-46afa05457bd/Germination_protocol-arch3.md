# The germination rates of seeds from Eschscholzia californica plants located within habitats comprising habitats with different floral cover

## Overview
- Dataset details germination rates of Eschscholzia californica seeds from field-exposed plants across habitats with different floral cover.
- Collected in June 2015 at the Hillesden estate, Buckinghamshire, UK.
- Part of a larger experiment on how floral resources influence pollination services to isolated plants.
- Data and interpretation credited to Evans, T.M.

## Experimental design
- 16 experimental arrays across four 100 ha replicate blocks, each >500 m apart.
- Each array consists of three E. californica plants arranged in a triangle (1 m spacing).
- In each block, four arrays positioned along a 150 m transect across the boundary between florally rich and florally poor habitat (two arrays in each habitat type).

## Collection and germination methods
- All open flowers removed from the 48 field-exposed plants; field exposure lasted 16 days to ensure anthesis and multiple pollination events.
- Fruits tagged to ensure only field-origin development is analyzed.
- Plants collected and stored under glasshouse conditions (day:night = 20°C:15°C; 12:12 light:dark).
- At fruit maturation, 20 seeds from each of the 48 plants sown into compost and germination tracked daily for 30 days; seeds not germinating by 90 days recorded as non-viable.
- Germination success expressed as the ratio of seeds germinated to seeds sown for each plant.

## Data structure and units
- Single CSV file: Germination_rates_of_Eschscholzia_californica_seeds.csv
- Key columns:
  - Block: replicate block ID (1–4)
  - Experimental_array: array ID within a block (1–4)
  - Plant_identification_number: plant ID before field transfer
  - Habitat: florally rich vs florally poor
  - Treatment: contextual treatment category (as recorded)
  - Number_of_seeds_germinated
  - Total_number_of_seeds_sown

## Data provenance and scope
- Dataset is complete and was collected and interpreted by Evans, T.M.
- Embedded in a larger study examining how floral resources affect pollination services to isolated plants.

## Relevance to monitoring frameworks
- Demonstrates a structured approach to collecting, documenting, and reporting ecological germination data linked to habitat quality.
- Emphasizes the importance of clear metadata, traceability to experimental design, and alignment with data-sharing and governance practices in monitoring.

## Data quality and accessibility considerations
- Well-documented data structure with explicit column definitions facilitates transparency and reproducibility.
- Data is centralized in a single CSV; however, the documentation here does not specify public accessibility beyond the dataset itself.
- Lacks ancillary covariates (e.g., weather, management history) in the description, which may affect broader comparability across studies.

## Practical considerations for monitoring use
- Useful as a baseline for germination outcomes under different floral-resource contexts.
- Can be integrated with other pollination and habitat quality metrics to inform landscape-level monitoring and policy decisions.