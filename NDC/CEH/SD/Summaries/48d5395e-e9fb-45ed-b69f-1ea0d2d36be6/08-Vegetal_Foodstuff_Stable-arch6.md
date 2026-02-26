# Supporting documentation for 08-Vegetal_Foodstuff_Stable.csv

## Purpose and scope
- Provides metadata definitions and data quality guidance for the Vegetal_Foodstuff_Stable.csv dataset.
- Clarifies what each column represents, including units, descriptions, and how to interpret missing or threshold values.
- Aids data verification, cleaning, transformation, and the creation of user-friendly data products (e.g., dashboards, reports).

## Key data components

- Sample metadata
  - Sample_Code: Unique sample identifier.
  - Sample_Type: General description of the sample (e.g., foodstuff group).
  - Location: Location where the sample was collected.
  - Sample_Description: Part of the organism analyzed (e.g., tissue or organ).
  - Collection_Date: Date of sample collection (format: dd-mm-yyyy).
  - Sample_size: Amount of sample analyzed (units vary; e.g., g fresh matter or mL for olive oil and wine).

- Analyte concentrations and related fields
  - Cs_mg/kg_dm, Sr_mg/kg_dm, K_mg/kg_dm, Na_mg/kg_dm, Ca_mg/kg_dm, Mg_mg/kg_dm, P_mg/kg_dm, Pb_mg/kg_dm, U_mg/kg_dm, Th_mg/kg_dm: Concentration of stable elements on a dry mass basis (or per litre for olive oil and wine in some cases).
  - Unc_<analyte> (e.g., Unc_Cs_mg/kg_dm): Combined uncertainty of the analyte concentration on a dry mass basis.
  - Detection_Limit_<analyte> (e.g., Detection_Limit_Cs_mg/kg_dm): Detection limit for the analyte on a dry mass basis (note: some fields specify units as mg per kg dry mass or mg per litre for olive oil and wine).
  - Notes: Indicate when a concentration is below the detection limit (blank in the concentration field implies below detection limit).

- Units and variability
  - Common unit: mg per kg dry mass (dm) for most analytes.
  - For some matrices (e.g., olive oil and wine), certain fields reference mg per litre.
  - Several fields include explicit unit descriptions and, in some cases, enumerated qualifiers (e.g., 1, 2, 3) to denote alternatives or formats.

## Data quality and interpretation

- Missing values in concentration fields typically indicate concentrations below the stated detection limit.
- The document provides explicit guidance on units, uncertainties, and detection limits to support consistent data interpretation across analyses.
- Some formatting inconsistencies are present in the text (e.g., redundant or variably structured entries for Detection_Limit fields), which may require careful parsing during data ingestion.

## How this supports data use for the Data Support archetype

- Enables thorough understanding of what each column means, facilitating accurate data cleaning, transformation, and integration with other datasets.
- Supports creation of self-serve data products by clearly defining how to compute and display concentrations, uncertainties, and detection-limit handling.
- Aids communication of data provenance and quality to end users, helping promote data outputs and reuse across projects (policy work, dashboards, reports).
- Provides a framework to verify data consistency (dates, sample descriptions, units) and to address common challenges such as patchy data formats and cross-matrix comparisons.