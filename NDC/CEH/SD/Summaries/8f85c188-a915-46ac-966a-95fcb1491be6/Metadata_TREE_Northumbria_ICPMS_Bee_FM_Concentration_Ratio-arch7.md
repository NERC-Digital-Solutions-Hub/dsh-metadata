# TREE_Northumbria_ICPMS_Bee_FM_Concentration_Ratio

## Overview
- Metadata and field definitions for a dataset of ICP-MS concentration ratios in bees relative to dry mass soil.
- Captures species information, sampling context, and site-level details to enable map-based visualization of elemental contamination patterns.
- Includes a comprehensive set of concentration ratio fields for numerous elements, along with notes on measurement qualifiers (e.g., less-than values).

## Dataset scope and key concepts
- Focuses on bees collected at Northumbria with associated soil samples used to calculate concentration ratios.
- Links biological data (bee species) with sampling context (site, date, sampling codes) and analytical outputs (concentration ratios).
- Ready for GIS applications to explore spatial distribution and species-level patterns of element uptake.

## Key fields and structure (highlights)
- Taxonomy and identification
  - Latin_Species_Name: Latin name of species
  - Common_Species_Name: Common name of species
- Sampling and site context
  - Site: Sampling site
  - Date_Sample_Collected: Date of collection
  - CEH_Sample_Codes: CEH sample identifiers
  - Sample_Details: Sample preparation details
  - CEH_Sample_Description: CEH sample description
  - Notes: Notes related to the bee sample
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: Description of soil sample used for the ratio
- Concentration ratio fields (elemental)
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
  - Notes on special markers: Some columns use a less-than marker (e.g., <Be, <Se, <U) to denote that the reported ratio is an upper bound or below detection/thresholds.
  - The concentration ratios are based on Fresh Mass Bee (whole body) concentration divided by Dry Mass Soil, and are unitless.

## Data quality and interpretation cues
- Field explanations emphasize that many entries have “n/a” units because the ratios themselves are dimensionless.
- Explanations explicitly tie each ratio to the corresponding element and the described calculation.
- The presence of less-than indicators signals detection limits and data curation considerations for GIS analysis.

## GIS usage guidance
- Suitable for creating spatial visualizations of biotic uptake relative to soil concentrations across sampling sites.
- Recommend joining by Site and CEH_Sample_Codes, then linking to geographic coordinates for mapping.
- Use element-specific symbology (e.g., graduated colors or proportional symbols) to depict concentration ratios.
- Handle less-than values as censored data (e.g., treat as upper bounds or apply appropriate symbology/flags).
- Taxonomic fields enable species-based facet mapping and comparative analyses across bee species.

## Practical considerations for analysts
- Data integration: Ensure consistent site identifiers and sampling dates to enable robust spatial analyses.
- Data completeness: Be aware of potential gaps where some concentration ratios or metadata may be missing.
- Temporal context: Date_Sample_Collected allows trend analyses if multiple sampling events exist.
- Data provenance: CEH_Sample_Codes and Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio support traceability of calculations.