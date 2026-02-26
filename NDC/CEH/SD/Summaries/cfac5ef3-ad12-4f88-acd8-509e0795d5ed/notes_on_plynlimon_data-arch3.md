# Plynlimon hydrochemical data description (March 2019 – March 2023)

## Overview
- Data cover March 2019 to March 2023 with sampling every four weeks.

## Data sources and related files
- Site information: Plynlimon_site_information.csv
- Collection methods: Plynlimon_field_measurements_and_methods.csv
- Laboratory instrumentation, units, and analytical methods: Description_of_column_headings.csv
- Full data structure and determinants/methods described in Description_of_column_headings.csv (also aligned with CAST vocabulary)

## Data coverage and structure
- Sampling regime and period are detailed; data structure and recording units are described in the accompanying CSVs.
- Notes on reported values indicate how values below the limit of detection (LOD) are represented and how LODs may vary over subperiods, resulting in multiple rows for some chemicals.

## Quality control and laboratory procedures
- pH, conductivity, and alkalinity measured at CEH Bangor laboratories.
- CEH Bangor participates in the LGC AquaCheck Proficiency Testing QA scheme.
- Other chemical analyses conducted at CEH Lancaster Centralised Analytical Chemistry Group; UKAS accreditation to ISO 17025:2005 for many analyses.
- Data checks recorded as gaps (blanks) due to missing samples, instrument failure, or fieldworker error; some sampling was restricted during 2020 due to Covid.

## Data cleaning and corrections
- Corrected inconsistent quoting of SO4-S (SO4 vs SO4-S).
- Removed obvious gross errors in various variables, notably chlorine (Cl).
- Standardized bromide units (mg/L vs µg/L).
- Resolved swapped pH values for Afon Cyff/Gwy since August 2022.

## Interpretation and contextual notes
- For consistency with previously published Plynlimon hydrochemistry data, rainfall measurements for Carregwen rain chemistry are recorded from the Hafren rain gauge (near the Hafren sample site) rather than the Carregwen Standard gauge AJ.

## Metadata and references
- Descriptions of determinants and methods are provided in Description_of_column_headings.csv, using CAST vocabulary where possible.
- Data structure, site details, and measurement methods are linked across multiple CSV files as noted above.