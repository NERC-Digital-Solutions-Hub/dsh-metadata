# The seed set of supplemented and pollinator exposed flowers from Eschscholzia californica plants located within habitats comprising different floral cover

## Overview
- Dataset documenting seed production for pollinator-exposed vs pollen-supplemented Eschscholzia californica.
- Collected in June 2015 at Hillesden estate, Buckinghamshire, UK.
- Experimental design includes 16 arrays across four 100-hectare replicate blocks; arrays positioned along transects across habitat boundaries (florally rich vs florally poor).
- Part of a larger study on how floral resources affect pollination services to isolated plants.
- Complete dataset, collected and interpreted by T.M. Evans.

## Experimental design
- Each array contains three E. californica plants (1 m apart) in a triangular arrangement.
- Four replicate blocks; within each block, four arrays (two in florally rich, two in florally poor habitats) at 50 m intervals along a 150 m transect.
- Plants grown from seed and introduced to field sites to form the experimental arrays.

## Collection methods
- All open flowers removed prior to field placement; plants remained for 16 days to ensure full anthesis and multiple pollination events.
- On day 16, one flower per plant (48 plants total) was supplemented with outcrossed pollen via donor plant pollen transfer.
- Supplemented flowers protected with muslin to prevent wind-borne pollen from other sources.
- Fruits collected and stored under controlled glasshouse conditions until maturation.
- Seed set quantified as the mean number of seeds per fruit; pollen limitation expressed as the ratio of field-exposed mean seeds to supplemented mean seeds.

## Data structure and units
- Data stored in a single CSV: The_seed_set_of_supplemented_and_pollinator_exposed_E.californica_flowers.csv
- Key columns:
  - Block: replicate block identifier
  - Experimental_array: array identifier within a block
  - Plant_identification_number: plant ID in the field
  - Habitat: florally rich vs florally poor location
  - Treatment: field-exposed vs supplemented
  - Mean_number_of_seeds_from_field_exposed_flowers: average seeds per fruit from exposed flowers
  - Number_of_fruits: number of fruits used for the mean
  - Number_of_seeds_from_supplemented_flowers: seed count from supplemented flowers
- NA indicates supplemented flowers did not survive.

## Purpose and interpretation
- Objective: quantify pollen limitation and relate it to habitat context.
- Derived metric: ratio of field-exposed seed set to supplemented seed set.
- Documentation notes that the dataset is part of a broader investigation into how floral resources influence pollination services.
- Evans, T.M. is the data origination and interpretation authority.

## Supporting documentation
- Title: The seed set of supplemented and pollinator exposed flowers from Eschscholzia californica plants located within habitats comprising different floral cover.

## Data quality and governance (Data Steward perspective)
- Rich, explicit metadata with clear experimental design, locations, treatments, and data fields.
- Standardized data file naming and structure; single CSV with well-defined columns and units.
- Complete coverage: 48 plants across 16 arrays, aligned with the described design.
- Documentation includes provenance (collection and interpretation by Evans, T.M.) and purpose within a larger study.
- Considerations for governance: ensure licensing, long-term accessibility, and clear mapping between Habitat/Treatment labels and any external schemas; maintain provenance and versioning if data are updated or reprocessed.