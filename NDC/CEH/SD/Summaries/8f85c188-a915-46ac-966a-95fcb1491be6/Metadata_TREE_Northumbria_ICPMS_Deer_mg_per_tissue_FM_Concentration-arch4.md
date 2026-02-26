# TREE_Northumbria_ICPMS_Deer_mg_per_tissue_FM_Concentration

## Purpose and scope
- A dataset of ICP-MS measured concentrations of multiple elements in deer tissue from Northumbria.
- Concentrations are expressed as milligrams per total deer tissue fresh mass (mg per_tissue_FM).

## Data structure and fields
- Metadata fields:
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Tissue
- Concentration fields (examples; all presented as mg per_tissue_FM):
  - I_mg_per_tissue_FM, Li_mg_per_tissue_FM, Be_mg_per_tissue_FM, Na_mg_per_tissue_FM, Mg_mg_per_tissue_FM, Al_mg_per_tissue_FM
  - P_mg_per_tissue_FM, K_mg_per_tissue_FM, Ca_mg_per_tissue_FM, Ti_mg_per_tissue_FM, V_mg_per_tissue_FM
  - Cr_mg_per_tissue_FM, Mn_mg_per_tissue_FM, Fe_mg_per_tissue_FM, Co_mg_per_tissue_FM, Ni_mg_per_tissue_FM
  - Cu_mg_per_tissue_FM, Zn_mg_per_tissue_FM, As_mg_per_tissue_FM, Se_mg_per_tissue_FM, Rb_mg_per_tissue_FM
  - Sr_mg_per_tissue_FM, Mo_mg_per_tissue_FM, Ag_mg_per_tissue_FM, Cd_mg_per_tissue_FM, Cs_mg_per_tissue_FM
  - Ba_mg_per_tissue_FM, Tl_mg_per_tissue_FM, Pb_mg_per_tissue_FM, U_mg_per_tissue_FM
- Special notations and notes:
  - Some entries use "<" to indicate concentrations below detection/quantification limits.
  - Some fields reference thyroid measurements (e.g., thyroid columns) vs. total tissue.
  - Specific note: No data for Roe deer 4 thyroid for several elements.
  
## Data quality and limitations
- Data gaps:
  - No data for Roe deer 4 thyroid in many concentration fields.
- Data provenance:
  - Linked to UKCEH sample codes and descriptions; units are consistent (mg per_tissue_FM).
- Metadata and standardization:
  - Some inconsistencies in column naming (e.g., thyroid-related columns) suggesting a need for harmonization.
  - Occasional n/a values; may require explicit documentation of missingness and detection-limit treatment.

## Implications for Data Leaders
- Useful for cross-network analysis of wildlife metal concentrations and data-system thinking.
- Highlights importance of:
  - Clear, harmonized metadata and units to enable discoverability and interoperability.
  - Documenting detection limits and handling of "<" values in analyses.
  - Coordinating data collection to fill gaps (notably Roe deer thyroid data) and improve coverage.
- Recommendations:
  - Stabilize and standardize column names (especially thyroid vs. whole-tissue measurements).
  - Maintain detailed metadata to support reuse and integration with other datasets (e.g., sample locations, dates, and tissue types).