# Sampling regime

- Temporal coverage
  - Data span: March 2016 to March 2019
  - Sampling frequency:
    - March 2016 – July 2017: fortnightly
    - August 2017 – November 2018: stream samples every 4 weeks; rain samples every 2 weeks
    - December 2018 onward: all samples every 4 weeks

- Data collection and structure
  - Collection methods: refer to Plynlimon_field_measurements_and_methods.csv
  - Sample sites: refer to Plynlimon_site_information.csv
  - Laboratory instrumentation: refer to Description_of_column_headings.csv

- Data contents and units
  - Nature and units of recorded values: refer to Description_of_column_headings.csv
  - Determinants and methods: described in Description_of_column_headings.csv, using CAST vocab where possible
  - Values below detection limit: reported as half the LOD
  - LOD values: provided in Description_of_column_headings.csv

- Data quality controls
  - pH, conductivity and alkalinity: measured at CEH Bangor laboratories; participation in LGC AquaCheck PT QA scheme
  - Other chemical analyses: at CEH Lancaster; UKAS-accredited to ISO 17025:2005
  - Data screening: checked for missing values; blanks indicate missing data (due to sample insufficiency, instrument/field issues)

- Data structure and provenance
  - Full dataset descriptions available in the described CSVs
  - Rainfall adjustments for consistency:
    - Carregwen rainfall chemistry (C) rainfall volumes come from Hafren (B) gauge near the adjacent sample site, not Carregwen gauge
    - Carregwen rainfall data started in September 2010

- GIS-focused considerations
  - Spatial mapping enabled via Plynlimon_site_information.csv (site coordinates)
  - Temporal analysis supported by regular sampling schedule
  - Handle missing data and non-detects appropriately in maps and time-series visualizations

- References to data sources
  - Plynlimon_site_information.csv
  - Plynlimon_field_measurements_and_methods.csv
  - Description_of_column_headings.csv

- Use case alignment for map-based products
  - Suitable for hydrochemical spatial visualization, temporal trend mapping, and integration with other GIS datasets due to standardized site and measurement metadata.