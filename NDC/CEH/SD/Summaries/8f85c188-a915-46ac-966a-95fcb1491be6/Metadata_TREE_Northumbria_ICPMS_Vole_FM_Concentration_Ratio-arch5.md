# TREE_Northumbria_ICPMS_Vole_FM_Concentration_Ratio

## Overview
- A data dictionary-like record for a dataset of ICP-MS concentration ratios in vole samples relative to surrounding soil.
- Purpose: document concentration ratios calculated as Fresh Mass Vole (wholebody) divided by Dry Mass Soil, linking vole samples to their soil context.
- Includes sample identifiers, metadata, site information, and a large set of elemental concentration ratio fields, with qualifiers for non-detects or less-than values.

## Dataset structure and key fields
- Core identifiers and metadata
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Code
  - CEH_Sample_Description
  - Notes
- Spatial/ Provenance linkage
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio measurements (per element; numerator is Fresh Mass Vole, denominator is Dry Mass Soil)
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
  - Mn_Concentration_Ratio
  - Fe_Concentration_Ratio
  - Co_Concentration_Ratio
  - Ni_Concentration_Ratio (including a <Ni variant)
  - Cu_Concentration_Ratio
  - Zn_Concentration_Ratio
  - As_Concentration_Ratio
  - Se_Concentration_Ratio
  - Rb_Concentration_Ratio
  - Sr_Concentration_Ratio
  - Mo_Concentration_Ratio
  - Ag_Concentration_Ratio (including a <Ag variant)
  - Cd_Concentration_Ratio
  - Cs_Concentration_Ratio
  - Ba_Concentration_Ratio (two fields: Ba_Concentration_Ratio_1 and Ba_Concentration_Ratio_2)
  - Tl_Concentration_Ratio (two fields: Tl_Concentration_Ratio_1 and Tl_Concentration_Ratio_2)
  - Pb_Concentration_Ratio (two fields: Pb_Concentration_Ratio_1 and Pb_Concentration_Ratio_2)
  - U_Concentration_Ratio (two fields: U_Concentration_Ratio_1 and U_Concentration_Ratio_2)
- Note on data qualifiers
  - Some fields are prefixed with "<" to indicate less-than values (e.g., <Be_Concentration_Ratio).
  - Several fields indicate n/a in units, implying dimensionless ratios or unspecified units.

## Data quality and governance considerations
- Units and standardization
  - Most fields show Units = n/a; consider documenting and enforcing a consistent unit policy or confirm they are dimensionless ratios.
- Data completeness
  - Presence of n/a and potential missing values; implement validation rules to flag incomplete records.
- Data qualifiers and handling of censored data
  - Less-than indicators (<Be, <Ni, <Ag, <U) require clear policy for downstream analysis (e.g., treatment of censored data).
- Schema integrity and interoperability
  - Some column naming inconsistencies and typographical issues (e.g., duplicated or oddly formatted names) may hinder interoperability; standardize field names.
- Provenance and processing transparency
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio should be linked to soil sampling metadata.
  - Document the exact calculation method for each ratio, including any data transformations or substitutions for censored values.
- Metadata completeness
  - Include data collection protocols, instrument settings, detection limits, and QA/QC procedures to support reuse.

## Provenance, processing, and usage
- Calculation basis
  - Concentration Ratios are defined as Fresh Mass Vole (wholebody) divided By Dry Mass Soil.
- Linkage
  - Each ratio field can be tied to a specific soil sample location via Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio.
- Potential uses
  - Environmental monitoring and ecological risk assessment.
  - Studies of bioaccumulation and uptake of trace elements by vole populations.

## Recommendations for Data Stewards
- Strengthen metadata
  - Add explicit units, measurement methods, and detection limits for all ratio fields.
  - Provide a documented data dictionary with standardized field names and vocabularies (e.g., species, site, and soil sampling identifiers).
- Improve data quality controls
  - Implement validation for numeric ratio fields, handle censored (<) values consistently, and flag incomplete records.
- Enhance provenance and processing notes
  - Record data source, raw vs. processed status, and every processing step (including how < values are treated in analyses).
- Standardize interoperability
  - Clean up column names for consistency, and consider consolidating duplicated or closely related fields (e.g., Ba_Concentration_Ratio_1/2 and Tl_Concentration_Ratio_1/2) unless they represent distinct measurements.
- Documentation and accessibility
  - Publish a data usage guide describing context, sampling design, and data lifecycle; ensure updates are versioned and traceable.
- Governance alignment
  - Align with organisational data governance policies for data sharing, discoverability, and stewardship responsibilities.