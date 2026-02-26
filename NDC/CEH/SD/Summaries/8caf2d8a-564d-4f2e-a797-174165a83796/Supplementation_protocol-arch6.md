# The seed set of supplemented and pollinator exposed flowers from Eschscholzia californica plants located within habitats comprising different floral cover.

## Overview
- Dataset on seeds produced by Eschscholzia californica plants under two treatments: pollinator-exposed vs supplemented with outcrossed pollen.
- Samples collected in June 2015 at Hillesden estate, Buckinghamshire, UK.
- Study investigates pollen limitation across habitats with different floral cover (florally rich vs florally poor) as part of a larger experiment on floral resources and pollination services.
- Data interpreted by Evans, T.M.

## Experimental design
- Experimental arrays: 16 arrays across four 100-hectare replicate blocks (>500 m apart).
- Each array contains three E. californica plants, 1 m apart, in a triangular arrangement.
- Within each block, four arrays positioned along a 150 m transect crossing the boundary between florally rich and florally poor habitats (two arrays in each habitat type).
- Plants grown from seed and introduced to field sites.

## Collection methods
- All open flowers removed from 48 plants before field placement.
- Field exposure in situ for 16 days to allow multiple pollination events.
- After 16 days, one flower per plant supplemented with outcrossed pollen (via wiping four dehiscing anthers from a donor plant onto the stigma).
- Supplemented flowers covered with fine muslin to prevent windborne pollen contamination from HVAC.
- Fruits collected and stored under controlled glasshouse conditions (day:night = 20°C:15°C; photoperiod 12:12).
- Seed set quantified by counting filled seeds per fruit.
- Pollen limitation expressed as the ratio of mean seed set from field-exposed flowers to seed set from supplemented flowers.

## Data structure and units
- Data file: The_seed_set_of_supplemented_and_pollinator_exposed_E.californica_flowers.csv
- Key columns:
  - Block: replicate block identifier (four blocks)
  - Experimental_array: array identifier within a block (four per block)
  - Plant_identification_number: plant ID before field deployment
  - Habitat: florally rich or florally poor location
  - Treatment: pollinator-exposed or supplemented
  - Mean_number_of_seeds_from_field_exposed_flowers: average seeds per fruit for field-exposed flowers
  - Number_of_fruits: number of fruits used to compute seed set
  - Number_of_seeds_from_supplemented_flowers: seeds per fruit for supplemented flowers
- Note: NA indicates supplemented flowers did not survive.

## Context and interpretation
- Part of a broader study examining how floral resources influence pollination services to isolated plants.
- Data interpretation completed by Evans, T.M.

## Practical considerations for data users
- Focused on a single field site and a single collection period (June 2015); consider spatial and temporal limitations.
- Missing data (NA) for some supplemented flowers; plan analyses accordingly (e.g., pairwise comparisons with available pairs).
- Useful for assessing habitat-context effects on pollen limitation and the efficacy of pollen supplementation as a method to estimate potential seed set.