# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration

## Overview
- ICPMS concentration dataset for wood mice tissues (fresh mass basis) from Northumbria/UK CEH sampling.
- Includes taxonomic names, sampling site, date, UKCEH sample codes, and tissue type.
- Contains concentrations for a wide range of elements (in mg/kg FM), with notes on less-than values and data gaps.
- Some data points missing or not measured for certain tissues (e.g., Hind Leg Bone; woodmouse 8 liver; tissue containing thyroid for several elements).

## Data Structure and Key Variables
- Taxonomy
  - Latin_Species_Name
  - Common_Species_Name
- Spatial/Temporal
  - Site
  - Date_Sample_Collected
- Sampling metadata
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Tissue
  - Fresh_Mass_Dry_Mass_Ratio
- Concentration measurements (mg/kg FM)
  - I_mg_kg_FM
  - Li_mg_kg_FM
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
- Data quality/notation
  - <I, <Al, <V, <Cr, <Ni, <Sr, <Mo, <Ag, <As, <Ba, <U and similar marks indicate less-than values
  - Some notes indicate “No data for Tissue containing thyroid” for several elements
  - Footnotes hint at data formatting (e.g., “1 = ., 2 = fresh mass”) which may require clarification

## Spatial Context and GIS Readiness
- Site serves as a spatial key for mapping; potential to attach geographic coordinates or a site polygon layer.
- Data can be visualized by site and by tissue, enabling map-based exploration of element distribution across locations.
- Requires standardization of site identifiers and linking to a GIS-ready spatial layer for true map visualization.

## Data Quality, Gaps, and Standards
- Notable data gaps: missing data for Hind Leg Bone and woodmouse 8 liver; tissue-containing thyroid data not available for many elements.
- Several elements have “less-than” values needing treatment in GIS analyses.
- Documentation of units (mg/kg FM) and tissue types exists, but some parts of metadata are fragmented (e.g., notes about fresh mass vs. dry mass ratio) and may need cleaning for consistent GIS use.

## Practical GIS Workflows
- Preparation
  - Standardize and harmonize Site names with spatial coordinates.
  - Convert to a long-form structure if needed (one row per site-tissue-element combination) for easy mapping.
  - Ensure units are consistently mg/kg FM across all measurements.
  - Resolve or flag less-than values appropriately (e.g., keep as a separate detection-limit flag or apply a consistent substitution rule).
- Visualization
  - Create choropleth maps of individual elements by site, facet by Tissue.
  - Build multi-layer visuals: site-level concentrations, tissue-specific concentration panels.
  - Use temporal dimension (Date_Sample_Collected) for time-series or trend analyses if multiple dates exist.
- Data Quality Handling
  - Mark missing data clearly and exclude from certain analyses as needed.
  - Document any assumptions made to handle less-than values or thyroid-related data gaps.
- Integration
  - Potentially join with other GIS layers (habitat, species distribution, i.e., Wood mice) or environmental layers for contextual mapping.

## Visualization and Analysis Considerations
- Focus on spatial patterns across sites and tissues for multiple elements.
- Compare metal concentrations across tissues within the same site or across sites for the same tissue.
- Clearly communicate detection limits and data gaps in any map legends or metadata.

## Summary for GIS Producers
- This dataset provides rich, site- and tissue-level ICPMS concentration data for wood mice, suitable for map-based analyses once standardized.
- Key tasks to enable GIS use include data cleaning, standardizing site identifiers to spatial coordinates, handling less-than values, and aligning tissue types.
- Intended GIS outputs include site-by-site concentration maps, tissue-specific visualizations, and cross-element spatial comparisons, with clear documentation of data limitations and missing values.