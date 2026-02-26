# TREE_Northumbria_ICPMS_Deer_FM_concentration

## Purpose and scope
- Document outlining ICP-MS concentration data for deer tissue (fresh mass) from Northumbria, with associated sampling metadata.
- Designed for map-based visualization and spatial analysis of elemental concentrations across sampling sites.
- Includes species identifiers, sampling details, tissue type, mass ratio, and a wide range of elemental concentrations.

## Dataset structure and key fields
- Taxonomy and identification
  - Latin_Species_Name (with explanation), Common_Species_Name (with explanation)
- Sampling metadata
  - Site, Date_Sample_Collected, CEH_Sample_Codes (UKCEH codes), CEH_Sample_Description
- Tissue and mass
  - Tissue, Fresh_Mass_Dry_Mass_Ratio
- Concentration measurements (concentrations in mg/kg fresh mass, FM)
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM
  - Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM
  - V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM
  - Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM
  - Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM
  - Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Non-detects and data notes
  - Some concentration values are reported as "<" (less than) values to indicate non-detects.
  - Repeated notes indicate no data for Roe deer 4 thyroid for multiple elements.

## Data quality, gaps, and consistency notes
- Non-detects are labeled with less-than markers for several elements.
- Specific data gap: No data for Roe deer 4 thyroid across numerous elements, indicating missing measurements for that sample.
- Dataset appears to be a data dictionary or schema excerpt with variable definitions and expected units; some formatting inconsistencies are present (e.g., repeated explanations and markers).

## GIS considerations and usage
- Suitable for creating map-based visualizations of spatial patterns in elemental concentrations in deer tissue.
- Requires harmonization of units (mg/kg FM is the standard for most elements) and resolution across samples.
- Users should account for missing Roe deer 4 thyroid data and handle non-detects appropriately in analyses and visualizations.
- Metadata (Site, Date_Sample_Collected, CEH codes) supports spatial joins and temporal analyses when integrated with GIS datasets.