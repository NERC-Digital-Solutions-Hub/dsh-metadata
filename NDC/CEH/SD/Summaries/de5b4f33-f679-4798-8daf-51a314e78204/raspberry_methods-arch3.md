# Additional information about the raspberry fruit set, measurements, and seed number data set

## Overview
- Describes a dataset on raspberry fruit set, measurements, and seed counts across four pollination treatments.
- Comprises four CSV files: Fruit_set.csv, Fruit_measurements.csv, Seed_no.csv, and metadata.csv.
- Collected at a soft fruit farm in Reading, UK, in multiple fields during July–September 2019–2021.
- Study design includes two location treatments (Field edge <20 m from edge; internal >20 m) and four pollination treatments (Insect pollinated, Insect Excluded, Insect pollinated with hand pollen supplementation, Insect exclusion with hand pollen supplementation).
- Measurements include fruit set, marketable fruit set, fruit size (length, width), weight, and a subset of seed counts.
- Data processing includes exclude criteria for fungal infection and physical damage; final dataset comprises 273 study plants.

## Data files and key variables
- Fruit_set.csv (13 columns)
  - Cultivar, Year, Plant, Plant_ID, Location, Treatment
  - Fruit_set, Marketable_fruit_set, Fruit, Marketable, Marketability_failures
  - No_of_flowers, Fruit_failures
- Fruit_measurements.csv (11 columns)
  - Year, Cultivar, Plant, Location, Treatment
  - Berry_no, Marketable_Reason, Length.mm, Width, Weight
- Seed_no.csv (11 columns)
  - Year, Cultivar, Plant, Treatment
  - Berry.no, Marketable, Length, Width, Weight
  - Drupelet.seed.number, bins
- metadata.csv
  - Explanations of each variable for all three data files.

## Study design and data collection
- Plants randomly located within fields under two location treatments: Field edge and internal.
- Four pollination treatments as described above.
- Fruits weighed in grams; berry length and width measured in mm using calipers.
- A subset across treatments and cultivars weighed; lengths and widths measured where possible.
- A subset of fruits had seeds counted.

## Processing, exclusions, and dataset summary
- Exclusions: plants infected with Phytophthora and branches damaged by humans.
- Final data: 273 study plants.
- Totals: 2733 flowers produced 2456 ripe fruit; 1991 marketable fruit.
- Weighing and measuring: 2179 fruit weighed; majority measured; some crumbly fruit weighed but not measured; 277 berries not measured (110 harvested by commercial pickers when ripe and marketable; 148 berries from 2019 not weighed/measured; 19 not measured due to death after ripening).
- Seeds: seed counts available for a subset via Seed_no.csv.

## Data quality, governance, and provenance
- Metadata.csv provides explanations for all variables to support data understanding and reuse.
- Data are collected and processed by Imogen Ryan with interpretation by Imogen Ryan and Lynn Dicks.
- Highlights transparency in data handling, exclusions, and measurement approaches, aiding reproducibility and cross-study comparisons.

## Relevance for monitoring frameworks
- Demonstrates how to structure environmental health data across treatments, locations, and phenotypic measurements.
- Emphasizes metadata completeness, data cleaning, and data provenance to support governance and policy-relevant analyses.
- Provides a concrete example of handling data gaps (missing measurements, unmeasured berries) and documenting exclusions for monitoring outputs.