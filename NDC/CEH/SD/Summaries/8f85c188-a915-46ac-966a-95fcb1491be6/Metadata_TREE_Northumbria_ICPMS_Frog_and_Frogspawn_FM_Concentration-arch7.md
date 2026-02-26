# TREE_Northumbria_ICPMS_Frog_and_Frogspawn_FM_Concentration

## Overview
- A tabular dataset of ICP-MS concentration measurements in frog and frogspawn tissue from Northumbria, expressed as mg/kg of fresh mass (FM).
- Includes biological and sampling context: Latin and common species names, sampling site, date of collection, UKCEH sample codes and descriptions, tissue type, and the Fresh Mass / Dry Mass ratio.
- Provides a comprehensive suite of element concentrations (e.g., I, Li, Be, Na, Mg, Al, P, K, Ca/Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) with corresponding units and explanations.
- Some concentration values are recorded as less-than (<) values to indicate upper bounds.

## Key fields and meaning
- Species and identification
  - Latin_Species_Name, Common_Species_Name
- Sampling context
  - Site, Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue (frog tissue or frogspawn)
  - Fresh_Mass_Dry_Mass_Ratio
- Element concentrations (mg/kg FM)
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM
  - Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM
  - As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Note on data values
  - Some columns include less-than markers (e.g., <Be, <Al, <Ni, <Se, <U, <Ba), indicating upper-bound concentrations.

## Data structure and format
- Structure: tabular/content fields with Units = mg/kg_FM and Explanation for each concentration column.
- Coverage: broad panel of elements measured via ICP-MS, typical for ecological contaminant assessments in amphibians.
- Data quality considerations: header shows some inconsistencies in a few explanatory notes (e.g., some lines incorrectly refer to other elements); overall intent is mg/kg fresh mass across a wide range of elements.

## GIS and mapping applications
- Spatial analysis
  - Join by Site to geographic site polygons to create choropleth or symbol maps of element concentrations.
  - Visualize spatial distribution of contaminants across sampling locations.
- Temporal analysis
  - Use Date_Sample_Collected to construct timeSeries maps or animated maps showing changes over time.
- Taxon and tissue differentiation
  - Break down by Latin_Species_Name/Common_Species_Name and by Tissue to compare concentrations across species and tissue types.
- Data integration
  - Link CEH_Sample_Codes with lab records for QA, provenance, and metadata.
- Handling < values
  - Treat as upper bounds in maps; consider censored-data approaches or separate symbol categories to reflect uncertainty.

## Data quality, standards, and preparation
- Data are collected from multiple sources and may lack consistent standards across fields.
- Requires cleaning and transformation to standardize species names, sites, date formats, and units.
- The dataset may be large and complex; plan for data reduction or chunking for efficient GIS processing.
- Ensure alignment of site geolocations with the sampling coordinates before mapping.

## Practical considerations for use
- Align with audience needs (policy colleagues, clients, or public) by producing clear map-based visuals that show contamination patterns by site, species, and date.
- Use explicit documentation of less-than values to communicate detection limits and uncertainty in visualizations.
- Verify and cross-reference CEH_Sample_Codes with UKCEH records for traceability and data provenance.