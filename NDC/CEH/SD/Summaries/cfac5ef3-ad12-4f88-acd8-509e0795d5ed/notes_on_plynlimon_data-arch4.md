# Plynlimon hydrochemistry data description and methods

## Overview
- Data cover March 2019 to March 2023, with sampling every four weeks.
- Additional details and structure are provided in related CSV files (e.g., site information, methods, and column descriptions).

## Data collection and scope
- Sampling regime: 2019-03 to 2023-03, four-week cadence.
- Collection methods: documented in Plynlimon_field_measurements_and_methods.csv.
- Sample sites: documented in Plynlimon_site_information.csv.
- Laboratory instrumentation, nature and units of recorded values, and analytical methods: described in Description_of_column_headings.csv.

## Data structure and reporting
- Full data structure details available in Description_of_column_headings.csv.
- Reported value handling:
  - Values below the limit of detection (LOD) are recorded as halfway between 0 and the LOD.
  - LOD values can change over time for certain chemicals, leading to multiple rows per chemical per subperiod with the specific LOD.
- Determinants and methods descriptions align with CEH Analytical Services Thesaurus (CAST) where possible: https://vocabs.ceh.ac.uk/cast/en/

## Quality control and calibration
- pH, conductivity, and alkalinity measured at CEH Bangor laboratories; these labs participate in the LGC AquaCheck Proficiency Testing scheme.
- Other chemical analyses conducted at CEH Lancaster Centre; UKAS-accredited to ISO 17025:2005 for many analyses.
- Data checks: missing values may appear as blank cells due to sample insufficiency, instrument failure, or fieldwork error; some periods had restricted access (e.g., Covid-19 lockdown in 2020).

## Data cleaning
- Fixed inconsistent quoting for SO4-S (SO4 vs SO4-S).
- Removed obvious gross errors in several variables, notably chlorine (Cl).
- Fixed inconsistent bromide units (mg/L vs µg/L).
- Corrected swapped pH values for the Afon Cyff/Gwy dataset (issue since Aug 2022).

## Additional interpretation notes
- Rainfall data alignment: Carregwen rain chemistry rainfall measurements are recorded from a Hafren near the B site rather than the Carregwen standard rain gauge, for consistency with prior hydrochemistry data.

## Implications and considerations for Data Leaders
- System-wide perspective: data spans multiple sources and metadata files; requires careful integration and governance.
- User needs and accessibility: understanding data availability, gaps, and varying LODs; need for clear metadata and documentation to support reuse.
- Data quality and standards: reliance on CAST terminology and ISO/17025 accreditation; ongoing QA and calibration processes.
- Data stewardship: clear versioning, updates, and cross-referencing among related datasets (sites, methods, and column descriptions) to maintain discoverability and usability.
- Collaboration potential: opportunities to coordinate with wider data communities to improve consistency, standards, and data-sharing practices across related datasets.