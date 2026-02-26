# Plynlimon hydrochemistry data documentation

- Timeframe and sampling cadence
  - Data cover March 2019 to March 2023.
  - Samples collected every four weeks.

- Collection methods and site information
  - Collection methods and data lineage described in Plynlimon_field_measurements_and_methods.csv.
  - Sample sites described in Plynlimon_site_information.csv.
  - Full data structure and field descriptions are provided in Description_of_column_headings.csv.

- Laboratory instrumentation and analytical methods
  - pH, conductivity, and alkalinity measured at CEH Bangor laboratories.
  - Other chemical analyses performed at CEH Lancaster (Centralised Analytical Chemistry Group).
  - QA: CEH Bangor participates in the LGC AquaCheck Proficiency Testing; CEH Lancaster is UKAS-accredited to ISO 17025:2005 for many analyses.

- Data quality, completeness, and access
  - Data checked for missing values (gaps may arise from insufficient samples, instrument failure, or field errors). Some sample IDs are excluded when sampling was restricted (e.g., 2020 Covid-related restrictions).
  - Access to Carregwen rain chemistry is aligned with Hafren site rainfall measurements for consistency with prior data; Carregwen C rainfall uses the Hafren B gauge rather than its own AJ gauge.

- Data cleaning and standardisation
  - Fixed inconsistent quoting of SO4-S (SO4 vs SO4-S).
  - Removed obvious gross errors in several variables, particularly Cl.
  - Fixed inconsistent bromide units (mg/L vs µg/L).
  - Corrected swapped pH values for Afon Cyff/Gwy since August 2022.

- Reporting conventions and LOD handling
  - Values below the limit of detection (LOD) are reported as halfway between 0 and the LOD.
  - Some chemicals have changing LODs over the study period, resulting in multiple rows with a LOD specific to each subperiod.
  - Detailed determinant methods and vocabulary are provided via Description_of_column_headings.csv and the CAST (CEH Analytical Services Thesaurus) vocabulary online.

- Interpretation and usage notes
  - The dataset supports consistent interpretation by cross-referencing the CSVs for metadata, methods, and column definitions.
  - For data products, refer to the metadata and data-cleaning notes to understand formatting, units, and detection limits.

- Practical notes for data users
  - Use the linked CSVs to understand data structure, site context, and measurement methods.
  - Be mindful of LOD-specific rows when analyzing low-concentration constituents.
  - Consider potential past data adjustments (pre- vs. post-August 2022 pH correction) when performing longitudinal analyses.