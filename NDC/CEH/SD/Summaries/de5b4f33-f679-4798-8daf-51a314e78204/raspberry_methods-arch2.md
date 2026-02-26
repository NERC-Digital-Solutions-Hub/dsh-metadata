# Additional information about the raspberry fruit set, measurements, and seed number data set

## Overview
- Describes four related CSV data files (Fruit_set.csv, Fruit_measurements.csv, Seed_no.csv, metadata.csv) that document raspberry fruit production, fruit characteristics, and seed counts.
- Context: measurements from two raspberry varieties under four pollination treatments, collected at a soft fruit farm in Reading, UK during July–September 2019–2021.
- Study design includes spatial variation (Field edge vs internal) and randomized plant placement within each field.

## Data files and key variables
- Fruit_set.csv (13 columns)
  - Cultivar, Year, Plant, Plant_ID, Location, Treatment
  - Fruit_set, Marketable_fruit_set, Fruit, Marketable, Marketability failures, No of flowers, Fruit failures
- Fruit_measurements.csv (11 columns)
  - Year, Cultivar, Plant, Location, Treatment
  - Berry no, Marketable Reason, Length.mm, Width, Weight
- Seed_no.csv (11 columns)
  - Year, Cultivar, Plant, Treatment, Berry.no, Marketable, Length, Width, Weight, Drupelet.seed.number, bins
- metadata.csv
  - Explanations of variables for all other files

## Study design and data collection
- Study plants: two raspberry varieties, randomly located across fields.
- Treatments (4 pollination treatments):
  - Insect pollinated
  - Insect Excluded
  - Insect pollinated with hand pollen supplementation
  - Insect Exclusion with hand pollen supplementation
- Spatial treatments: Field edge (<20 m from non-cropped edge) and internal (>20 m from edge).
- Measurements:
  - Fruit weighed (grams) and measured (length and width in mm) using calipers.
  - A subset across pollination treatments and cultivars selected for weight-based binning; seeds counted in a subset.
- Processors: Imogen Ryan collected and processed; analysis and interpretation by Imogen Ryan and Lynn Dicks.
- Exclusions: Plants infected with Phytophthora, branches damaged by humans excluded.
- Final dataset: 273 study plants after exclusions.

## Data completeness and sample sizes
- Flowers and fruit
  - 2733 flowers produced
  - 2456 ripe fruit
  - 1991 marketable fruit
- Measurements and weight
  - 2179 fruit weighed
  - Majority of weighed fruit also measured (length/width)
  - Some fruit weighed but not measured (crumbly fruit)
- Non-measured samples
  - 277 berries not measured
  - 110 berries harvested by commercial pickers when ripe and marketable (not necessarily measured)
  - Berries collected in 2019 not weighed/measured (148); remaining unmeasured due to fruit dead after ripening (19)
- Final data scope: 273 study plants, with 2733 flowers, 2456 ripe fruit, and 1991 marketable fruit included after quality control

## Metadata and data quality
- Detailed explanations of all variables provided in metadata.csv to facilitate consistent interpretation and reuse.
- Data quality controls include removal of diseased or damaged plants/structures and standardized measurement procedures.

## Potential uses for environmental monitoring
- Assess pollination treatment effectiveness and its interaction with field position on fruit set and marketability.
- Track environmental or management-related factors influencing fruit size (length, width) and weight, and correlate with seed counts.
- Use standardized formats to enable cross-study comparisons and integration with other environmental datasets.
- Facilitate data sharing and secondary analyses by providing comprehensive metadata and clearly defined variables.

## Accessibility and reuse considerations
- Data are organized for clear downstream analysis (standardized fields, documented treatments, and explicit QC criteria).
- Encourages broader use by enabling integration with additional environmental data and by providing accessible metadata to support reproducibility.