# TREE_Northumbria_ICPMS_Earthworm_FM_Concentration

## Overview
- Dataset of metal and metalloid concentrations in earthworms measured as milligrams per kilogram of fresh mass (mg/kg FM).
- Includes a wide range of elements (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U).
- Associated biological and sampling context: Latin and common species names, sampling site, date of collection, UKCEH sample codes and descriptions, and notes.

## Data Structure
- Core metadata fields:
  - Latin_Species_Name, Common_Species_Name
  - Site, Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Notes
- Concentration fields (examples):
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Note: There are inconsistencies in the explanatory text for several concentration fields (many lines incorrectly state "Concentration of Fe" or similar), indicating metadata quality issues.

## Provenance and Scope
- Appears to be associated with Northumbria ICPMS earthworm sampling (eco-chemical dataset) and UKCEH sample coding.
- ICPMS indicates the analytical method used for multi-element determination.
- Focus is on the fresh mass basis (FM) of earthworms.

## Data Quality and Metadata Considerations
- Metadata quality issues:
  - Repeated incorrect explanations in several concentration fields (e.g., misattributed “Concentration of Fe” in descriptions).
  - Requires cleaning and standardization to ensure accurate, consistent metadata and variable descriptions.
- Units consistency:
  - All concentration fields are intended as mg/kg FM; verify exact unit definitions across the dataset.
- Data usability:
  - Clear linkage between sample codes (CEH_Sample_Codes) and sample descriptions (CEH_Sample_Description) is essential for reuse and provenance.
  - Need for consistent naming and documentation to support cross-dataset integration.

## Relevance for Data Leaders
- Illustrates the importance of an end-to-end data asset: biological context, sampling metadata, and chemical measurements all in one schema.
- Highlights need for:
  - Comprehensive, accurate metadata to enable discovery and reuse.
  - Standardization of units, variable names, and descriptions.
  - Clear data governance around sample identification and description.
- Demonstrates cross-domain data integration (taxonomy, sampling sites, temporal context, and multi-element chemistry).

## Challenges and Opportunities
- Challenges:
  - Fragmented or inconsistent metadata across variables can hinder data discovery and interoperability.
  - Ensuring data accuracy when descriptions are misaligned with data fields.
- Opportunities:
  - Use as a case to implement metadata cleansing, standardization, and validation workflows.
  - Strengthen data cataloging and cross-reference capabilities with CEH sample codes and descriptions.
  - Improve data governance to support reuse by partner networks and policy or research teams.

## Recommended Actions for Data Management (aligned with Data Leaders)
- metadata sanitation:
  - Correct inconsistent explanations for concentration fields; ensure each variable has an accurate, specific description.
  - Validate and standardize unit definitions (mg/kg_FM) across all concentration variables.
- metadata enrichment:
  - Ensure CEH_Sample_Codes and CEH_Sample_Description are complete and linkable to sampling events.
  - Add clear provenance notes (sampling method, analysis method, QA/QC steps) if missing.
- data governance and discovery:
  - Develop a data dictionary for this dataset with standardized variable names and descriptions.
  - Register dataset in a data catalog with rich metadata to improve discoverability and interoperability.
- data quality controls:
  - Implement data validation to verify numeric ranges, detect outliers, and confirm alignment between sample metadata and concentration data.
  - Establish versioning and change-log practices for metadata and data updates.
- interoperability:
  - Align with relevant data standards for environmental chemistry and biological sampling to facilitate cross-network sharing.