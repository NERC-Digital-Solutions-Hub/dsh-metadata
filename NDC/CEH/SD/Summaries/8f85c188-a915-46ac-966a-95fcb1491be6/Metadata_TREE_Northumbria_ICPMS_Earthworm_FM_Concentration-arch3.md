# TREE_Northumbria_ICPMS_Earthworm_FM_Concentration

## Overview
- Dataset schema for earthworm tissue concentrations measured by ICPMS.
- Records concentrations of multiple elements (in mg/kg fresh mass) alongside sampling and specimen metadata.
- Includes species identification, sampling site, date collected, and UKCEH sample codes/descriptions.

## Key Fields / Data Schema
- Biological and sampling metadata
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes (UKCEH sample codes)
  - CEH_Sample_Description
  - Notes

- Concentration measurements (all in mg/kg fresh mass)
  - I_mg_kg_FM
  - Li_mg_kg_FM
  - Be_mg_kg_FM
  - Na_mg_kg_FM
  - Mg_mg_kg_FM
  - Al_mg_kg_FM
  - P_mg_kg_FM
  - K_mg_kg_FM
  - Ca_mg_kg_FM
  - Ti_mg_kg_FM
  - V_mg_kg_FM
  - Cr_mg_kg_FM
  - Mn_mg_kg_FM
  - Co_mg_kg_FM
  - Ni_mg_kg_FM
  - Cu_mg_kg_FM
  - Zn_mg_kg_FM
  - As_mg_kg_FM
  - Se_mg_kg_FM
  - Rb_mg_kg_FM
  - Sr_mg_kg_FM
  - Mo_mg_kg_FM
  - Ag_mg_kg_FM
  - Cd_mg_kg_FM
  - Cs_mg_kg_FM
  - Ba_mg_kg_FM
  - Tl_mg_kg_FM
  - Pb_mg_kg_FM
  - U_mg_kg_FM

- Notes on field definitions
  - Units are mg/kg (fresh mass) for all elemental concentrations.
  - Explanations provide the intended meaning of each field; some descriptions in the source material incorrectly reference other elements (e.g., repeated “Concentration of Fe” in several explanations), highlighting the need for careful metadata validation.

## Data Quality and Metadata Considerations
- Metadata completeness: Field-level descriptions exist, but some explanations may require correction to ensure accuracy (e.g., element-specific explanations should reference the correct element).
- Data standardization: Concentrations are consistently defined as mg/kg_FM across all elements, enabling cross-element comparisons.
- Provenance and codes: UKCEH sample codes and descriptions are included to support traceability; consistent coding is essential for linking to other datasets.
- Potential gaps: As with many monitoring datasets, metadata completeness and up-to-date provenance information are critical to ensure usability across monitoring programs.

## Data Governance and Sharing
- The dataset appears designed to support transparent data sharing, with explicit sample codes and descriptive fields.
- Governance needs include ensuring metadata accuracy, maintaining data quality through QA/QC, and establishing clear data management standards at the data origin.
- Public sharing of underlying data can be a barrier if metadata are incomplete or inconsistent; robust metadata and QA processes help mitigate this.

## Relevance for Monitoring Frameworks
- Illustrates a structured approach to environmental health monitoring data: specimen metadata linked to multi-element concentration data.
- Facilitates stakeholder engagement, data verification, and reuse in dashboards, reports, and trend analyses.
- Supports decision-making by enabling comparisons across species, sites, and time, provided data governance and metadata quality are maintained.