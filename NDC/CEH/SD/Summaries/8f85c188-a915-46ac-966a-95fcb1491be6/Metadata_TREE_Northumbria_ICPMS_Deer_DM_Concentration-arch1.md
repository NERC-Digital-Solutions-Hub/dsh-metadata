# TREE_Northumbria_ICPMS_Deer_DM_Concentration

## Overview
- This appears to be a metadata and data dictionary for a dataset of ICP-MS measured element concentrations in deer tissue, on a dry mass basis, from Northumbria.
- Includes both sample metadata (species, site, date, sample codes, tissue, mass ratios) and a wide range of elemental concentrations.
- Lists concentrations for numerous elements with units and explanatory notes, plus indications of missing data and detection-limit markers.

## Dataset Structure and Key Variables
- Latin_Species_Name: Latin name of species.
- Common_Species_Name: Common name of species.
- Site: Sampling site.
- Date_Sample_Collected: Date the sample was collected.
- CEH_Sample_Codes: UKCEH sample codes.
- CEH_Sample_Description: UKCEH sample descriptions.
- Tissue: Deer tissue sampled.
- Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to dry mass.
- I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM: Concentrations of each element in mg/kg dry mass.
- Notes appear that some data are missing for Roe deer 4 thyroid across multiple elements.

## Measurement Details and Annotations
- All element concentrations are reported in mg/kg dry mass.
- Some entries are marked with a less-than sign (e.g., <Be, <Al, etc.) indicating concentrations reported as below detection limits.
- The entry "No data for Roe deer 4 thyroid" indicates missing data for Roe deer 4 thyroid in several columns.
- Some formatting in the text includes duplicate or fragmented explanations (e.g., repeated "Units = mg/kg" and "Explanation = Concentration of X in milligram per kilogram dry mass"), reflecting a metadata table structure.

## Data Quality and Limitations
- Missing data for Roe deer 4 thyroid across multiple elements could affect analyses involving that specific individual.
- Below-detection values require appropriate handling (censoring) in analyses.
- The text shows some formatting inconsistencies and potential data standardization issues (e.g., repeated explanations, minor punctuation issues) that may need cleaning before analysis.

## Use Cases and Analytical Opportunities
- Compare elemental concentrations by species, site, date, and tissue type.
- Explore correlations and potential exposure patterns across multiple elements.
- Assess environmental or ecological contamination signals using the dry-mass concentration data.
- Develop handling strategies for censored data due to detection-limit entries.