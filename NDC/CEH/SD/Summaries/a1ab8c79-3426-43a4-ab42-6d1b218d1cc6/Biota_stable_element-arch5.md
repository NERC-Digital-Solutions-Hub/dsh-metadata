# Supporting documentation for Biota_Stable_Element.csv

## Overview
- Defines the data dictionary for Biota_Stable_Element.csv.
- Describes fields for sample identification, classification, description, collection date, and a comprehensive set of elemental concentrations.
- For each element, includes the concentration on a fresh mass basis (units mg/kg_fw) and a corresponding detection limit field.
- Indicates that some samples (RCN119, RCN120, RCN121) are replicate soil samples.
- Includes a Notes column to document analyses or usage in estimating whole-organism concentration.

## Key Fields and Structure
- Sample_Code: Unique sample identifier.
- RAP: Sample type based on International Commission on Radiological Protection (ICRP) Reference Animals and Plants (RAPs).
- Sample_Description: Further explanation of the sample (with specified units where relevant, e.g., cm for size/length information in this context).
- Collection_Date: Date of soil sample collection (format: dd-mmm-yyyy).
- Element concentration fields (examples; all are on a fresh mass basis):
  - I-127_mg_kg_fw
  - Li_mg_kg_fw
  - Be_mg_kg_fw
  - B_mg_kg_fw
  - Na_mg_kg_fw
  - Mg_mg_kg_fw
  - Al_mg_kg_fw
  - P_mg_kg_fw
  - S_mg_kg_fw
  - K_mg_kg_fw
  - Ca_mg_kg_fw
  - Ti_mg_kg_fw
  - V_mg_kg_fw
  - Cr_mg_kg_fw
  - Mn_mg_kg_fw
  - Fe_mg_kg_fw
  - Co_mg_kg_fw
  - Ni_mg_kg_fw
  - Cu_mg_kg_fw
  - Zn_mg_kg_fw
  - As_mg_kg_fw
  - Se_mg_kg_fw
  - Rb_mg_kg_fw
  - Sr_mg_kg_fw
  - Mo_mg_kg_fw
  - Ag_mg_kg_fw
  - Cd_mg_kg_fw
  - Cs_mg_kg_fw
  - Ba_mg_kg_fw
  - Tl_mg_kg_fw
  - Pb_mg_kg_fw
  - U_mg_kg_fw
- Detection_Limit_<element>_mg_kg_fw (for each element): Detection limit on a fresh mass basis.
- Notes: Notes on analyses or how samples were used in estimating whole-organism concentration.
- Replicate samples: RCN119, RCN120, and RCN121 are identified as replicate soil samples.

## Data Quality and Standards
- Consistent units: All concentration values are in milligrams per kilogram on a fresh mass basis (mg/kg_fw).
- Detection limits: Each element includes a corresponding detection limit field to indicate measurement sensitivity per sample.
- Handling below-detection values: Documentation uses blanks to indicate below the detection limit, with explanatory notes guiding interpretation (and occasionally “detectable” indications in adjacent columns).
- Metadata completeness: Includes sample identity, classification, descriptive context, collection date, and detailed analytical metadata for each element.
- Replicate handling: Explicitly notes replicate soil samples, enabling assessment of measurement precision.

## Data Governance Considerations
- Provenance and classification: RAP field ties samples to ICRP RAP categories, supporting standardized classification and interoperability.
- Metadata completeness: Rich metadata supports discoverability and reuse across datasets and studies.
- Data interoperability: Uniform naming conventions for elemental concentrations and detection-limit fields facilitate integration with other datasets.
- Documentation of analyses: The Notes field provides context on analyses and estimation methods, supporting transparent data lineage.

## Practical Guidance for Data Stewards
- Validation checks:
  - Ensure all element concentration columns exist and are populated with mg/kg_fw values or appropriate blanks for non-detects.
  - Verify corresponding Detection_Limit_<element>_mg_kg_fw fields are present for each element.
  - Confirm Collection_Date follows the dd-mmm-yyyy format.
  - Confirm RAP values align with ICRP RAP classifications.
- Handling non-detects:
  - Interpret blank concentration values as below the detection limit, guided by the corresponding detection-limit field and Notes.
- Replicates:
  - Treat RCN119, RCN120, and RCN121 as replicate soil samples and document any variance or consolidation rules in accompanying metadata.
- Data sharing and discovery:
  - Preserve the full metadata, including detection limits and notes, to enable correct downstream analysis (e.g., exposure assessments, ecological risk evaluations).
  - Ensure consistent column naming and unit usage across datasets to support interoperability and reuse.