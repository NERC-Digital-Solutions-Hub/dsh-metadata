# TREE_Northumbria_ICPMS_Vegetation_FM_Concentration_Ratio

## Overview
- Defines a dataset schema for ICP-MS concentration ratios derived from vegetation samples around Northumbria, enabling standardized environmental health monitoring over time.
- Core metric: Concentration Ratio = Fresh Mass Vegetation divided by Dry Mass Soil, used to assess element uptake by vegetation relative to soil.

## Data Structure and Key Fields
- Taxonomy and identifiers
  - Latin_Species_Name, Common_Species_Name: scientific and common names of plant species.
  - Site: sampling location.
  - Date_Sample_Collected: date of sample collection.
  - CEH_Sample_Identifier, CEH_Sample_Description: CEH sample codes and descriptions.
  - Notes: notes about preparation of vegetation.
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: description of the soil sample linked to the vegetation sample for ratio calculation.
- Concentration Ratio fields
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio.
  - Each ratio is defined as the Concentration Ratio (Fresh Mass Vegetation divided By Dry Mass Soil).
  - Some entries use a less-than marker (e.g., "<I") to indicate censored values; corresponding notes explain how to interpret these markers.
  - Certain elements have variant columns labeled with additional notation (e.g., suffixes like ", 2" or references to related concentration ratios), indicating alternative or censored forms for specific entries.
- Data quality and provenance indicators
  - Columns include markers for less-than values to denote censored data.
  - Unit information for many fields is not specified (n/a), reflecting the dataset’s focus on ratio values rather than absolute units.

## Calculation and Semantics
- Calculation basis: Concentration Ratio = Fresh Mass of Vegetation / Dry Mass of Soil for each listed element.
- Handling of censored data: less-than markers in certain concentration ratio fields indicate upper-bound values; metadata provides guidance on interpretation.

## Metadata, Provenance, and Preparation
- Sample provenance linked through CEH_Sample_Identifier and Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio to ensure traceability between vegetation and soil samples.
- Date and site information support temporal and spatial analyses across monitoring programs.
- Notes field captures preparation details relevant for reproducibility.

## Use in Monitoring and Policy
- Supports consistent, time-series evaluation of environmental health by enabling cross-site and cross-year comparisons of vegetation uptake relative to soil.
- Standardized outputs (via this schema) facilitate reporting and scrutiny of policy performance and ecosystem health.
- Enables integration with other environmental datasets to increase the value of monitoring datasets.

## Challenges and Opportunities
- Increasing the value of datasets by combining vegetation-to-soil concentration ratios with additional environmental data (soil properties, climate, land use) rather than treating them as single-use.
- Ensuring broad access to underlying data used to generate final outputs, promoting transparency and reuse across analyses and stakeholders.