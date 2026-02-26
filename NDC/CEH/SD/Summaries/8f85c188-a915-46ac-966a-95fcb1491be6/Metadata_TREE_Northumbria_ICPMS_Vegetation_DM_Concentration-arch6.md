# TREE_Northumbria_ICPMS_Vegetation_DM_Concentration

## Overview
- Metadata/dictionary for ICP-MS measurements of vegetation from Northumbria.
- Focuses on concentrations of multiple elements in plant tissue, expressed as milligrams per kilogram of dry mass (mg/kg_DM).
- Includes sampling and sample-identification details (species names, site, date collected, CEH identifiers and descriptions).

## Data Structure and Key Fields
- Core metadata fields:
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Identifier
  - CEH_Sample_Description
- Concentration fields (one per element, in mg/kg_DM):
  - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM.
- Notation for 'less than' values:
  - Columns prefixed with < (e.g., <I, <Li) indicate concentrations reported as below detection/less than a value.
  - Some elements have dual-part or paired notation (e.g., Se_mg_kg_DM_1, Se_mg_kg_DM_2; Rb_mg_kg_DM_1/2; Tl_mg_kg_DM_1/2) to capture upper/lower bounds or split information.
- Descriptive/auxiliary fields:
  - CEH_Sample_Description
  - n/a markers indicate missing information in some fields.
- Formatting notes imply some irregularities (e.g., mixed punctuation) in the data dictionary.

## Special Coding and Notation
- <I, <Li, <Be, etc. denote concentrations below the stated value.
- Some elements use a two-part or paired coding scheme to store additional information about the measurement (e.g., Se_mg_kg_DM_1/2 and similar patterns).
- Emphasis on dry mass basis for all elemental concentrations.

## Units, Data Quality and Handling Notes
- All elemental concentrations are in mg/kg_DM.
- Concentrations are tied to specific samples via sampling metadata; ensure consistent linkage across species, site, and sample identifiers.
- The presence of “n/a” information and formatting inconsistencies suggests careful data cleaning and validation when using this dataset for analysis.

## How this Supports Data Work
- Provides a clear, structured schema enabling data integration across species, sites, and sample events.
- Facilitates quality assurance, cleaning, and transformation into analysis-ready formats (dashboards, pivot tables, reports).
- Supports handling of non-detect (<) values and two-part value coding for accurate interpretation and visualization.
- Aids in communicating data provenance and context to end users and stakeholders.

## Practical Use and Considerations
- Use the metadata to align species names, sampling sites, and sample identifiers before analysis.
- Implement rules for interpreting < value markers and two-part codes to avoid bias in summaries.
- Leverage the comprehensive element list to examine nutrient/trace-metal patterns across species and environments.
- Be mindful of incomplete fields (n/a) and formatting irregularities during data preparation and documentation.