# TREE_Northumbria_ICPMS_Frog_and_Frogspawn_FM_Concentration

- Overview
  - A dataset metadata description for ICP-MS measured concentrations of various elements in frog and frogspawn tissue from Northumbria.
  - Key fields cover species identity, sampling context, UKCEH sample codes, tissue type, and multi-element concentrations expressed as mg/kg in fresh mass (FM).
  - Includes indicators for less-than values and fields with non-applicable or missing units.

- Data Schema / Key Variables
  - Taxonomy and identity
    - Latin_Species_Name
    - Common_Species_Name
  - Sampling context
    - Site
    - Date_Sample_Collected
  - UKCEH metadata
    - CEH_Sample_Codes
    - CEH_Sample_Description
  - Tissue and mass
    - Tissue
    - Fresh_Mass_Dry_Mass_Ratio
  - Concentration measurements (mg/kg FM)
    - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM
    - Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM
    - Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM
    - Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM
    - Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM
    - Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
  - Data flags and notes
    - With < markers indicating concentrations below detection or reporting thresholds
    - Some field descriptions contain inconsistencies or misalignments (potential data dictionary errors)

- Data Quality and Anomalies
  - Several misalignments in the field descriptions (e.g., mislabeling of Ti vs Ca, Ca vs Ti; typographical errors in some column names).
  - Some columns show inconsistent naming or formatting (e.g., Fresh_Mass_Dry_Mass_Ra tio).
  - "<" flags are present for certain concentration columns (below detection limits) and should be treated accordingly in analyses.
  - Units are consistently mg/kg FM for concentrations, but some descriptions show "n/a" or unclear mappings, indicating a need for data cleaning and column verification.

- Potential Analyses and Use
  - Multi-element exposure assessment in frog tissues, comparing species, sites, and sampling dates.
  - Identification of spatial or temporal patterns in metal concentrations.
  - Correlations between element concentrations and tissue type or fresh/dry mass ratio.
  - Risk screening against ecological or health-based thresholds, with attention to detection limits.

- Provenance, Access, and Documentation
  - Data derived from UK Centre for Ecology & Hydrology (UKCEH) sample codes and Northumbria sampling context.
  - Metadata suggests a formal data dictionary intended to support data discovery and reproducibility, including sample descriptions and coding.
  - Prior to analysis, ensure proper data cleaning, consistent column mappings, and resolution of misaligned field descriptions.