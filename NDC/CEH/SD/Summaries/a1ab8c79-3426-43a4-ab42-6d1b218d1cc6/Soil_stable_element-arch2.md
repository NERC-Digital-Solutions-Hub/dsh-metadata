# Supporting documentation for Soil_Stable_Element.csv

- Purpose and scope
  - Provides the data dictionary and explanations for the Soil_Stable_Element.csv dataset used in environmental monitoring.
  - Enables consistent reporting of soil elemental concentrations to assess environmental health and policy performance over time.

- Key data categories
  - Sample metadata
    - Sample_Code: unique sample identifier.
    - Sample_type: type of sample.
    - Sample_Description: further explanation of the sample (note: units listed as cm for descriptions; RCN119, 120, 121 are replicate samples).
    - Collection_Date: date of collection (format: dd month yyyy).
  - Elemental concentrations (all on a dry mass basis)
    - I-127_mg_kg_dw, Li_mg_kg_dw, Be_mg_kg_dw, B_mg_kg_dw, Na_mg_kg_dw, Mg_mg_kg_dw, Al_mg_kg_dw, P_mg_kg_dw, S_mg_kg_dw, K_mg_kg_dw, Ca_mg_kg_dw, Ti_mg_kg_dw, V_mg_kg_dw, Cr_mg_kg_dw, Mn_mg_kg_dw, Fe_mg_kg_dw, Co_mg_kg_dw, Ni_mg_kg_dw, Cu_mg_kg_dw, Zn_mg_kg_dw, As_mg_kg_dw, Se_mg_kg_dw, Rb_mg_kg_dw, Sr_mg_kg_dw, Mo_mg_kg_dw, Ag_mg_kg_dw, Cd_mg_kg_dw, Cs_mg_kg_dw, Ba_mg_kg_dw, Tl_mg_kg_dw, Pb_mg_kg_dw, U_mg_kg_dw.
    - For each element, the dataset provides the concentration on a dry mass basis (mg/kg_dw) and associated notes.
  - Detection limits
    - Detection_Limit_<Element>_mg_kg_dw: detection limit for the given sample (mg/kg_dw), indicating when a concentration is below detectability.
    - Some entries indicate variations (e.g., “given sample”) or formatting nuances, but all serve to flag non-detects and detection thresholds.
  - Replicates and notes
    - Replicate samples are indicated (e.g., RCN119, 120, 121) to support quality assurance and reproducibility.

- Data quality and processing
  - The document outlines standardised data definitions to support verification, quality assurance, cleaning, and transformation.
  - Outputs are clear concentrations and detection-limiting indicators that can be compared against environmental standards or policy performance metrics.
  - Data are intended to be stored and uploaded to appropriate portals for accessibility and interoperability.

- Usage and interpretation guidance
  - Concentrations are reported as mg/kg_dw; non-detects are indicated via blanks with corresponding detection-limit fields.
  - Replicate samples help assess measurement reliability and variability.
  - The standardised format supports combining this dataset with other environmental data to evaluate ecosystem health and monitor policy outcomes over time.

- Practical considerations for analysts
  - Ensure proper handling of non-detects using Detection_Limit_<Element>_mg_kg_dw fields.
  - Maintain consistency with the sample metadata (Code, Type, Description, Collection Date) to enable temporal and spatial analyses.
  - Follow standardised methods and QA steps to align outputs (maps, charts, reports) with monitoring objectives.
  - Facilitate data sharing by preparing datasets that can be uploaded to monitoring portals, preserving underlying data accessibility.