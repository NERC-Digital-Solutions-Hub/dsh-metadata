# Supporting documentation for 10-Animal_Foodstuff_Stable.csv

## Overview
- This is supporting documentation (a data dictionary) for the dataset 10-Animal_Foodstuff_Stable.csv.
- It documents metadata fields and per-element measurement fields for concentrations of several stable elements in animal-derived foodstuffs.
- Key metadata includes sample identifiers, location, collection date, sample description, and the portion of the organism analysed.
- Per-element data include concentration, combined uncertainty, and detection limit values, with specific units and notes on how to interpret missing data.

## Data structure and fields

- Sample metadata
  - Sample_Code: Unique sample identifier.
  - Sample_Type: General description of the sample (foodstuff group).
  - Location: Name of the collection location.
  - Collection_Date: Date of sample collection (format: dd-mm-yyyy).
  - Sample_size: Amount of sample analyzed (units: g fresh matter or mL for milk).
  - Sample_Description: Part of the organism analysed (e.g., tissue or organ portion).

- Measurement fields (per element)
  - Cs (cesium)
    - Cs_mg/kg_fm: Concentration on a fresh mass basis.
    - Unc_Cs_mg/kg_fm: Combined uncertainty on a fresh mass basis.
    - Detection_Limit_Cs_mg/kg_fm: Detection limit on a fresh mass basis.
  - Sr (strontium)
    - Sr_mg/kg_fm, Unc_Sr_mg/kg_fm, Detection_Limit_Sr_mg/kg_fm
  - K (potassium)
    - K_mg/kg_fm, Unc_K_Mg/kg_fm, Detection_Limit_K_mg/kg_fm
  - Na (sodium)
    - Na_mg/kg_fm, 1; Na_mg/kg_fm, 2; Na_mg/kg_fm, 3 (description indicates multiple subfields describing Na concentration, units, and detection-limit relation)
    - Unc_Na_mg/kg_fm, 1; Unc_Na_mg/kg_fm, 2; Unc_Na_mg/kg_fm, 3
    - Detection_Limit_Na_mg/kg_fm, 1; Detection_Limit_Na_mg/kg_fm, 2; Detection_Limit_Na_mg/kg_fm, 3
  - Ca (calcium)
    - Ca_mg/kg_fm; Unc_Ca_Mg/kg_fm; Detection_Limit_Ca_mg/kg_fm
  - Mg (magnesium)
    - Mg_mg/kg_fm, 1; Unc_Mg_mg/kg_fm, 1
    - Mg_mg/kg_fm, 2; Unc_Mg_mg/kg_fm, 2
    - Detection_Limit_Mg_mg/kg_fm (note: some naming variations such as Mg_mg/ kg_fm, 1)
  - P (phosphorus)
    - P_mg/kg_fm; Unc_P_mg/kg_fm; Detection_Limit_P_mg/kg_fm
  - Pb (lead)
    - Pb_mg/kg_fm; Unc_Pb_mg/kg_fm; Detection_Limit_Pb_mg/kg_fm
  - U (uranium)
    - U_mg/kg_fm; Unc_U_mg/kg_fm; Detection_Limit_U_mg/kg_fm
  - Th (thorium)
    - Th_mg/kg_fm; Unc_Th_mg/kg_fm; Detection_Limit_Th_mg/kg_fm

- Notes on field structure
  - Some elements (notably Na and Mg) appear with indexed subfields (e.g., 1, 2, 3) describing different aspects of the same measurement (concentration, unit representation, and detection-limit interpretation).
  - The dataset uses a mix of field label variants (e.g., Unc_K_Mg/kg_fm vs Unc_K_mg/kg_fm; Mg_mg/kg_fm vs Mg_mg/kg_fm) which may reflect formatting inconsistencies.
  - For many fields, a blank value indicates the measurement was below the detection limit.

## Units and data interpretation

- Concentrations are reported on a fresh mass basis (fm) for solid samples and as mg per litre for milk where applicable.
- Units used in field labels include:
  - mg/kg_fm (mg per kg fresh mass) for most elements
  - mg/L for milk in applicable fields
- Detection limits are provided per element; blank detection limit fields indicate “not detected” or below detection limit.
- “Where blank, then concentration was below the detection limit” guidance appears for several elements.
- Collection_date uses the format dd-mm-yyyy; sample_size specifies whether the mass is in grams (fresh matter) or milliliters (milk).

## Data governance and sharing considerations for Data Stewards

- Metadata completeness: Ensure all sample metadata fields (Sample_Code, Location, Collection_Date, Sample_size, Sample_Type, Sample_Description) are populated for discoverability.
- Standardization: Align field names and units across elements to support interoperability (resolve inconsistent capitalisation and suffixes such as Unc_K_Mg/kg_fm vs Unc_K_mg/kg_fm).
- Documentation of methods: Capture the analytical methods used to determine concentrations, uncertainties, and detection limits to enable reproducibility.
- Handling below-detection-limit data: Establish a consistent policy for representing non-detects (e.g., using blanks in concentration fields and clearly documented handling in data release notes).
- Data update and provenance: Implement clear update workflows and versioning, and document any changes to field definitions or measurement protocols.
- Portal and catalogue integration: Ensure dataset can be uploaded to portals and catalogues with consistent metadata to support discovery and reuse.

## Challenges and considerations for Data Stewards

- Incomplete or ambiguous user needs: The dataset’s wide range of elements and detailed per-field metadata may require user guidance to identify relevant fields.
- Data timing and delivery: Timely access to data from creators may be challenging, especially given large numbers of elements and subfields.
- Metadata quality and consistency: Variability in field naming and unit representation could hinder interoperability and automated validation.
- Format and interoperability: Mixed field naming conventions and index-based subfields may complicate data ingestion into standardized pipelines.

## Practical use and curation guidance

- Validate consistency of units and naming across all element fields.
- Produce a standardized data dictionary with uniform field names and definitions.
- Include a methods section documenting analytical techniques, calibration, and uncertainty estimation.
- Provide guidance for end users on interpreting below-detection-limit values and missing data.
- Ensure clear versioning and change logs when updating the dataset or metadata.

## Recommendations for data standardization

- Unify field naming conventions (e.g., consistent use of mg/kg_fm for all concentrations, consistent Unc_ prefixes, and removal of ambiguous mixed-case variants).
- Harmonize detection-limit fields so each element has a single, clearly named Detection_Limit element.
- Consolidate Na and Mg into standard, single-field structures or clearly documented subfields with consistent semantics.
- Enforce controlled vocabularies for Sample_Type and Location where possible.
- Provide a separate, machine-readable metadata file (e.g., JSON or YAML) that mirrors the data dictionary to support automated validation and discovery.