# Additional information about the raspberry fruit set, measurements, and seed number data set

- Purpose and scope
  - A consolidated data set describing raspberry fruit set, fruit measurements, and seed counts from a field study.
  - Enables analysis of pollination treatments, plant location, and cultivar effects on fruit production and quality.

- Data files and metadata
  - Four CSV files: Fruit_set.csv, Fruit_measurements.csv, Seed_no.csv, metadata.csv.
  - metadata.csv provides explanations for every variable across the other files.
  - Data typed and organized with explicit columns to support reuse and interoperability.

- Study design and collection context
  - Location: soft fruit farm in Reading, UK; data collected during July–September 2019–2021.
  - Experimental factors:
    - Two field location treatments: Field edge (<20 m from edge) and internal (>20 m from edge).
    - Four pollination treatments: Insect pollinated; Insect excluded; Insect pollinated with hand pollen supplementation; Insect exclusion with hand pollen supplementation.
  - Plant selection: Study plants randomly located within each field and treatment.
  - Measurements:
    - Fruit production: number of flowers, fruit set, marketable fruit set, and associated success/failure counts.
    - Fruit quality: weight (grams), length and width (mm) measured with calipers; subset of berries weighed and measured.
    - Seeds: number of seeds counted in a subset of fruits.
  - Data processing and authorship: Data collected and processed by Imogen Ryan; analysis and interpretation by Imogen Ryan and Lynn Dicks.

- Variables and data structure
  - Fruit_set.csv (13 columns): Cultivar, Year, Plant, Plant_ID, Location, Treatment, Fruit_set, Marketable_fruit_set, Fruit, Marketable, Marketability failures, No of flowers, Fruit failures.
  - Fruit_measurements.csv (11 columns): Year, Cultivar, Plant, Location, Treatment, Berry no, Marketable Reason, Length.mm, Width, Weight.
  - Seed_no.csv (11 columns): Year, Cultivar, Plant, Treatment, Berry.no, Marketable, Length, Width, Weight, Drupelet.seed.number, bins.
  - All datasets capture treatment, location, cultivar, year, plant identifiers, and outcome/measurement variables using consistent units (mm, g).

- Data quality, curation, and exclusions
  - Exclusions applied to ensure data quality: plants infected with Phytophthora or branches damaged by humans were removed.
  - Final dataset composition after filtering: 273 study plants.
  - Production outcomes: 2733 flowers → 2456 ripe fruit → 1991 marketable fruit.
  - Measurements: 2179 fruit weighed; majority measured; some fruit crumbly or not measured due to quality or handling.
  - Additional notes: 277 berries not measured; 110 berries harvested by commercial pickers when ripe and marketable; berries from 2019 not weighed/measured (148 not weighed; 19 not measured due to post-ripening death).

- Data governance and sharing considerations
  - Metadata provides variable definitions to support proper interpretation and reuse.
  - Clear provisioning of identifiers (Plant, Plant_ID) supports traceability across treatments and locations.
  - Documentation supports reproducibility and potential re-use in meta-analyses or cross-study comparisons.
  - Users should note the exclusions and subset-specific measurements when analyzing seed numbers and fruit quality.