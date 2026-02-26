# TREE_Northumbria_ICPMS_Toad_FM_Concentration

## Overview
- Dataset header for toad tissue concentration analysis using ICP-MS from Northumbria.
- Captures both metadata about samples and a broad suite of elemental concentrations normalized to fresh mass (mg/kg FM).

## Key data fields

- Taxonomy and site
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected

- Sample identifiers and descriptions
  - CEH_Sample_Code
  - CEH_Sample_Description
  - Fresh_Mass_Ash_Mass_Ratio (ratio of whole-body fresh mass to ash mass)
  - Notes (preparation notes; e.g., “separate tissues were not prepared”)

- Analytical measurements (all in mg/kg FM)
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
  - Mn_mg_kg_FM
  - Fe_mg_kg_FM
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

- Data quality notes
  - Some field descriptions appear corrupted or ambiguously labeled (e.g., incorrect elemental descriptors in certain lines), indicating potential data quality issues in the schema.

## Data context and potential uses

- Enables analysis of elemental exposure or accumulation in toad tissue across samples and sites.
- Facilitates exploration of correlations between elements, body/tissue mass normalization (Fresh_Mass_Ash_Mass_Ratio), and sampling metadata (Site, Date_Sample_Collected).
- Supports cross-dataset linking via CEH_Sample_Code and CEH_Sample_Description for broader environmental monitoring work.

## Potential analyses and considerations

- Compare element concentrations across sites and dates to identify spatial or temporal patterns.
- Assess relationships between mass normalization ratio and element concentrations.
- Examine multivariate profiles to detect pollutant signatures (e.g., heavy metals, essential vs. non-essential elements).
- Integrate with additional datasets through sample codes to contextualize environmental exposure.