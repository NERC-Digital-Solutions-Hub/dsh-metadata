# Supporting documentation for Soil_Stable_Element.csv

- The document is metadata and field descriptions for the Soil_Stable_Element.csv dataset.
- It defines the meaning, units, and interpretation rules for each column to support consistent monitoring and data governance.

## Overview of dataset structure

- Core identifiers
  - Sample_Code: Unique sample identifier.
  - Sample type: Type of sample.
  - Sample_Description: Further explanation of the sample (e.g., depth; RCN119, 120 and 121 are replicate soil samples; units: cm).
  - Collection_Date: Date of soil sample collection (format: dd month yyyy).

- Element concentration columns (dry mass basis)
  - Examples include I-127_mg_kg_dw, Li_mg_kg_dw, Be_mg_kg_dw, B_mg_kg_dw, Na_mg_kg_dw, Mg_mg_kg_dw, Al_mg_kg_dw, P_mg_kg_dw, S_mg_kg_dw, K_mg_kg_dw, Ca_mg_kg_dw, Ti_mg_kg_dw, V_mg_kg_dw, Cr_mg_kg_dw, Mn_mg_kg_dw, Fe_mg_kg_dw, Co_mg_kg_dw, Ni_mg_kg_dw, Cu_mg_kg_dw, Zn_mg_kg_dw, As_mg_kg_dw, Se_mg_kg_dw, Rb_mg_kg_dw, Sr_mg_kg_dw, Mo_mg_kg_dw, Ag_mg_kg_dw, Cd_mg_kg_dw, Cs_mg_kg_dw, Ba_mg_kg_dw, Tl_mg_kg_dw, Pb_mg_kg_dw, U_mg_kg_dw.
  - Each field denotes the concentration of the element in milligrams per kilogram of dry mass (mg/kg_dw).

## Detection limits and non-detect handling

- For many elements, there is a corresponding Detection_Limit_<element>_mg_kg_dw column.
- Interpretation rules (illustrative pattern observed across elements):
  - If the concentration value is blank, it indicates the concentration was below the detection limit for that sample (non-detect).
  - The Detection_Limit_<element>_mg_kg_dw column provides the detection limit for the given sample.
  - In some cases, notes indicate “below the detection limit” or “concentration was detectable” relative to the associated concentration column.
  - Some elements have variants of the concentration column described as “<element>_mg_kg_dw, given sample” or similar, with associated detection-limit context.
- This structure supports distinguishing detected concentrations from non-detects and understanding the detection capability for each sample.

## Replicates and sample notes

- Replicate samples are identified in the Sample_Description (e.g., RCN119, 120, and 121 are replicate soil samples).
- The documentation provides consistent interpretation cues for replicates and non-detects to facilitate quality checks and comparability across samples.

## Units and standardization

- Concentrations: mg/kg_dw (milligrams per kilogram of dry mass) for all listed elements.
- Sample_Description may include depth information in centimeters (cm).
- The documentation standardizes how units and notes should be recorded and interpreted to enable clear reporting and data governance.

## Data quality, governance, and interoperability implications

- Emphasizes the importance of metadata completeness (explanation, units, notes) to verify data suitability for monitoring frameworks.
- Highlights handling of non-detects and detection limits as critical for accurate interpretation and reporting.
- Underlines the need to maintain data provenance, consistent terminology, and clear communication of complex findings when disseminating outputs from monitoring programs.