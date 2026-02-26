# Sampling regime

- Timeframe and cadence:
  - Data cover March 2023 to March 2024, with samples collected every four weeks.
  - Details available in Plynlimon_site_information.csv.

- Collection methods and sites:
  - See Plynlimon_field_measurements_and_methods.csv for collection methods.
  - Sample sites information in Plynlimon_site_information.csv.

- Laboratory instrumentation and measurements:
  - Refer to Description_of_column_headings.csv for specifics on instrumentation, units, and recorded values (hydrochemical measurements, other chemistry, etc.).

- Data structure and metadata:
  - Description_of_column_headings.csv provides full structure, determinants, and methods.
  - Where possible, CAST (CEH Analytical Services Thesaurus) terms used (https://vocabs.ceh.ac.uk/cast/en/).

- Value interpretation and handling of limits:
  - Values below the limit of detection (LOD) are reported as halfway between 0 and the LOD.
  - LOD values may change over the sampling period, resulting in multiple rows per chemical with a period-specific LOD.
  - NPOC values and other determinants are described within the same metadata framework.

- Quality control and laboratory standards:
  - pH, conductivity, and alkalinity measured at UKCEH Bangor laboratories; Bangor participates in the LGC AquaCheck Proficiency Testing scheme.
  - Other chemical analyses conducted at UKCEH Centralised Analytical Chemistry Group (Lancaster); ISO 17025:2005 UKAS accreditation for many analyses.
  - Data checked for missing values; blanks may reflect insufficient sample, instrument failure, or fieldworker error; some samples not included if no sample was collected.

- Data integrity incidents and gaps:
  - Example: a glass bottle broke before analysis (Upper Hafren sample 05/12/2023; sample 76247).
  - NPOC values missing for Lower Hore (76267) and Upper Hore (76270) on 04/03/2024.
  - Some records may have incomplete or missing data due to sampling or analysis issues.

- Documentation and interpretation aids:
  - To maintain consistency with previous hydrochemistry datasets, rainfall measurements associated with Carregwen rain chemistry (C) are recorded from a Hafren (B) rain gauge near the Hafren sample site, not the Carregwen Standard gauge AJ.

- Governance, sharing, and updates:
  - Data are accompanied by metadata and method documentation (via multiple CSVs) to enable discovery, reuse, and proper interpretation.
  - As a steward, ensure metadata completeness, maintain consistent LOD handling across subperiods, and track any data quality issues or changes in analytical methods.
  - Facilitate updates and ensure alignment with data availability and sharing policies across portals and catalogues.