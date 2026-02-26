# Supporting documentation for 12-Feedstuff_Stable.csv

## Overview
- Documents the structure and field definitions for the 12-Feedstuff_Stable.csv dataset.
- Includes sample metadata (identifier, type, location, description, collection date, sample size) and chemical concentration data for multiple elements.
- Provides accompanying uncertainty (Unc_*) and detection limit (Detection_Limit_*) fields for each analyte.
- Indicates that blank values denote concentrations below the detection limit.
- Uses dry-mass basis for concentration units (mg per kg dry mass) and dd-mm-yyyy for collection dates; sample size is in g fresh matter.
- Annotations reflect that the table contains fields for Cs, Sr, K, Na, Ca, Mg, P, Pb, U, and Th, each with concentration, uncertainty, and detection-limit information, with some formatting inconsistencies in the source text.

## Dataset structure and key fields
- Sample metadata
  - Sample_Code: unique sample identifier
  - Sample_Type: general description of sample (e.g., foodstuff group)
  - Location: location where the sample was collected
  - Sample_Description: part of the organism analyzed
  - Collection_Date: date of sample collection (dd-mm-yyyy)
  - Sample_size: amount analyzed (units: g fresh matter)
- Analyte measurements (all on dry mass basis)
  - Cs_mg/kg_dm, Unc_Cs_mg/kg_dm, Detection_Limit_Cs_mg/kg_dm
  - Sr_mg/kg_dm, Unc_Sr_mg/kg_dm, Detection_Limit_Sr_mg/kg_dm
  - K_mg/kg_dm, Unc_K_Mg/kg_dm, Detection_Limit_K_mg/kg_dm
  - Na_mg/kg_dm, Unc_Na_mg/kg_dm, Detection_Limit_Na_mg/kg_dm
  - Ca_mg/kg_dm, Unc_Ca_Mg/kg_dm, Detection_Limit_Ca_mg/kg_dm
  - Mg_mg/kg_dm, Unc_Mg_mg/kg_dm, Detection_Limit_Mg_mg/kg_dm
  - P_mg/kg_dm, Unc_P_mg/kg_dm, Detection_Limit_P_mg/kg_dm
  - Pb_mg/kg_dm, Unc_Pb_mg/kg_dm, Detection_Limit_Pb_mg/kg_dm
  - U_mg/kg_dm, Unc_U_mg/kg_dm, Detection_Limit_U_mg/kg_dm
  - Th_mg/kg_dm, Unc_Th_mg/kg_dm, Detection_Limit_Th_mg/kg_dm
- Notes on field values
  - Blanks indicate concentrations below the detection limit for that analyte.

## Data quality and governance implications for Data Stewards
- Ensuring consistency: enforce uniform field names, units, and meaning across the dataset to support discovery and reuse.
- Metadata completeness: verify that sample metadata (identifier, type, location, collection date, description, and sample size) are present and correctly formatted.
- Measurement metadata: maintain explicit Unc_* and Detection_Limit_* fields for all analytes to support traceability and uncertainty assessment.
- Unit and basis standardization: confirm that all concentration values are on dry-mass basis (mg/kg_dm) and dates use the requested format.
- Handling below-detection values: adopt the documented approach where blank indicates below detection limit, and ensure consistent interpretation during analysis and sharing.
- Provenance and transformations: document any data cleaning or transformations applied to raw data before sharing.
- Ingestion and sharing: plan for portal upload and cataloguing, including versioning and updates to reflect new measurements or corrected metadata.

## Practical considerations for ingestion and sharing
- Validate that all analyte fields are present or appropriately marked as below detection, with corresponding Unc_ and Detection_Limit_ values where applicable.
- Address formatting inconsistencies noted in the source (e.g., bracketed capitalization differences like Unc_K_Mg/kg_dm vs Unc_K_mg/kg_dm) to ensure schema alignment.
- Prepare complete field definitions and data dictionaries to accompany the dataset during publication.
- Establish guidance for data creators on meeting metadata requirements, including precise field semantics and units.

## Potential data quality issues noted
- Formatting inconsistencies and typos in field names (e.g., Unc_K_Mg/kg_dm, Unc_Na_mg/kg_dm, and uneven capitalization).
- Some entries show multiple subfields (e.g., 1 = ..., 2 = ..., 3 = ...) which may require explicit mapping to the schema.
- Some notes appear truncated or incomplete (e.g., Na_mg/kg_dm notes), indicating a need for clean, consistent field documentation.