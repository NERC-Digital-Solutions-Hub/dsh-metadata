# TREE_Northumbria_ICPMS_Woodmice_mg_per_tissue_FM_Concentration

## Overview
- A dataset of ICP-MS concentration measurements (milligrams per total tissue, fresh mass) for multiple elements in wood mice tissues.
- Includes sample metadata (species names, site, collection date, UKCEH sample codes and descriptions) to support map-based visualization and spatial analysis.
- Designed to support GIS-driven exploration of elemental accumulation across sampling sites.

## Data Structure and Fields
- Species and sample identifiers
  - Latin_Species_Name, Common_Species_Name
  - Site, Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue (name of the sampled wood mouse tissue)
- Concentration measurements (per tissue, FM)
  - I_mg_per_tissue_FM, Li_mg_per_tissue_FM, Na_mg_per_tissue_FM, Al_mg_per_tissue_FM, P_mg_per_tissue_FM, K_mg_per_tissue_FM, Ca_mg_per_tissue_FM
  - Ti_mg_per_tissue_FM, V_mg_per_tissue_FM, Cr_mg_per_tissue_FM, Mn_mg_per_tissue_FM, Fe_mg_per_tissue_FM, Co_mg_per_tissue_FM
  - Ni_mg_per_tissue_FM, Cu_mg_per_tissue_FM, Zn_mg_per_tissue_FM, As_mg_per_tissue_FM, Se_mg_per_tissue_FM
  - Rb_mg_per_tissue_FM, Sr_mg_per_tissue_FM, Mo_mg_per_tissue_FM, Ag_mg_per_tissue_FM, Cd_mg_per_tissue_FM
  - Cs_mg_per_tissue_FM, Ba_mg_per_tissue_FM, Tl_mg_per_tissue_FM, Pb_mg_per_tissue_FM, U_mg_per_tissue_FM
- Data qualifiers and notes
  - Some values are denoted with a "<" marker (e.g., <I, <Al, <V, <Cr, <Ni, <Mo, <Ag, <Pb, <Ba, <U) indicating a “less than” detection threshold for the corresponding concentration column.
  - Explanations indicate that columns represent concentrations in total wood mouse tissue (fresh mass).
  - Some tissues or samples have no data (e.g., Hind Leg Bone and woodmice 8 liver; thyroid data noted as not collected in several instances).

## Spatial and Temporal Scope
- Site-based sampling within Northumbria (data structured to support linking to GIS site polygons or point locations).
- Date_Sample_Collected provides temporal context for mapping and temporal analyses.

## Data Quality, Standards and Gaps
- Data quality notes
  - Inconsistent data coverage across tissues and elements; several entries marked as “No data collected” for particular tissues (e.g., hind leg bone, thyroid for some woodmice).
  - Some fields carry minimal or placeholder units (n/a) and mixed explanatory text, implying a need for harmonization before large-scale GIS use.
- Standardization considerations
  - Several field names and descriptions use abbreviated or concatenated forms; there may be ambiguity in units and casing.
  - Handling of less-than values requires a consistent approach in GIS workflows (e.g., censoring or bounding).
- Gaps to address for robust GIS use
  - Missing tissue data reduces the ability to compare across sites for certain elements.
  - Missing date or site-level metadata in some records could limit spatial-temporal analyses.

## GIS Use and Best Practices
- Mapping approach
  - Join this dataset to site-level shapefiles or point features to create spatial layers by tissue or by element.
  - Create per-element choropleth or heatmap layers, with separate layers for different tissues to preserve biological context.
- Handling non-detects and missing data
  - Treat "<" values as censored data; decide on a reporting convention (e.g., use the threshold as a lower bound, or impute).
  - Clearly flag records with “No data” for specific tissue-element combinations to avoid misinterpretation.
- Temporal analysis
  - If Date_Sample_Collected is available, build time-enabled maps or animations to show changes in concentrations over time.
- Data integration considerations
  - Ensure consistent tissue naming and alignment of Site identifiers with GIS spatial data.
  - Consider data cleaning to harmonize units and resolve n/a fields before publishing or sharing.

## Use Cases
- Environmental monitoring and bioindicator studies in the Northumbria region using wood mice tissue concentrations.
- Spatial pattern analysis of multi-element accumulation across sampling sites to identify contamination hotspots or ecological risk areas.
- Comparative analyses across tissues and elements to understand tissue-specific uptake dynamics and metal exposure.

## Notes for Analysts
- Review and harmonize units and field descriptions prior to GIS publication.
- Develop a clear policy for handling left-censored ("<") data and for documenting any imputed values.
- Document any missing tissue data and provide guidance on how this affects comparative spatial analyses.