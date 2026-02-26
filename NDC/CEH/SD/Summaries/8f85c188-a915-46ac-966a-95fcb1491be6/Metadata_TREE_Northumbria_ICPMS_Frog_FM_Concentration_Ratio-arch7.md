# TREE_Northumbria_ICPMS_Bee_FM_Concentration_Ratio

## Overview
- A dataset of ICP-MS concentration ratios for bees, calculated as the Fresh Mass Bee (whole body) concentration divided by the Dry Mass Soil concentration.
- Captures taxonomic (Latin and common species names), sampling context (site, date collected), and sample metadata (CEH codes, sample details, descriptions, notes).
- Includes a field linking to the co-located soil sample used to calculate each concentration ratio, enabling integrated bee–soil analyses.

## Data structure and key fields
- Species and sampling context
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
- Sample metadata
  - CEH_Sample_Codes
  - Sample_Details
  - CEH_Sample_Description
  - Notes
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio columns (I and elemental metals)
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
- Note on special cases
  - Some "<" marker fields (e.g., <Be, <Se, <U) indicate concentration ratio values reported as less-than thresholds.
  - Some elements have dual fields or markers (e.g., 1/2 suffixes) reflecting specific data representations (e.g., lower/upper bounds or categorical qualifiers); interpret accordingly during data processing.

## Spatial relevance and GIS applications
- Site-level data supports spatial mapping of bee–soil metal uptake across sampling locations.
- Enables creation of map-based visualizations by species, date, and metal concentration ratio.
- Facilitates spatial analyses alongside other GIS layers (pollution sources, land use, soil maps).

## Data quality, cleaning and preparation
- Goals align with GIS needs: verify data accuracy, harmonize units (noted as n/a in this dataset), and transform for map-ready formats.
- Important steps
  - Link sites to geographic coordinates or GIS layers.
  - Resolve missing values and handle less-than entries appropriately.
  - Standardize naming conventions across species, sites, and samples.
  - Manage large/complex datasets by modular extraction and chunked processing.
  - Maintain traceability to the co-located soil samples used for ratio calculations.

## Challenges and considerations for use
- Data are distributed across multiple sources and may lack consistent data standards.
- Units are not explicitly defined in the headers (Units = n/a), requiring careful interpretation during analysis.
- Large or complex datasets may require packaging into manageable chunks for efficient GIS processing.
- Some concentration values use less-than markers or dual fields; plan for threshold handling and field mapping.

## End-use and audiences
- Designed for GIS analysts and policy-oriented users to understand and explore spatial patterns of contaminant transfer from soil to bees.
- Suitable for map-based visualizations and spatial decision-support for policy colleagues, clients, and the public.