# TREE_Northumbria_ICPMS_Woodmice_DM_Concentration

## Overview
- A dataset of ICP-MS measured concentrations of multiple elements in wood mice tissues, reported as mg/kg dry mass (DM).
- Includes sample metadata (species, site, date, UKCEH sample codes) and tissue/mass information to support GIS-based visualization of spatial patterns and tissue-specific accumulation.

## Data structure and key columns
- Species metadata
  - Latin_Species_Name: Latin name of the species
  - Common_Species_Name: Common name of the species
- Sampling metadata
  - Site: Sampling site
  - Date_Sample_Collected: Collection date
  - CEH_Sample_Codes: UKCEH sample codes
  - CEH_Sample_Description: UKCEH sample description
- Sample description and mass
  - Tissue: Name of tissue sampled
  - Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to dry mass
- Concentration measurements (mg/kg DM)
  - I_mg_kg_DM, Li_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM
  - Notes on data conventions
    - "<" markers indicate concentrations below the detection limit for that column
    - Some entries are marked as having no data (e.g., Hind Leg Bone, woodmouse 8 liver)
    - In several rows, tissue descriptions include “Tissue containing thyroid”
    - Certain elements may have multi-part or special notations (e.g., Sr, Mo, Ag, Ba) in specific contexts

## Data quality, gaps, and conventions
- Missing data
  - No data for Hind Leg Bone and woodmouse 8 liver
  - Some tissues or samples lack concentration values for one or more elements
- Detection limits
  - "<" notation used to indicate concentrations below detection limits for the corresponding element
- Tissue specifics
  - Some samples described as “Tissue containing thyroid” (affects interpretation of certain element concentrations)
- Data consistency
  - Concentrations are reported in mg/kg dry mass; ensure consistent DM basis when combining with other datasets
  - Some entries imply complex or multi-value notations for certain elements (e.g., Sr, Mo, Ag, Ba) that may require careful parsing

## GIS applicability and usage guidance
- Linkage and spatial joins
  - Use Site and CEH_Sample_Codes to join to GIS site-level shapefiles or point datasets
  - Date_Sample_Collected enables temporal analysis alongside location
- Visualization approaches
  - Map-based visuals per site: aggregate by site or by tissue type for choropleth or proportional symbol maps
  - Tissue-driven visuals: differentiate by Tissue to show organ-specific metal accumulation
  - Temporal visuals: explore changes over collection dates
- Data preparation for GIS
  - Standardize Tissue naming and ensure consistent units (mg/kg DM)
  - Parse and handle "<" values (e.g., imputation, censoring flags)
  - Create data quality flags for samples with missing data or special notes (e.g., thyroid tissue, Hind Leg Bone missing)
  - When aggregating, consider excluding samples with missing critical metadata or concentrations for key analyses

## Practical notes for analysts
- This dataset provides a comprehensive multi-element metal panel for wood mice with useful metadata to support spatial and tissue-specific analyses in GIS.
- Prioritize data cleaning around:
  - Handling below-detection (<) values
  - Interpreting tissue descriptors (e.g., thyroid-containing samples)
  - Managing known data gaps (e.g., Hind Leg Bone, woodmouse 8 liver)
- Ensure consistent join keys between the chemical concentrations and spatial layers to enable accurate mapping and querying.