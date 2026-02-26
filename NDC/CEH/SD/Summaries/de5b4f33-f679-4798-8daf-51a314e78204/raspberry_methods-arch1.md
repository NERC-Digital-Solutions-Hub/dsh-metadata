# Additional information about the raspberry fruit set, measurements, and seed number data set

## Overview
- A multi-file dataset describing raspberry fruit set, marketability, size, and seed counts from a study conducted in Reading, UK (2019–2021, July–September).
- Data collected to analyze how pollination treatment and field position affect fruit set, marketable fruit set, fruit size, and seed numbers.

## Data files and key variables
- Fruit_set.csv (13 columns)
  - Cultivar, Year, Plant, Plant_ID, Location, Treatment
  - Fruit_set, Marketable_fruit_set, Fruit, Marketable
  - Marketability failures, No of flowers, Fruit failures
- Fruit_measurements.csv (11 columns)
  - Year, Cultivar, Plant, Location, Treatment
  - Berry no, Marketable Reason, Length.mm, Width, Weight
- Seed_no.csv (11 columns)
  - Year, Cultivar, Plant, Treatment
  - Berry.no, Marketable, Length, Width, Weight, Drupelet.seed.number, bins
- metadata.csv
  - Explanations for every variable in the other files

## Study design and context
- Location: Soft fruit farm in Reading, UK; multiple fields
- Time frame: July–September 2019–2021
- Field treatments: Field edge (<20 m from field edge) and internal (>20 m from field edge)
- Pollination treatments (4 total): 
  - Insect pollinated
  - Insect Excluded
  - Insect pollinated with hand pollen supplementation
  - Insect exclusion with hand pollen supplementation
- Plant selection: Study plants randomly located within each field and treated accordingly

## Sampling and data collection details
- Final dataset: 273 study plants after exclusions
- Flowers and fruits: 2733 flowers produced 2456 ripe fruit; 1991 marketable fruit
- Measurements and weighing:
  - 2179 fruit weighed; most weighed fruits also measured
  - Crumbly fruit weighed but not measured
  - 277 berries not measured
  - 110 berries harvested by commercial pickers when ripe and marketable
  - Berries collected from 2019 not weighed/measured (n = 148); remaining 19 not measured due to death after ripening
- Size measurements: Length (mm), Width (mm) at longest/widest berry parts
- Seed data: Seed counts (subset) documented in Seed_no.csv

## Exclusions and data cleaning
- Excluded plants/fruit with fungal infection (Phytophthora) and branches damaged by humans
- After exclusions: 273 plants included in the final data set

## Data quality and usage considerations
- Data span multiple years and treatments, enabling cross-treatment comparisons
- Requires integration across four CSVs to link fruit set, marketability, size, and seed data via Year, Cultivar, Plant, Location, Treatment
- Some data gaps due to measurement status (e.g., 148 berries from 2019 not weighed/measured; 19 not measured due to death)
- Metadata file provides variable definitions and context to support robust analysis

## Potential analyses for data-driven insights
- Effect of pollination treatment on:
  - Fruit set rate and marketable fruit set
  - Proportion of marketable fruits among ripe fruits
- Influence of field position (edge vs internal) on fruit development and marketability
- Relationships between berry size (Length, Width, Weight) and marketability
- Variation in seed number (and its relationship with size/marketability) within the subset
- Cross-dataset analyses linking Fruit_set, Fruit_measurements, and Seed_no to construct predictive models
- Considerations for data cleaning and missing data imputation due to measurement gaps and 2019 data omissions

## Usage notes for analysts
- Ensure consistent keys across Fruit_set, Fruit_measurements, Seed_no, and metadata for proper data merging
- Be mindful of small sample subsets when analysing seed counts or rare treatments
- Report treatment- and location-specific effects with appropriate handling of missing/measured status and year-to-year variability