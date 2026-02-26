# TREE_Northumbria_ICPMS_Earthworm_FM_Concentration_Ratio

## Overview
- Dataset intended to characterize bioaccumulation by earthworms through concentration ratios of elements in whole-body fresh mass to dry-mass soil.
- Supports environmental health monitoring by informing policy scrutiny, evaluation, and decision-making about contamination and ecological risk.

## Data Structure and Key Variables
- Species and sampling context
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Notes
- Sampling context and comparability
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio (description of soil sample used for the ratio)
- Concentration ratios (calculation: Fresh Mass Earthworm (wholebody) divided By Dry Mass Soil)
  - I_Concentration_Ratio
  - Li_Concentration_Ratio
  - Be_Concentration_Ratio
  - Na_Concentration_Ratio
  - Mg_Concentration_Ratio
  - Al_Concentration_Ratio
  - P_Concentration_Ratio
  - K_Concentration_Ratio
  - Ca_Concentration_Ratio
  - Ti_Concentration_Ratio
  - V_Concentration_Ratio
  - Cr_Concentration_Ratio
  - Fe_Concentration_Ratio
  - Co_Concentration_Ratio
  - Ni_Concentration_Ratio
  - Cu_Concentration_Ratio
  - Zn_Concentration_Ratio
  - As_Concentration_Ratio
  - Se_Concentration_Ratio
  - Rb_Concentration_Ratio
  - Sr_Concentration_Ratio
  - Mo_Concentration_Ratio
  - Ag_Concentration_Ratio
  - Cd_Concentration_Ratio
  - Cs_Concentration_Ratio
  - Ba_Concentration_Ratio
  - Tl_Concentration_Ratio
  - Pb_Concentration_Ratio
  - U_Concentration_Ratio
- Notes on units and data labeling
  - Units for many concentration ratios are listed as n/a
  - Some rows contain inconsistencies or typos (e.g., Fe_Concentration_Ratio explanatory text references MnConcentration Ratio; Tl vs Ti naming in TiConcentration_Ratio field)

## Calculation Method
- Concentration Ratio definition: Fresh Mass Earthworm (wholebody) divided By Dry Mass Soil
- Co-located soil sample is used to calculate each concentration ratio

## Data Context and Source
- Source: TREE_Northumbria_ICPMS_Earthworm dataset
- Focused on earthworms and a broad suite of elements measured by ICP-MS
- Includes specimen-level identifiers and sampling metadata to support traceability and cross-site comparisons

## Metadata, Data Governance, and Accessibility
- Metadata presence for key fields (species, site, date, soil sample context) is essential for interpretability
- Public sharing of underlying data is a listed consideration and can be a barrier in practice
- Quality assurance, data cleaning, transformation, and clear presentation (reports, charts, dashboards) are expected
- Data governance requirements to ensure datasets meet standards, are stored and kept up to date, and are openly shareable where possible

## Practical Implications for Monitoring Framework Authors
- Enables assessment of bioavailability and potential ecological risk across sites and species via concentration ratios
- Supports policy evaluation related to soil contamination and biotic uptake in ecosystems
- Provides a structured approach to documenting sampling context (co-located soil) and measurement scope (broad element suite)

## Challenges and Considerations
- Data availability and metadata completeness may be inconsistent, hindering verification and reuse
- Frequent data governance and sharing barriers could limit accessibility of the full dataset
- Inconsistencies or mislabeling in the field definitions (e.g., Fe_Concentration_Ratio description; Tl/Ti naming) require clarification and standardization
- Units are often listed as n/a, which may affect cross-study comparability and interpretation

## Recommendations for Monitoring Framework Authors
- Standardize metadata fields and ensure consistent naming and labeling for all concentration ratios
- Provide clear units or justification for absence of units to improve comparability
- Implement robust data governance: provenance, versioning, and open-data considerations aligned with policy needs
- Validate and correct any typographical or misannotation issues in the data dictionary (e.g., Fe vs Mn references, Ti/Tl naming)
- Ensure co-located soil context is consistently captured to support accurate concentration-ratio calculations
- Promote accessible data sharing while safeguarding sensitive information and metadata quality to reduce barriers to uptake