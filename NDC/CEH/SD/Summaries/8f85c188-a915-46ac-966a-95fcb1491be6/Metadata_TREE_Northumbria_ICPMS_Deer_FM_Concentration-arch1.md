# TREE_Northumbria_ICPMS_Deer_FM_concentration

## Overview
- Data dictionary for ICP-MS concentrations of multiple elements in deer tissue, expressed as mg/kg fresh mass (FM).
- Includes species metadata, sampling details, and a broad panel of elemental concentrations.

## Data fields / structure
- Metadata and identifiers
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Tissue
  - Fresh_Mass_Dry_Mass_Ratio
- Element concentration columns (mg/kg FM)
  - I_mg_kg_FM
  - Li_mg_kg_FM
  - Be_mg_kg_FM (may include "<" values)
  - Na_mg_kg_FM
  - Mg_mg_kg_FM
  - Al_mg_kg_FM (may include "<" values)
  - P_mg_kg_FM
  - K_mg_kg_FM
  - Ca_mg_kg_FM
  - Ti_mg_kg_FM
  - V_mg_kg_FM
  - Cr_mg_kg_FM
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
- Notes on data entries
  - Some concentrations may be missing for specific rows (e.g., “No data for Roe deer 4 thyroid” appears for many elements).
  - Some columns contain less-than values indicated by a preceding "<" marker.

## Data quality / caveats
- Repeated notes of missing data for Roe deer 4 thyroid across numerous elements.
- Occasional formatting irregularities in column descriptions (e.g., stray characters), but the intent is a comprehensive multi-element concentration dataset.
- "<" markers indicate lower-than detection values rather than exact measurements.

## Potential analyses / usage
- Examine correlations between element concentrations and tissue type, site, or collection date.
- Compare element profiles across species or sites to identify environmental exposure patterns.
- Develop predictive models of metal/element exposure and potential ecological or health impacts.
- Integrate with other datasets (e.g., environmental measurements) to contextualize concentrations.