# TREE_Northumbria_ICPMS_Frog_and_Frogspawn_FM_Concentration

## Overview
- A data dictionary for a dataset of elemental concentrations measured by ICP-MS in frog tissue or frogspawn from Northumbria.
- Metadata fields describe species, sampling site, collection date, UKCEH sample codes, and tissue type.
- Core measurements cover a wide panel of elements (I, Li, Be, Na, Mg, Al, P, K, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) expressed as concentrations per fresh mass (FM), typically mg/kg FM.
- The dataset includes a Fresh Mass to Dry Mass ratio to contextualize concentration values.
- Some columns indicate “less than” values (e.g., <Be, <Al, <Ni, <Se, <U), signaling censored/upper-bound measurements.

## Data structure and fields
- Metadata
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Tissue (frog tissue or frogspawn)
  - Fresh_Mass_Dry_Mass_Ratio
- Measurements (concentrations in mg/kg FM)
  - I_mg_kg_FM
  - Li_mg_kg_FM
  - Be_mg_kg_FM (with potential <Be indicators)
  - Na_mg_kg_FM
  - Mg_mg_kg_FM
  - Al_mg_kg_FM (with potential <Al indicators)
  - P_mg_kg_FM
  - K_mg_kg_FM
  - Ti_mg_kg_FM
  - V_mg_kg_FM
  - Cr_mg_kg_FM
  - Mn_mg_kg_FM
  - Fe_mg_kg_FM
  - Co_mg_kg_FM
  - Ni_mg_kg_FM (with potential <Ni indicators)
  - Cu_mg_kg_FM
  - Zn_mg_kg_FM
  - As_mg_kg_FM
  - Se_mg_kg_FM (with potential <Se indicators)
  - Rb_mg_kg_FM
  - Mo_mg_kg_FM
  - Ag_mg_kg_FM (with potential <Ag indicators)
  - Cd_mg_kg_FM
  - Cs_mg_kg_FM
  - Ba_mg_kg_FM (with potential <Ba indicators)
  - Tl_mg_kg_FM
  - Pb_mg_kg_FM
  - U_mg_kg_FM (with potential <U indicators)

## Units and measurement notes
- Primary unit for all measured elements is milligrams per kilogram of fresh mass (mg/kg FM).
- Some columns include a less-than marker to denote upper-bound values (e.g., <Be, <Al, <Ni, <Se, <U, <Ag, etc.).
- Fresh_Mass_Dry_Mass_Ratio provides context for how concentrations relate to sample mass changes.

## Data quality and interpretation considerations
- Documentation inconsistencies: some explanations appear misaligned (e.g., certain “Concentration” descriptions do not match the listed element, indicating potential data dictionary errors).
- Presence of censored data: < marker values require special handling (e.g., substitution methods or survival analysis approaches) during analysis.
- Data may be patchy or inconsistently formatted across sites or samples, reflecting the broader challenge of integrating data from multiple sources.
- Ensure correct mapping between element symbols and their corresponding explanations, given potential mislabeling in the current text.

## Potential uses
- Environmental monitoring and risk assessment for frog populations by comparing elemental burdens across sites, dates, and tissue types.
- Baseline establishment for trace element concentrations in Northumbria’s amphibian fauna.
- Data visualization and self-serve reporting through dashboards or pivot-style summaries for end users (policy makers, researchers, public summaries).
- Data quality improvement and standardization efforts by correcting misalignments in the data dictionary and documenting handling for censored values.

## Practical considerations for data support
- Clarify and correct any misaligned field-explanation mappings before analysis.
- Develop a consistent handling strategy for < values (e.g., use of censoring methods or imputation where appropriate).
- Document data provenance (sampling sites, dates, codes) to facilitate reproducibility and cross-study comparisons.
- Liaise with topic experts to verify species-site context and ensure correct interpretation of tissue types and sampling methods.