# TREE_Northumbria_ICPMS_Bee_FM_Concentration_Ratio

## Overview
- Dataset describing concentration ratios of multiple elements in bee tissue relative to co-located soil, calculated as Fresh Mass Bee (whole body) concentration divided by Dry Mass Soil.
- Includes taxonomic, site, sampling, and sample-processing metadata (e.g., Latin/Common species names, site, date collected, CEH sample codes, sample details, descriptions, notes).
- Aims to support environmental health monitoring by providing standardized, comparable concentration-ratio outputs across sites and times.

## Dataset structure and key fields
- Taxonomy and name fields:
  - Latin_Species_Name, Common_Species_Name (explanations provided).
- Spatial and temporal metadata:
  - Site, Date_Sample_Collected.
- Sampling and processing identifiers:
  - CEH_Sample_Codes, Sample_Details, CEH_Sample_Description, Notes.
- Co-located data:
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio (description of soil sample used for the calculation).
- Concentration ratio fields (element-specific):
  - I_Concentration_Ratio (Iodine).
  - Be_Concentration_Ratio, Li_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio.
- Less-than indicators:
  - <Be_Concentration_Ratio, <Se_Concentration_Ratio, <U_Concentration_Ratio (used to denote a “less than” value for the corresponding concentration ratio).
- Data conventions:
  - Units are not specified (n/a); the concentration ratio is defined as competition between bee tissue and dry soil mass.

## Concentration ratio concept
- The Concentration Ratio for each element is defined as:
  - Fresh Mass Bee (whole body) concentration divided by Dry Mass Soil concentration.
- Some rows include less-than qualifiers to indicate upper-bound values for certain elements.

## Data quality and workflow
- Data are intended to be:
  - Verified against established data sources.
  - Quality assured, cleaned, and transformed to standard formats.
  - Analyzed using standardised methods to produce outputs (e.g., tables, maps, charts).
- Data management practices include:
  - Storing and uploading the final datasets to appropriate portals for accessibility and reuse.

## Intended use for environmental monitoring
- Enables assessment of environmental health and policy performance over time by comparing concentration ratios across sites and sampling periods.
- Supports cross-site comparisons and trend analysis for understanding metal transfer from soil to bee tissue.

## Challenges and data access
- Key challenges:
  - Increasing the value of datasets by integrating with additional relevant data sources (avoiding single-use datasets).
  - Facilitating access to the underlying data that informs the final concentration ratio outputs.