# Supporting documentation for Soil_Stable_Element.csv

## Overview
- Metadata-driven documentation for the Soil_Stable_Element.csv dataset.
- Provides explanations, units, and notes for each column, including detection-limit semantics and replicate information.
- Aims to support data governance, discovery, and reuse by ensuring consistent metadata and interpretation of measurements.

## Dataset structure and key fields

- Core sample metadata
  - Sample_Code: Unique sample identifier.
  - Sample_type: Type of sample.
  - Sample_Description: Further explanation of the sample; includes depth in centimetres (units: cm) and notes on replicates (RCN119, 120, 121 are replicate soil samples).
  - Collection_Date: Date of soil sample collection (format: dd month yyyy).

- Analytical measurements (concentrations on a dry mass basis, units mg/kg_dw)
  - I-127_mg_kg_dw
  - Li_mg_kg_dw
  - Be_mg_kg_dw
  - B_mg_kg_dw
  - Na_mg_kg_dw
  - Mg_mg_kg_dw
  - Al_mg_kg_dw
  - P_mg_kg_dw
  - S_mg_kg_dw
  - K_mg_kg_dw
  - Ca_mg_kg_dw
  - Ti_mg_kg_dw
  - V_mg_kg_dw
  - Cr_mg_kg_dw
  - Mn_mg_kg_dw
  - Fe_mg_kg_dw
  - Co_mg_kg_dw
  - Ni_mg_kg_dw
  - Cu_mg_kg_dw
  - Zn_mg_kg_dw
  - As_mg_kg_dw
  - Se_mg_kg_dw
  - Rb_mg_kg_dw
  - Sr_mg_kg_dw
  - Mo_mg_kg_dw
  - Ag_mg_kg_dw
  - Cd_mg_kg_dw
  - Cs_mg_kg_dw
  - Ba_mg_kg_dw
  - Tl_mg_kg_dw
  - Pb_mg_kg_dw
  - U_mg_kg_dw

- Detection limit fields (per-element, where applicable)
  - Detection_Limit_I-127_mg_kg_dw
  - Detection_Limit_Li_mg_kg_dw
  - Detection_Limit_Be_mg_kg_dw
  - Detection_Limit_B_mg_kg_dw
  - Detection_Limit_Na_mg_kg_dw
  - Detection_Limit_Mg_mg_kg_dw
  - Detection_Limit_Al_mg_kg_dw
  - Detection_Limit_P_mg_kg_dw
  - Detection_Limit_S_mg_kg_dw
  - Detection_Limit_K_mg_kg_dw
  - Detection_Limit_Ca_mg_kg_dw
  - Detection_Limit_Ti_mg_kg_dw
  - Detection_Limit_V_mg_kg_dw
  - Detection_Limit_Cr_mg_kg_dw
  - Detection_Limit_Mn_mg_kg_dw
  - Detection_Limit_Fe_mg_kg_dw
  - Detection_Limit_Co_mg_kg_dw
  - Detection_Limit_Ni_mg_kg_dw
  - Detection_Limit_Cu_mg_kg_dw
  - Detection_Limit_Zn_mg_kg_dw
  - Detection_Limit_As_mg_kg_dw
  - Detection_Limit_Se_mg_kg_dw
  - Detection_Limit_Rb_mg_kg_dw
  - Detection_Limit_Sr_mg_kg_dw
  - Detection_Limit_Mo_mg_kg_dw
  - Detection_Limit_Ag_mg_kg_dw
  - Detection_Limit_Cd_mg_kg_dw
  - Detection_Limit_Cs_mg_kg_dw
  - Detection_Limit_Ba_mg_kg_dw
  - Detection_Limit_Tl_mg_kg_dw
  - Detection_Limit_Pb_mg_kg_dw
  - Detection_Limit_U_mg_kg_dw

- Notes on interpretation and semantics
  - Many concentration columns have accompanying detection-limit columns to indicate non-detects.
  - In several cases, blanks in concentration fields imply concentration was below the detection limit; corresponding detection-limit fields define the actual threshold.
  - Some detection-limit columns include coded notes (e.g., 1 = detection limit, 2 = units, 3 = concentration detectable) to support downstream parsing and quality checks.
  - For certain elements, capitalization or formatting in the notes varies (e.g., “given sample” or “below the detection limit”), but the core concept is consistent: non-detects are typically represented via detection-limit metadata.

## Data conventions and units

- Concentrations are reported on a dry mass basis (mg/kg_dw) for most elements.
- Sample_Description depth is given in centimetres (cm).
- Collection_Date follows a standard dd month yyyy format.
- Replicate samples are explicitly noted (RCN119, 120, 121).

## Data governance and quality considerations for Data Stewards

- Metadata completeness and consistency
  - Ensure all measurement and detection-limit columns are properly documented and mapped.
  - Maintain clear provenance: sample codes, replicate identifiers, and collection dates.
- Handling non-detects
  - Use Detection_Limit columns to interpret blanks in concentration fields.
  - Align data ingestion pipelines to apply the same non-detect conventions across datasets.
- Units and standardization
  - Confirm mg/kg_dw as the standard unit for all elemental concentrations; verify consistency across related datasets.
  - Maintain depth information through Sample_Description as a standardized descriptor.
- Replicates and provenance
  - Respect replicate identifiers (RCN119, RCN120, RCN121) to enable replication analyses and uncertainty assessment.
- Interoperability and reuse
  - Preserve the meaning of detection-limit semantics when integrating with other systems; ensure downstream consumers understand how non-detects are represented.
- Documentation and updates
  - Keep metadata aligned with any data transformations or re-analyses; document any changes to column definitions or units.

## Practical implications for discovery and reuse

- Enables filtering by sample depth, collection date, and element concentrations.
- Supports accurate interpretation of non-detects via dedicated detection-limit metadata.
- Facilitates data quality auditing, reproducibility, and integration with broader soil chemistry datasets.