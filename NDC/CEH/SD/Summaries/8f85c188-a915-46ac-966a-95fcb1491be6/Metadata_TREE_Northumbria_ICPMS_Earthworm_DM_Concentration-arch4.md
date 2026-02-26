# TREE_Northumbria_ICPMS_Earthworm_DM_Concentration

## Purpose and scope
- Multi-element concentration data for earthworms (dry mass basis) collected in Northumbria, UK.
- Supports environmental contaminant monitoring, ecological risk assessment, and cross-site comparisons.
- Includes both biological identifiers and detailed sample metadata to enable traceability and data reuse.

## Data structure and key fields
- Biological identifiers:
  - Latin_Species_Name (Latin name)
  - Common_Species_Name (common name)
- Site and sampling:
  - Site
  - Date_Sample_Collected
- Provenance and sample identifiers:
  - CEH_Sample_Codes (UK CEH sample codes)
  - CEH_Sample_Description (UK sample description)
  - Notes (contextual notes about earthworms or sampling)
- Concentration measurements (all in mg/kg dry mass, DM):
  - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM
  - P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM
  - Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM
  - Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM
  - Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM
  - Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM
- Explanations accompany each element field (clarifying that it is the concentration of the element in mg/kg dry mass).

## Units and measurement notes
- All element concentrations are presented as mg/kg DM.
- Some fields include both a numeric name (e.g., I_mg_kg_DM) and a descriptive explanation (e.g., “Concentration of I in milligram per kilogram dry mass”).
- A few typographical inconsistencies appear in the headers (e.g., minor punctuation and formatting issues), which may impact automated parsing unless standardized.

## Data provenance and governance
- CEH_Sample_Codes and CEH_Sample_Description indicate UK Centre for Ecology & Hydrology involvement and provide traceability to original sample records.
- Metadata includes Notes for context; overall structure supports auditability and reuse across studies.

## Data quality and usability considerations
- Consistency and standardization:
  - Ensure uniform naming conventions across all element fields (I vs I_mg_kg_DM) for reliable schema parsing.
  - Resolve any typographical inconsistencies (e.g., Tl_mg_kg_DM_, and truncated descriptions) to improve data quality.
- Metadata completeness:
  - Confirm complete species and site details where missing or ambiguous (Units for some fields show n/a; explanations provide context but require consistent formatting).
  - Validate sample dates and codes against source records to enable proper temporal analyses.
- Granularity and comparability:
  - Data are element-specific concentrations in dry mass; confirm digestion method, detection limits, and QA/QC procedures to support cross-site comparisons.
- Discoverability and reusability:
  - A clear data dictionary and standardized field names will enhance discoverability within data catalogs and workflows.

## How Data Leaders can use and act on this dataset
- Assess environmental contamination by comparing multi-element profiles across sites and species.
- Integrate with broader data ecosystems (e.g., cross-partner datasets) to support co-ownership of data products and collaborative analyses.
- Prioritize data improvements by addressing gaps in metadata, standardizing field names, and documenting measurement methods and QA/QC.
- Leverage sample provenance (CEH codes and descriptions) to link chemical data with ecological context and sampling history.

## Gaps and potential actions
- Action: standardize field names and fix typographical inconsistencies for reliable ingestion and analysis.
- Action: complete and harmonize metadata (units, explanations, and method details) across all fields.
- Action: document measurement methods, QA/QC procedures, and detection limits to support interpretation and comparability.