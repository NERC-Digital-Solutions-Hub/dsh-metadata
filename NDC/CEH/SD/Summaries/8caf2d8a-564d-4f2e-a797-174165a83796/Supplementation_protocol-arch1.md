# The_seed_set_of_supplemented_and_pollinator_exposed_E.californica_flowers.csv

- Objective and context
  - Dataset quantifies seed production for Eschscholzia californica plants exposed to pollinators versus those supplemented with outcrossed pollen.
  - Investigates pollen limitation across habitats with different floral cover.
  - Field work conducted in June 2015 at Hillesden estate, Buckinghamshire, UK.
  - Experimental focus within a larger study on how floral resources affect pollination services to isolated plants.

- Experimental design
  - Four replicate blocks, each 100 hectares.
  - Within each block, four experimental arrays (triangular group of three plants, 1 m apart).
  - 16 arrays total across blocks.
  - Arrays positioned along a 150 m transect crossing the boundary between florally rich wildflower patches and florally poor habitat (bare fallow or grazed grassland).
  - In each block: two arrays in florally rich habitat and two in florally poor habitat.

- Collection methods
  - All open flowers removed from 48 plants before placement in the field.
  - Field exposure period: 16 days to ensure anthesis and multiple pollination events.
  - After 16 days, one flower per plant received outcrossed pollen via careful pollen transfer.
  - Fruits tagged and supplemented flowers protected from unintended pollen transfer.
  - Fruits collected and stored under controlled glasshouse conditions until maturation.
  - Seed set per fruit counted to quantify reproductive output.
  - Pollen limitation expressed as the ratio of mean seed set from field-exposed flowers to seed set from supplemented flowers.

- Data structure and units
  - Single CSV: The_seed_set_of_supplemented_and_pollinator_exposed_E.californica_flowers.csv
  - Columns:
    - Block: replicate block identifier
    - Experimental_array: array identifier within a block
    - Plant_identification_number: plant ID (pre-field transfer)
    - Habitat: florally rich vs florally poor location
    - Treatment: field-exposed vs supplemented
    - Mean_number_of_seeds_from_field_exposed_flowers: average seeds per fruit for field-exposed flowers
    - Number_of_fruits: fruits from which seed sets are averaged
    - Number_of_seeds_from_supplemented_flowers: seed count for supplemented flowers
  - Notes: NA appears when supplemented flowers did not survive

- Data quality, provenance, and documentation
  - Dataset is complete and intended for detailed pollen-limitation analysis.
  - Collected and interpreted by Evans, T.M.
  - Supporting documentation available under the title related to the seed set of supplemented and pollinator-exposed flowers in habitats with varying floral cover.

- Analytical considerations and potential uses
  - Compute pollen limitation per plant, array, or block using the provided seed counts.
  - Assess effects of Habitat (rich vs poor) on pollen limitation, potentially controlling for Block and Array effects.
  - Suitable for mixed-effects modeling (e.g., random effects for Block/Array; fixed effects for Habitat/Treatment).
  - Explore correlations between mean field seed set and habitat context, considering the number of fruits as a weighting factor.
  - Caveats: single species, specific geographic location, and NA values for failed supplemented flowers; results may require scale-up for broader generalizations.