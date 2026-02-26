# TREE_Northumbria_ICPMS_Earthworm_FM_Concentration

## Overview
- Dataset of earthworm tissue concentrations measured by ICP-MS, focused on Northumbria.
- Includes species information, sampling metadata, UKCEH sample codes, and multi-element concentration data (mg/kg fresh mass).

## Data Structure and Key Fields
- Taxonomy
  - Latin_Species_Name
  - Common_Species_Name
- Sampling metadata
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Notes
- Concentration measurements (all in mg/kg fresh mass, FM)
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
  - Cr_mg_kg_FM
  - Mn_mg_kg_FM
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
- Notes on units
  - Units for measurement fields: mg/kg FM
  - Some field metadata in the source appears mislabelled (e.g., incorrect “Explanation” text), indicating a need for data cleaning and metadata validation.

## Data Quality and Consistency
- Data may be stored in multiple locations; consolidation and provenance tracking required.
- Potential gaps or inconsistent resolutions across sites and dates.
- Metadata descriptions may contain copy errors; verify with original data source.
- Standardization needed for site identifiers, coordinates, and unit handling.

## GIS Applications
- Spatial distribution: map element concentrations across sampling sites to identify hotspots.
- Temporal analysis: track changes through Date_Sample_Collected where multiple time points exist.
- Species comparisons: examine differences in metal accumulation between Latin/Common species names.
- Data integration: join with site coordinates to create choropleth maps, heatmaps, or point-based symbol maps for each element.
- Multivariate visualization: parallel coordinate plots or bubble maps to compare multiple elements simultaneously.

## Preparation and Integration Guidance
- Align Site and CEH_Sample_Codes with precise coordinates and basemap layers.
- Validate and harmonize units (confirm all concentration fields use mg/kg FM).
- Clean metadata: correct mislabelled explanations and ensure consistent field naming.
- Handle missing values appropriately (e.g., imputation or exclusion based on analysis goals).
- Consider data normalization or standardization if combining with other datasets.

## Limitations and Considerations
- Possible variability in sampling resolution and timing across sites.
- Not all elements may be present or detectable at every site or sample.
- Metadata quality may require verification before GIS analyses.

## Additional Notes
- The dataset is designed to support map-based exploration of earthworm contaminant concentrations and related ecological interpretations, with emphasis on UKCEH sampling context.