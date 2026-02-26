# TREE_Northumbria_ICPMS_Bee_FM_Concentration

## Overview
- Dataset describing ICP-MS concentration of multiple elements in bee samples, enabling GIS-based mapping and spatial analysis of exposure across sampling sites and times.

## Key fields

- Taxonomy
  - Latin_Species_Name
  - Common_Species_Name

- Sampling and metadata
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Sample_Details
  - Notes

- Concentration measurements (all in mg/kg_fresh_mass)
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

- Special notations
  - Be_mg_kg_FM, Se_mg_kg_FM, U_mg_kg_FM may include “<” markers indicating concentrations reported as less-than values.

## Data context and definitions
- Units: Concentrations are reported as milligrams per kilogram of fresh mass (mg/kg_FM).
- Species and site information allow spatial linkage and species-specific analysis.
- CEH_Sample_Codes and CEH_Sample_Description provide UK Centre for Ecology & Hydrology sampling context.

## Practical GIS usage
- Join attributes to spatial features by Site and potentially Date_Sample_Collected.
- Map concentration patterns for individual elements or combine across elements for multi-pollutant exposure.
- Use Taxonomy fields to compare species-specific exposure, and Notes/Sample_Details for contextual interpretation.
- Handle less-than values appropriately in analyses (imputation or censoring) using Be_mg_kg_FM, Se_mg_kg_FM, and U_mg_kg_FM markers.