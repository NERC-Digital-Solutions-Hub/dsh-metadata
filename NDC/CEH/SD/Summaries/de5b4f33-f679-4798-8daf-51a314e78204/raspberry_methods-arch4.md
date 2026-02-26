# Additional information about the raspberry fruit set, measurements, and seed number data set

## Data assets (files)
- Four CSV files: Fruit_set.csv, Fruit_measurements.csv, Seed_no.csv, metadata.csv
- metadata.csv provides explanations of each variable across all files
- Fruit_set.csv (13 columns): Cultivar, Year, Plant, Plant_ID, Location, Treatment, Fruit_set, Marketable_fruit_set, Fruit, Marketable, Marketability failures, No of flowers, Fruit failures
- Fruit_measurements.csv (11 columns): Year, Cultivar, Plant, Location, Treatment, Berry no, Marketable Reason, Length.mm, Width, Weight
- Seed_no.csv (11 columns): Year, Cultivar, Plant, Treatment, Berry.no, Marketable, Length, Width, Weight, Drupelet.seed.number, bins
- Data represent fruit production from raspberry flowers of two varieties under four pollination treatments, shown as both percentage fruit set and marketable fruit set, and as a success:failure vector
- Includes number of flowers per treatment; fruit measurements (length, width, weight) provided in a separate file; seed counts documented for a subset

## Study design and data collection
- Location: soft fruit farm, Reading, UK; fields sampled July–September 2019–2021
- Experimental layout: study plants randomly located within each field
- Location treatments: Field edge (<20 m from non-cropped field edge) and internal (>20 m from field edge)
- Pollination treatments (4): Insect pollinated, Insect Excluded, Insect pollinated with hand pollen supplementation, Insect exclusion with hand pollen supplementation
- Measurements: fruit weighed in grams; length and width measured at the longest dimensions using calipers
- Seed counts: subset across pollination treatments and cultivars counted in a weight bin–based selection
- Data collection and initial processing by Imogen Ryan; analysis and interpretation by Imogen Ryan and Lynn Dicks

## Data processing and quality control
- Exclusions applied: plants infected with Phytophthora (fungal pathogen) and branches damaged by humans
- Final dataset: 273 study plants included
- Totals: 2733 flowers produced 2456 ripe fruit; 1991 marketable fruit
- Weighing/measurement: 2179 fruit weighed; majority measured; crumbly fruit weighed but not measured
- Unmeasured berries: 277 not measured; among these, 110 harvested by commercial pickers when ripe and marketable; berries from 2019 not weighed/measured (148); remaining 19 unmeasured due to ripening death