# Sampling regime

- Timeframe and sampling cadence
  - Data cover March 2023 to March 2024
  - Samples collected every four weeks

- Spatial scope and GIS relevance
  - Sampling sites documented in Plynlimon_site_information.csv
  - Data designed for integration into map-based visualisations; site locations are essential for GIS products

- Data collection methods and laboratory details
  - Collection methods described in Plynlimon_field_measurements_and_methods.csv
  - Laboratory instrumentation and measurement specifics align with Description_of_column_headings.csv
  - Analytical methods outlined in Description_of_column_headings.csv

- Data structure and metadata
  - Full determinant and method descriptions provided using CEH CAST vocabulary (see CAST link)
  - Detailed data structure definitions available in Description_of_column_headings.csv
  - Notes on reporting values and units embedded in the metadata files

- Handling of detected values and quality control
  - Values below the limit of detection (LOD) are reported as a value halfway between 0 and the LOD
  - Some chemicals have LOD changes over time, resulting in multiple rows with subperiod-specific LODs
  - pH, conductivity, and alkalinity measured at UKCEH Bangor; other chemical analyses at UKCEH Lancaster
  - UKCEH Bangor participates in LGC AquaCheck Proficiency Testing; Lancaster site operates under ISO 17025:2005 accreditation

- Data completeness and quality considerations
  - Missing values may occur due to insufficient sampling, instrument failure, or fieldworker error; some sample IDs are not included when no sample was collected
  - Example of data issue: bottle break at Upper Hafren on 05/12/2023 (sample 76247)
  - NPOC values missing for specific samples (Lower Hore 76267 and Upper Hore 76270 on 04/03/2024)

- Ancillary interpretation notes
  - Rainfall measurements for Carregwen rain chemistry (C) are recorded from a Hafren near-site gauge (B) rather than the Carregwen Standard gauge (AJ) to maintain consistency with earlier hydrochemistry data

- Data references and access
  - Refer to multiple CSVs for comprehensive details:
    - Plynlimon_site_information.csv
    - Plynlimon_field_measurements_and_methods.csv
    - Description_of_column_headings.csv
  - CAST vocabulary reference: https://vocabs.ceh.ac.uk/cast/en/