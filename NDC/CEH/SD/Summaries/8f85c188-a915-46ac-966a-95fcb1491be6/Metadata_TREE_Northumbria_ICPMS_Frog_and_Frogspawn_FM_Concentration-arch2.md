# TREE_Northumbria_ICPMS_Frog_and_Frogspawn_FM_Concentration

## Overview
- Dataset of concentrations of multiple elements in frog tissue or frogspawn (FM) collected for environmental monitoring at Northumbria.
- Uses ICP-MS to quantify element levels in biological samples from specified sites and dates.
- Aims to provide standardized outputs (e.g., trend analyses, health indicators) for environmental health and policy performance over time.

## Data Structure and Key Variables
- Core identifiers
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue (frog tissue or frogspawn)
  - Fresh_Mass_Dry_Mass_Ratio
- Concentration data (all in mg/kg FM unless noted)
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM
  - Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM
  - Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM
  - Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM
  - Se_mg_kg_FM, Rb_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM
  - Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Data considerations
  - Some columns use a “<” marker to indicate concentrations below detection limits.
  - Several lines contain annotation inconsistencies (e.g., Ti_mg_kg_FM descriptions incorrectly reference Ca). Indicates need for data cleaning and metadata verification.

## Data Quality and Processing
- Data handling workflow aligns with the analysts’ standardised approach: verify, quality assure, clean, and transform data from established sources.
- Outputs are produced in clear formats (reports, maps, charts) to compare environmental health against standards.
- Datasets should be stored and uploaded to appropriate data portals for accessibility and long-term preservation.

## Outputs and Reporting
- Visual and tabular outputs by:
  - Species and site
  - Date of sampling
  - Tissue type
  - Element concentration profiles (mg/kg FM)
- Potential analyses include temporal trends, spatial comparisons, and health indicator assessments against environmental standards.

## Relevance to the Analysts Monitoring the Environment Archetype
- Provides standardized, source-verified concentration data essential for monitoring environmental health over time.
- Facilitates cross-site and cross-species comparisons using uniform units and data structure.
- Supports transparency and scrutiny of policy performance via accessible datasets and outputs.

## Notes and Anomalies
- The metadata text contains several typographical inconsistencies (e.g., Ti_mg_kg_FM descriptions mislabeling Ti as Ca, and similar errors for other elements), suggesting the need for data cleaning and metadata correction before analysis.