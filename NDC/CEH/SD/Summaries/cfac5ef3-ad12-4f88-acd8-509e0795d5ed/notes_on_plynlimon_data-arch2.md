# Plynlimon hydrochemistry data description

## Overview
- Time period: March 2019 to March 2023.
- Sampling cadence: every four weeks.
- Data are part of a structured hydrochemistry dataset with multiple supporting CSV files that describe sites, methods, instruments, and data fields.

## Data collection regime
- Frequent, regular sampling over four-year period to monitor hydrochemical conditions.
- Sampling scope and specifics are documented across related CSV files (site information, field measurements, and column descriptions).

## Collection methods and data structure
- Collection methods: described in Plynlimon_field_measurements_and_methods.csv.
- Sample sites: described in Plynlimon_site_information.csv.
- Laboratory instrumentation and measurement details: described in Description_of_column_headings.csv.
- Nature, units, and analytical methods: described in Description_of_column_headings.csv.
- Data structure: described in Description_of_column_headings.csv, including determinants and method metadata (CAST thesaurus where possible).

## Quality control and calibration
- pH, conductivity, and alkalinity analyzed at CEH Bangor laboratories with quality assurance via the LGC AquaCheck Proficiency Testing scheme.
- Other chemical analyses performed at CEH Centralised Analytical Chemistry Group (Lancaster); UKAS-accredited to ISO 17025:2005 for many analyses.
- Missing values possible due to sampling gaps, instrument issues, or field errors; some sample IDs excluded when sampling was restricted (e.g., COVID-19 pandemic in 2020).

## Data cleaning and processing
- Corrected inconsistent quoting for sulfate (SO4-S versus SO4-S).
- Removed obvious gross errors (notably in chloride, Cl).
- Standardized units for bromide (mg/L vs μg/L).
- Corrected pH anomalies for Afon Cyff/Gwy due to a historical swap (since Aug 2022).

## Notes on interpretation and data context
- For values below the limit of detection (LOD), reported as halfway between 0 and LOD.
- Some chemicals have multiple LODs over the sampling period; these are captured by multiple rows with period-specific LOD values.
- Determinants and methods described with CEH Analytical Services Thesaurus (CAST) terminology where possible.

## Additional information useful for interpretation
- Rainfall data alignment: Carregwen rain chemistry rainfall volumes are recorded from the Hafren (B) site gauge rather than the Carregwen Standard gauge (AJ) to maintain consistency with published hydrochemistry data.

## How this aligns with Analysts Monitoring the Environment
- What analysts do:
  - Understand and verify data from established sources; perform quality assurance and cleaning.
  - Transform data into standardized formats suitable for environmental health assessment.
  - Analyze using standardised methods to classify environmental health against standards.
  - Present outputs via clear formats (reports, maps, charts) and store/upload datasets to appropriate portals.
- Key outputs supported by this dataset:
  - Cleaned, QA’d hydrochemical time series suitable for trend analysis and policy performance evaluation.
  - Clear documentation of data structure, methods, and QA processes to enable replication and integration with other datasets.

## Particular challenges and opportunities for Analysts
- Challenge: increasing the value of the hydrochemical datasets by combining with other relevant data sources (avoiding single-use data).
- Challenge: enabling broad access to the underlying data used to create final outputs (data transparency and reuse).