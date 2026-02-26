# Plynlimon hydrochemical data documentation

- Time period
  - Data cover March 2016 to March 2019.

- Sampling regime
  - Fortnightly sampling: March 2016 – July 2017 (streams) and rain samples.
  - August 2017 – November 2018: stream samples every 4 weeks; rain samples every 2 weeks.
  - December 2018 onward: all samples every 4 weeks.

- Collection methods and site details
  - Details available in:
    - Plynlimon_field_measurements_and_methods.csv
    - Plynlimon_site_information.csv
    - Description_of_column_headings.csv (for laboratory instrumentation and measurement details)

- Nature and units of recorded values
  - Defined in Description_of_column_headings.csv (including determinant names, units, and measurement methods)

- Analytical methods and data structure
  - Analytical methods and data structure described in Description_of_column_headings.csv.
  - Where possible, CAST (CEH Analytical Services Thesaurus) terms used for consistency (http://vocabs.ceh.ac.uk/evn/tbl/cast.evn).

- Reporting and limits of detection
  - Values below the limit of detection (LOD) are recorded as half the LOD.
  - LOD values listed in Description_of_column_headings.csv.

- Quality control and laboratory accreditation
  - pH, conductivity, and alkalinity analyzed at CEH Bangor laboratories.
  - CEH Bangor participates in the LGC AquaCheck Proficiency Testing scheme.
  - Other chemical analyses conducted at CEH Centralised Analytical Chemistry Group (Lancaster).
  - UKAS-accredited to ISO 17025:2005 for many analyses.

- Data quality and completeness
  - Data checked for missing values; blank cells indicate missing data.
  - Missing data may result from insufficient sample, instrument failure, or fieldwork errors.

- Interpretation notes for end users
  - Rainfall data for Carregwen chemistry (C) is recorded from a rain gauge near Hafren (B) rather than Carregwen gauge (AJ); Carregwen rainfall measurements started in September 2010 to align with prior datasets.

- Practical guidance for data usage (Data Support perspective)
  - Expect variable sampling frequencies across periods; plan analyses accordingly.
  - Be mindful of LOD handling (half-LOD values) and ensure consistent interpretation across datasets.
  - Utilize the accompanying metadata files (site, methods, instrumentation, and column headings) to understand determinants, units, and measurement contexts.
  - Consider data gaps and potential quality flags when aggregating or comparing across sites or time periods.
  - When sharing outputs or creating dashboards, reference the CAST terminology and ISO 17025-aligned QA practices to maintain traceability and comparability with other datasets.