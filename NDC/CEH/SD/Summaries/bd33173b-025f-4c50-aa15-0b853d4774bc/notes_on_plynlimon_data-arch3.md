# Plynlimon hydrochemistry dataset (March 2023 – March 2024)

- Sampling regime and period
  - Data cover March 2023 to March 2024.
  - Samples collected every four weeks.

- Collection methods and references
  - Detailed collection methods, sample sites, instrumentation, units, and analytical methods are described in accompanying CSV files:
    - Plynlimon_field_measurements_and_methods.csv
    - Plynlimon_site_information.csv
    - Description_of_column_headings.csv
  - Full data structure details and determinants are provided in Description_of_column_headings.csv, with mappings to the CAST therau­sus.

- Sample sites and site information
  - Site-specific sampling locations and related metadata are available in Plynlimon_site_information.csv.

- Laboratory instrumentation and analytical approach
  - pH, conductivity, and alkalinity analyzed at UKCEH Bangor laboratories (Bangor).
  - Other chemical analyses performed at UKCEH Centralised Analytical Chemistry Group (Lancaster).
  - UKCEH Bangor participates in LGC AquaCheck Proficiency Testing; Lancaster lab is UKAS ISO 17025:2005 accredited for many analyses.

- Nature, units, and handling of recorded values
  - Hydrochemical values include notes for measurements below the limit of detection (LOD): values reported as halfway between 0 and the LOD.
  - LOD values may change over the sampling period, resulting in multiple rows for a single chemical with a period-specific LOD.
  - NPOC values and other measurements may be missing for certain sites/times as noted.

- Data quality control and calibration
  - Quality assurance procedures are described and data are checked for missing values; blanks may indicate sample omission due to insufficient sample, rain, instrument failure, or fieldworker error.
  - An example incident noted: a bottle broke before analysis (sample 76247, Upper Hafren, 05/12/2023).
  - Specific missing data: NPOC values missing for Lower Hore (76267) and Upper Hore (76270) on 04/03/02024 (likely a typographical error in date in the dataset narrative).

- Data integrity and interpretation notes
  - To maintain consistency with historical data, rainfall measurements associated with Carregwen rain chemistry are recorded from a Hafren near-site gauge rather than the Carregwen standard gauge (AJ).
  - When interpreting the data, refer to the linked CSVs for metadata, units, and methodological details; variables may require transformation due to occasional format or metadata limitations.

- Practical considerations for monitoring framework authors
  - The dataset exemplifies handling of data gaps, changing LODs, and the need for rigorous metadata to support data governance.
  - Data provenance and public sharing considerations are illustrated by references to data availability through multiple CSV files and the CAST thesaurus for methodological descriptions.
  - The documentation highlights potential barriers to reuse common in monitoring frameworks: incomplete metadata, data silos, and the need for consistent quality control across laboratories.