# Additional information about the raspberry fruit set, measurements, and seed number data set

## Overview
- A multi-file raspberry dataset describing fruit set, measurements, and seed counts across two cultivars, four pollination treatments, and two location treatments in field conditions.
- Data captured in Reading, UK, during July–September across 2019–2021; designed to enable analysis of how pollination and site position affect fruit production, quality, and seed content.
- Includes both raw counts (e.g., flowers, ripe fruit, marketable fruit) and continuous measurements (berry length, width, weight) plus seed counts for a subset.

## Data files and key variables
- Fruit_set.csv (13 columns)
  - Cultivar, Year, Plant, Plant_ID, Location, Treatment, Fruit_set, Marketable_fruit_set, Fruit, Marketable, Marketability failures, No of flowers, Fruit failures
- Fruit_measurements.csv (11 columns)
  - Year, Cultivar, Plant, Location, Treatment, Berry no, Marketable Reason, Length.mm, Width, Weight
- Seed_no.csv (11 columns)
  - Year, Cultivar, Plant, Treatment, Berry.no, Marketable, Length, Width, Weight, Drupelet.seed.number, bins
- metadata.csv
  - Explanations of variables for all files

## Study design and data collection
- Location and timing
  - Soft fruit farm in Reading, UK; fields sampled July–September 2019–2021
- Field layout
  - Two location treatments: Field edge (<20 m from non-cropped edge) and internal (>20 m from edge)
- Pollination treatments (4 total)
  - Insect pollinated
  - Insect Excluded
  - Insect pollinated with hand pollen supplementation
  - Insect Exclusion with hand pollen supplementation
- Measurements
  - Fruits weighed (grams) and measured for length and width with calipers
  - Subset across treatments and cultivars used for seed counting
- Plant and fruit scope
  - Plants randomly located within fields
  - Study excluded plants infected with Phytophthora and branches damaged by humans
  - Final data set includes 273 study plants

## Data processing and final dataset
- Cleaning steps
  - Excluded phytophthora-infected plants and damaged branches
- Final counts
  - 273 study plants included
  - 2733 flowers produced
  - 2456 ripe fruit
  - 1991 marketable fruit
  - 2179 fruit weighed; most also measured
  - Some fruit weighed but not measured (crumbly fruit)
  - 277 berries not measured; 110 harvested by commercial pickers when ripe and marketable
  - Berries collected from 2019 largely not weighed/measured (148 not weighed/measured; 19 not measured due to death after ripening)
- Data presentation
  - Contains both percent fruit set and percent marketable fruit set
  - Includes a success:failure vector for fruit set and marketability

## Measurements and quality metrics
- Measurements
  - Berry length (mm), width (mm), weight (g)
- Subsampled data
  - Seed counts (drupelet seed number) available for a subset of berries
- Data notes
  - Marketable versus non-marketable distinctions captured
  - Metadata file provides detailed variable explanations to support interpretation

## Provenance and authorship
- Collected by Imogen Ryan; analysis and interpretation performed by Imogen Ryan and Lynn Dicks
- Data designed to support broader data exploration, combination with other datasets, and creation of self-serve data products (e.g., dashboards, summaries)

## Potential uses and practical considerations
- Analyses of how pollination treatment and field location influence:
  - Fruit set rates and marketability
  - Fruit size (length, width), weight, and overall quality
  - Seed content in subset of berries
- Opportunities to build data products for end users (e.g., dashboards showing treatment effects, site position effects, and year-to-year trends)
- Important caveats
  - Some data gaps due to non-measured berries (e.g., 2019 berries not weighed/measured)
  - Exclusions applied (phytophthora infections, physical damage) may limit generalizability to untreated populations
  - Variability across years and field conditions should be accounted for in analyses

## Summary relevance for data support
- Provides a well-documented, multi-faceted dataset ready for integration with other data sources
- Clear variable definitions and metadata facilitate data cleaning, validation, and transformation for end-user analytics
- Structure supports creating self-serve analytics, dashboards, and reports on pollination effects, fruit quality, and seed characteristics across treatments and sites