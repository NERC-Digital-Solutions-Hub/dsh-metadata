# Additional information about the raspberry fruit set, measurements, and seed number data set

## Overview
- A multi-file raspberry dataset containing fruit set, fruit measurements, seed counts, and accompanying metadata.
- Four CSV files: Fruit_set.csv, Fruit_measurements.csv, Seed_no.csv, and metadata.csv.
- Metadata explains every variable across the data files.
- Designed to capture how pollination treatment, location within fields, cultivar, and year affect fruit production, weight, size, and seed counts.

## Data Files and Key Variables
- Fruit_set.csv (13 columns)
  - Cultivar, Year, Plant, Plant_ID, Location, Treatment, Fruit_set, Marketable_fruit_set, Fruit, Marketable, Marketability_failures, No_of_flowers, Fruit_failures
- Fruit_measurements.csv (11 columns)
  - Year, Cultivar, Plant, Location, Treatment, Berry_no, Marketable_Reason, Length.mm, Width, Weight
- Seed_no.csv (11 columns)
  - Year, Cultivar, Plant, Treatment, Berry.no, Marketable, Length, Width, Weight, Drupelet.seed.number, bins
- metadata.csv
  - Explanations of every variable in the above files

## Study Design and Geography
- Location: soft fruit farm in Reading, United Kingdom; data collected in multiple fields during July–September 2019–2021.
- Field location treatments: Field edge (<20 m from the non-cropped field edge) and internal (>20 m from the edge).
- Raspberry varieties: two cultivars.
- Pollination treatments (four levels):
  - Insect pollinated
  - Insect Excluded
  - Insect pollinated with hand pollen supplementation
  - Insect exclusion with hand pollen supplementation
- Measurements and data collection:
  - Fruit produced from study flowers; weighed (g) and measured (Length.mm, Width) with calipers.
  - Number of flowers per treatment; fruit set and marketable fruit set reported as percentages and as a success:failure vector.
  - Subset of fruits used to count seeds (seed number) per berry.
  - Data processing and analysis credited to Imogen Ryan (with collaboration from Lynn Dicks).

## Data Processing and Quality Control
- Exclusions:
  - Plants infected with Phytophthora (fungal pathogen) and branches damaged by humans removed.
- Final dataset: 273 study plants.
- Totals across the dataset:
  - 2733 flowers produced
  - 2456 ripe fruit
  - 1991 marketable fruit
  - 2179 fruit weighed; majority also measured
  - Some fruit weighed but not measured (crumbly fruit)
  - 277 berries not measured (with explanations for subsets):
    - 110 berries harvested by commercial pickers when ripe and marketable
    - 148 berries collected in 2019 not weighed/measured
    - 19 berries not measured because fruit were found dead after ripening

## Measurements and Derived Metrics
- Fruit_set and Marketable_fruit_set: reported as percentages and as a success:failure vector (set vs. not marketable).
- Physical measurements:
  - Length (mm), Width (mm), Weight (g) for individual fruits
- Seed data:
  - Drupelet seed number recorded for a subset of berries
  - Additional fields include Berry.no, Weight, Length, Width, and a bins variable

## GIS-Relevant Considerations and Potential Applications
- Spatial integration:
  - Link cultivar, year, treatment, and location to spatial coordinates of the fields to visualize and analyze spatial patterns in fruit set, marketability, size, and seed counts.
  - Compare edge vs internal field effects on fruit set and quality.
- Temporal analysis:
  - Explore changes across years (2019–2021) and potential interactions with treatments and locations.
- Data integration:
  - Use metadata.csv to accurately map variable definitions to GIS attributes.
  - Potential to combine with environmental or management layers (e.g., pest management, weather, field boundaries) for spatial analyses.
- Visualization opportunities:
  - Map-based displays of fruit set percentages by treatment and location.
  - Spatial distribution of fruit weights and dimensions across fields and years.
  - Seed-number distributions by cultivar, treatment, and location.

## Notes
- The dataset provides rich, multi-dimensional fruit production data suitable for map-based visualization and spatial analysis, with careful attention to metadata and data quality controls.