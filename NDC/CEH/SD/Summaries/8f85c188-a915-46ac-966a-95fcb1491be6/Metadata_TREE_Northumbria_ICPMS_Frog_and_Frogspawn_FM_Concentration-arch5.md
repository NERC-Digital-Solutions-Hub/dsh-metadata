# TREE_Northumbria_ICPMS_Frog_and_Frogspawn_FM_Concentration

## Overview
- A dataset of trace element concentrations in frog tissue or frogspawn from Northumbria, analyzed by ICP-MS.
- Captures both sample metadata (species, site, collection date, UKCEH sample codes/descriptions, tissue type) and chemical concentration data.
- Concentrations are reported as milligrams per kilogram fresh mass (mg/kg FM) for a broad suite of elements.
- Includes qualifiers for some measurements using a less-than symbol (e.g., <Be, <Al, <Ni, <Se, <U).
- Some field descriptions contain inconsistencies (e.g., misassigned explanatory text for certain elemental columns), indicating data quality considerations.

## Dataset Structure and Key Fields
- Taxonomy and identifiers
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
- Sample characteristics
  - Tissue (type of frog tissue or frogspawn)
  - Fresh_Mass_Dry_Mass_Ratio
- Concentration data (mg/kg FM)
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM
  - Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM
  - Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM
  - Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM
  - Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM
  - Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Data qualifiers
  - Some concentration fields may use a “<” prefix to indicate a less-than value.

## Data Governance and Standards
- UKCEH-related identifiers (CEH_Sample_Codes, CEH_Sample_Description) provide traceability to source samples.
- Units standardized to mg/kg fresh mass for comparability across samples.
- Metadata should clearly define sample collection context, site details, tissue type, and mass ratio to support reproducibility and reuse.
- Noted inconsistencies in the data descriptions (e.g., several concentration fields have misattributed explanatory text) that should be corrected to ensure accurate interpretation.
- Important to document any embargoes, proprietary considerations, or data sharing limitations affecting dataset updates.

## Data Quality and Limitations
- Challenges include:
  - Incomplete or evolving understanding of user needs for this dataset.
  - Timeliness of data delivery and updates to reflect new measurements.
  - Variability in data provenance and metadata completeness (e.g., collection context, site specifics).
  - Interoperability across different systems and formats; handling large datasets with many elemental columns.
- Specific data quality notes:
  - Some column descriptions appear misaligned (e.g., “Concentration of Ca in mg/kg fresh mass” shown in multiple places where it should refer to other elements), indicating a need for metadata cleaning.
  - Presence of “<” qualifiers requires consistent interpretation rules in downstream analyses.

## Practical Considerations for Data Stewards
- Ensure metadata accuracy and completeness:
  - Validate species names, sites, dates, and CEH codes against authoritative sources.
  - Confirm tissue types and the definition of Fresh_Mass_Dry_Mass_Ratio.
  - Clarify any ambiguous sample collection context to aid discovery and reuse.
- Standardize and document data quality rules:
  - Explicitly define how less-than values are stored and interpreted (e.g., detection limits).
  - Correct any erroneous explanatory text in concentration columns.
- Facilitate data sharing and updates:
  - Upload to appropriate data portals with consistent field definitions.
  - Maintain a changelog or metadata revision history to track corrections and updates.
  - Document any embargoes or access restrictions on specific samples or measurements.
- Align with user needs:
  - Ensure dataset discoverability through consistent naming, clear variable definitions, and linkage to related datasets (e.g., species, sites, sampling campaigns).

## Notes for Users and Reuse
- Use mg/kg FM as the standard concentration unit for cross-sample comparisons.
- Pay attention to qualifiers (< values) when performing quantitative analyses; establish handling rules in analysis workflows.
- Consult CEH_Sample_Codes and CEH_Sample_Description for sample provenance and context.
- Be aware of potential metadata inconsistencies and verify key fields (taxonomy, site, date, tissue) during data integration.