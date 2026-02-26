# Supporting documentation for Soil_Stable_Element.csv

## Overview
- Defines the metadata and data columns for Soil_Stable_Element.csv.
- Columns cover sample identifiers, sample description, collection date, and concentrations of a wide range of elements.
- All element concentrations are reported on a dry mass basis (mg/kg).
- Each concentration column has a corresponding detection limit column.
- RCN119, 120, and 121 are noted as replicate soil samples.
- Collection dates use the format: dd month yyyy.
- The documentation format includes repeated descriptions and variants due to the data structure (e.g., “given sample” notes and multiple formatting lines).

## Key Columns (data structure)
- Sample metadata
  - Sample_Code: Unique sample identifier.
  - Sample type: Type of sample.
  - Sample_Description: Further explanation of the sample (e.g., context or characteristics).
  - Collection_Date: Date of soil sample collection.

- Concentration measurements (all on a dry mass basis)
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

- Detection limits (one per each concentration column)
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

## Units and interpretation
- Concentrations: milligrams per kilogram (mg/kg) on a dry mass basis.
- Detection limits: mg/kg corresponding to each concentration column.
- How to interpret blanks:
  - If a concentration value is blank for a given sample, the concentration is below the detection limit.
  - The relevant Detection_Limit column for that sample shows the detection threshold.
  - If a concentration is present, it is above the detection limit for that sample.

## Replicates and sample details
- Replicate samples: RCN119, RCN120, and RCN121 are noted as replicate soil samples.
- Sample descriptions provide context for each sample, aiding interpretation and traceability.

## Practical guidance for analysts
- To interpret a data row:
  - Identify the Sample_Code, Sample_Type, and Collection_Date.
  - For each element, check the I- or X_mg_kg_dw value; if blank, consult the corresponding Detection_Limit_X_mg_kg_dw to understand the lower bound.
  - Use replicates (e.g., RCN119-121) to assess measurement consistency.
- Data quality considerations:
  - Be mindful of potential formatting inconsistencies across the long list of element/detection-limit columns.
  - Ensure units are consistently interpreted as mg/kg on a dry mass basis.
- Use-case alignment:
  - The documentation supports analyses requiring standardized, comparable element concentrations across soil samples, with explicit detection limits to support censoring decisions in statistical analyses.