# TREE_Northumbria_ICPMS_Bee_DM_Concentration

## Overview
- A dataset of elemental concentration measurements (in mg/kg dry mass) in bee samples, with accompanying sample metadata.
- Concentrations cover a wide range of elements (e.g., I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) across numerous samples.
- Metadata fields describe species, sampling site, collection date, UK Centre for Ecology & Hydrology (UKCEH) sample codes, sample descriptions, and preparation details.

## Key fields and data types
- Metadata
  - Latin_Species_Name, Common_Species_Name: scientific and common names of species.
  - Site: sampling site.
  - Date_Samples_Collected: date of sampling.
  - CEH_Sample_Codes, CEH_Sample_Description: UKCEH-specific identifiers and descriptions.
  - Sample_Details: sample preparation details.
- Concentration measurements (all in mg/kg DM)
  - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM.
- Notes on special values
  - Columns prefixed with "<" (e.g., <Be, <Se, <U) indicate concentrations reported as a "less than" value (below detection/threshold).

## Data quality and considerations
- Data may be sourced from multiple records; ensure consistent data standards and harmonization.
- Some explanatory text contains minor errors (e.g., Al_mg_kg_DM explanation) and should be QA-ed.
- Handling of "<" values is required for proper analysis (e.g., censored data handling or substitution strategies).

## GIS applicability and use cases
- Spatial visualization: map concentrations by Site to identify geographic patterns in element uptake or exposure.
- Stratification by biological metadata: compare concentrations across Latin/Common species names and dates collected.
- Temporal analysis: if multiple dates exist, explore trends over time at sites.
- Correlative analyses: combine with habitat or land-use layers to assess environmental drivers of observed concentrations.
- Data integration: join with other GIS datasets (e.g., pollinator health metrics, soil/bee forage maps) for multi-layer analyses.

## Practical guidance for GIS analysts
- Import and align the dataset with spatial layers for Site-based mapping; ensure Site identifiers match your spatial joins.
- Normalize units if integrating with other datasets; confirm all concentrations are mg/kg DM.
- Address "<" values appropriately (consider censoring approaches or substituting with detection limits) to avoid bias in maps and summaries.
- Create derived fields as needed (e.g., total metal load per sample, mean concentration by site or species).
- Validate metadata accuracy (species names, site codes, and collection dates) to ensure reliable spatial analyses.

## Endnotes
- The document represents a comprehensive matrix of bee-related ICPMS concentrations alongside rich sampling metadata, enabling diverse GIS-driven analyses of spatial and temporal patterns in heavy metal uptake across sites and species.