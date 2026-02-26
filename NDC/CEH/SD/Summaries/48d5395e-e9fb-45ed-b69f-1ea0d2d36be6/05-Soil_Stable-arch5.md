# Supporting documentation for 05-Soil_Stable.csv

## Overview
- Contains soil stable element concentrations for samples in 05-Soil_Stable.csv.
- Key metadata: Sample_Code (unique), Sample_Type (Soil), Location, Sample_Description, Collection_Date, Sample_size_g_dm.
- For each element (e.g., Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th, etc.): a concentration in mg/kg_dm, with associated Unc_<element>_mg/kg_dm and Detection_Limit_<element>_mg/kg_dm.
- Measurements are on a dry matter basis (mg per kg dry mass). Sample descriptions may specify depth (e.g., soil collected at depth 0-10 cm).

## Data Model and Fields
- Core identifiers and metadata
  - Sample_Code: unique sample identifier.
  - Sample_Type: fixed value "Soil".
  - Location: name of where the sample was collected.
  - Sample_Description: additional details about the sample (e.g., depth or conditions).
  - Collection_Date: date of collection (format dd-mm-yyyy).
  - Sample_size_g_dm: amount of sample analyzed (g dry matter).

- Analyte data (per element)
  - Element_mg/kg_dm: concentration on a dry matter basis (e.g., Cs_mg/kg_dm, Sr_mg/kg_dm, K_mg/kg_dm, Na_mg/kg_dm, Ca_mg/kg_dm, Mg_mg/kg_dm, P_mg/kg_dm, Pb_mg/kg_dm, U_mg/kg_dm, Th_mg/kg_dm, etc.).
  - Unc_Element_mg/kg_dm: combined uncertainty for the element concentration.
  - Detection_Limit_Element_mg/kg_dm: detection limit for the element on a dry matter basis.
  - Notes: blanks typically indicate the concentration was below the detection limit.

- Formatting notes
  - Several fields use phrasing like “on a dry matter basis” or “dry mass basis.”
  - Some entries show minor formatting inconsistencies (e.g., Ca_mg/kg_dm, on a dry matter basis = ...), which should be harmonized during data curation.

## Measurement Characteristics
- Units: mg/kg_dm (mg per kg dry mass) for all analyte concentrations.
- Depth or description: sample descriptions may indicate depth (e.g., 0-10 cm).
- Uncertainty: each concentration has a corresponding combined uncertainty value.
- Detection limits: provided for each analyte; if the concentration is blank, it indicates the concentration is below the detection limit.

## Quality, Uncertainty, and Detection Limits
- Each analyte concentration is accompanied by a corresponding Unc_<element>_mg/kg_dm.
- Detection_Limit_<element>_mg/kg_dm indicates the assay’s detection threshold.
- Blank values signal concentrations below the detection limit; these should be treated accordingly in analyses (e.g., censored data handling).

## Provenance, Collection, and Sample Metadata
- Collection_Date is recorded and formatted as dd-mm-yyyy.
- Location and Sample_Description provide contextual metadata for traceability.
- Sample_size_g_dm captures the amount of soil used for analysis (dry matter basis).

## Data Governance and Sharing Considerations
- Metadata should be complete and standardized to enable discoverability and reuse.
- Harmonize field naming and units across datasets to improve interoperability.
- Maintain data lineage by documenting collection methods, analytical methods, detection limits, and uncertainty calculations.
- Ensure appropriate data sharing practices, including any embargoes or proprietary restrictions, are applied (note: the provided document does not specify embargoes; governance practice should still account for potential restrictions).

## Data Quality Challenges and Recommendations
- Challenges
  - Incomplete or inconsistent user needs for metadata and data products.
  - Timely receipt of data from multiple creators.
  - Variability in systems/formats and non-interoperable legacy data.
  - Large datasets with many analytes and fields.
  - Outdated or heterogeneous databases requiring bespoke handling.
- Recommendations for Data Stewards
  - Enforce a standardized data dictionary and uniform field names.
  - Harmonize units and ensure consistent representation of “dry matter basis.”
  - Validate presence of core metadata (Sample_Code, Location, Collection_Date, Sample_Description, Sample_size_g_dm).
  - Ensure uncertainty and detection-limit fields exist for all analytes; flag missing or inconsistent values.
  - Implement data validation rules to catch formatting inconsistencies and rectify irregularities.
  - Document data provenance and methods to support reproducibility and discovery.

## Use and Interpretation Notes
- Concentrations are reported as mg/kg_dm; blank values imply concentrations below the detection limit.
- Interpret detection limits and uncertainties in downstream analyses; treat below-detection values with appropriate statistical methods.
- Be aware of potential depth-related context from Sample_Description when combining data from multiple depths.