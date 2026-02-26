# Plynlimon Hydrochemical Data Description

## Overview
- Data period: March 2016 to March 2019.
- Sampling cadence:
  - March 2016 – July 2017: fortnightly.
  - August 2017 – November 2018: stream samples every four weeks; rain samples every two weeks.
  - December 2018 onwards: all samples every four weeks.
- Additional details available in Plynlimon_site_information.csv.
  
## Collection, Sites, and Methods
- Collection methods: described in Plynlimon_field_measurements_and_methods.csv.
- Sample sites: described in Plynlimon_site_information.csv.
- Laboratory instrumentation and analytical methods: described in Description_of_column_headings.csv.
- Nature and units of recorded values: described in Description_of_column_headings.csv.
- Data structure: described in Description_of_column_headings.csv.

## Data Processing and Quality
- Handling of non-detect values: hydrochemical values below the limit of detection (LOD) are reported as a value halfway between 0 and the LOD.
- LODs: provided in Description_of_column_headings.csv.
- Detailing of determinants and methods: provided in Description_of_column_headings.csv, using the CEH Analytical Services Thesaurus (CAST) where possible.
- Quality control and calibration:
  - pH, conductivity, and alkalinity analyzed at CEH Bangor laboratories.
  - CEH Bangor participates in the LGC AquaCheck Proficiency Testing scheme for QA against other laboratories.
  - Other chemical analyses performed at CEH Lancaster; facility UKAS-accredited to ISO 17025:2005 for many analyses.
- Data completeness and reliability:
  - Data checked for missing values; blank cells indicate missing data.
  - Missing data may result from insufficient sample (e.g., rain), instrument failure, or fieldworker error.

## Notes for Interpretation
- To maintain consistency with earlier Plynlimon hydrochemistry data, Carregwen rainfall (C) rainfall volumes are recorded from a rain gauge near the Hafren sample site (B) rather than the Carregwen Standard rain gauge site (AJ); Carregwen rainfall measurements started in September 2010.

## Governance, Metadata, and Stewardship Considerations
- Metadata sources and references:
  - Descriptions and methods are linked to multiple CSVs (site information, field methods, measurement descriptions) to support data provenance and reproducibility.
- Data discoverability and usability:
  - Clear documentation of sampling regime, sites, methods, units, and QC enhances reuse by data users and supports data governance.
- Data quality governance:
  - Documented QA/QC processes (UKAS ISO 17025 accreditation, proficiency testing) should be referenced in data catalogs.
  - Handling of non-detects and LODs should be consistently applied and described in metadata.
- Update and provenance:
  - Sampling cadence changes are time-stamped; ensure future datasets maintain explicit temporal metadata for traceability.
- Recommended steward actions:
  - Link data files to their corresponding metadata CSVs in catalogs.
  - Verify that LOD values and detection handling are clearly documented for end users.
  - Maintain notes about rainfall data provenance to prevent misinterpretation of measurements.