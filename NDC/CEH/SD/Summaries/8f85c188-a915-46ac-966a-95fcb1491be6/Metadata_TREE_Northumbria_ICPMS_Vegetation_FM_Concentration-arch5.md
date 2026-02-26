# TREE_Northumbria_ICPMS_Vegetation_FM_Concentration

## Overview
- A dataset of ICP-MS concentration measurements in vegetation from Northumbria, including species and sampling metadata.
- Concentrations are reported on a fresh mass basis (FM) for a wide range of elements; data include both taxonomy and sample provenance.

## Data structure and key fields
- Taxonomy and naming
  - Latin_Species_Name: Latin name of species (explanation provided).
  - Common_Species_Name: Common name of species (explanation provided).
- Sampling metadata
  - Site: Sampling site (explanation provided).
  - Date_Sample_Collected: Date sample collected (explanation provided).
  - CEH_Sample_Identifier: UKCEH sample identifier (explanation provided).
  - CEH_Sample_Description: UKCEH sample description (explanation provided).
- Sample processing and context
  - Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to dry mass for the sample (explanation provided).
  - n/a indicators: Some fields use "n/a" to denote no information.
- Concentration measurements (all in mg/kg_FM)
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM.
- Notation and qualifiers
  - Some concentration columns use a less-than marker (e.g., <I, <Pb) to indicate values reported as thresholds rather than exact measurements; accompanying explanations describe the qualifier behavior.
  - n/a indicates no information for a field or entry.

## Data quality and governance considerations
- Units and basis
  - All concentration values are on a fresh mass (FM) basis and reported in mg/kg.
- Metadata completeness
  - Several fields may be incomplete (denoted by n/a); metadata completeness is essential for usability and traceability.
- Notation handling
  - Less-than qualifiers must be interpreted appropriately during analysis to avoid bias in summary statistics.
- Provenance and traceability
  - CEH_Sample_Identifier and CEH_Sample_Description support traceability to UKCEH data sources.
- Processing notes
  - Fresh_Mass_Dry_Mass_Ratio provides context for potential conversion to dry mass if required for cross-study comparability.

## Sharing, access and interoperability considerations
- Stewardship responsibilities
  - Upload datasets to relevant portals and catalogue holdings; document data processing steps.
  - Maintain updates and ensure that sharing limitations or embargoes are respected.
- Standardization and interoperability
  - Maintain consistent field naming, units, and qualifiers to enable cross-dataset interoperability across systems.
- Provisional constraints
  - Be aware of disclosure risks or proprietary issues that may affect data availability or timing of release.

## Challenges and considerations for data stewards
- Incomplete picture of user needs and priorities.
- Timeliness of data delivery from data creators.
- Encouraging data creators to meet standards, including metadata completeness.
- Managing multiple systems and formats, including difficult ones.
- Handling large datasets with many concentration measurements.
- Dealing with outdated databases requiring bespoke, non-interoperable solutions.

## Practical next steps for data stewards
- Validate and complete key metadata fields (e.g., Latin/Common species names, site, date, CEH identifiers).
- Ensure consistent units (mg/kg_FM) and clearly document the Fresh_Mass_Dry_Mass_Ratio usage.
- Explicitly document handling of less-than values and any data exclusions.
- Align dataset documentation with portal requirements and create clear data release notes.