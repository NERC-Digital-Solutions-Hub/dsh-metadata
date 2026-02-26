# TREE_Northumbria_ICPMS_Woodmice_mg_per_tissue_FM_Concentration

## Overview
- Dataset header describing ICP-MS measured concentrations of multiple elements in wood mouse tissues.
- Measurements are given as mg of each element per total tissue fresh mass (FM).
- Includes taxonomic and sampling metadata (Latin and common species names, site, date collected, UKCEH sample codes and descriptions, tissue type).
- Some data fields indicate detection limits or are explicitly marked as not collected for certain tissues (e.g., hind leg bone, thyroid, liver for specific woodmice).

## Data structure and key fields
- Taxonomic and sampling metadata
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Tissue
- Measurement fields (examples of elements; each represented as mg_per_tissue_FM)
  - I_mg_per_tissue_FM
  - Li_mg_per_tissue_FM
  - Na_mg_per_tissue_FM
  - Al_mg_per_tissue_FM
  - P_mg_per_tissue_FM
  - K_mg_per_tissue_FM
  - Ca_mg_per_tissue_FM
  - Ti_mg_per_tissue_FM
  - V_mg_per_tissue_FM
  - Cr_mg_per_tissue_FM
  - Mn_mg_per_tissue_FM
  - Fe_mg_per_tissue_FM
  - Co_mg_per_tissue_FM
  - Ni_mg_per_tissue_FM
  - Cu_mg_per_tissue_FM
  - Zn_mg_per_tissue_FM
  - As_mg_per_tissue_FM
  - Se_mg_per_tissue_FM
  - Rb_mg_per_tissue_FM
  - Sr_mg_per_tissue_FM
  - Mo_mg_per_tissue_FM
  - Ag_mg_per_tissue_FM
  - Cd_mg_per_tissue_FM
  - Cs_mg_per_tissue_FM
  - Tl_mg_per_tissue_FM
  - Pb_mg_per_tissue_FM
  - U_mg_per_tissue_FM
- Data format notes per field
  - Some entries include “<” markers indicating concentration is below a detection limit.
  - In several columns, there are explicit notes about data not being collected for woodmice thyroid or specific tissues (e.g., hind leg bone, liver for certain samples).

## Data quality, gaps, and caveats
- Notable missing data:
  - No data for Hind Leg Bone and woodmice 8 liver.
  - No data collected for woodmice thyroid for many elements.
- Some fields specify that outputs are not available for specific tissues or samples, requiring careful handling during analysis.
- Detection limits are indicated with “<” in certain concentration fields.

## How to use (Data Support perspective)
- Self-serve analysis:
  - Build dashboards or pivot tables to compare element concentrations across sites, dates, and tissues.
  - Join measurement fields with sample metadata (site, date, tissue) for contextual insights.
- Data quality and transformation:
  - QA: verify presence/absence of data per tissue and per element; flag and document missing data.
  - Cleaning: standardize units and handle detection-limit markers (<) appropriately (e.g., imputation or flagging).
  - Transformation: convert to consistent formats, align tissue naming conventions, and map CEH sample codes to descriptions.
- Reporting and dissemination:
  - Create summarized reports or charts showing general patterns of elemental concentrations, while clearly signaling where data are absent.
  - Share early prototypes to gather feedback and iteratively improve data products and coverage.

## Practical considerations
- Given patchy data across tissues and elements, plan analyses with explicit handling of missing data and detection limits.
- Maintain provenance by linking concentrations back to CEH sample codes and descriptions, site information, and collection dates.
- Communicate clearly any limitations due to unavailable data (e.g., thyroid measurements not collected for many elements) when presenting findings.