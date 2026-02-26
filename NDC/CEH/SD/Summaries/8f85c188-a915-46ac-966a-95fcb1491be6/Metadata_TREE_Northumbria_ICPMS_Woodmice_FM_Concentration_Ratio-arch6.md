# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

## Overview
- Dataset documenting element concentration ratios in woodmice (Fresh Mass Woodmice) divided by Dry Mass Soil.
- Captures sample metadata (species, site, collection date, sample description, notes) and the associated soil sample used to calculate the ratio.
- Designed to enable exploration of metal/element transfer from soil to woodmice and support data products for analysis and communication.

## Data Structure and Key Columns
- Latin_Species_Name, Common_Species_Name: scientific and common names of the woodmice species.
- Site: sampling location.
- Date_Sample_Collected: date when the woodmice sample was collected.
- CEH_Sample_Description, Notes: descriptions and notes related to the sample.
- Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: description of the soil sample paired with the woodmice sample for the ratio calculation.
- I_Concentration_Ratio: Concentration Ratio for I (Iodine) = Fresh Mass Woodmice divided by Dry Mass Soil.
- Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio: each represents the corresponding element’s concentration ratio (Fresh Mass Woodmice divided by Dry Mass Soil).
- For some elements, there are two columns (e.g., V_Concentration_Ratio and V_Concentration_Ratio, 2) indicating multiple related measurements or qualifiers.
- <I, <Be, <Ni, <Ag, <U markers: indicate that the associated concentration ratio value is a censored or “less than” value.
- Notes on units: All concentration ratios are unitless (n/a).

## Data Handling Notes
- Some columns use less-than markers to denote censored values (e.g., <I, <Be, <Ni, <Ag, <U).
- Certain elements have dual columns to capture different measurement contexts or replicates (e.g., V_Concentration_Ratio, 2).
- All data are presented as concentration ratios of fresh woodmice mass to dry soil mass; no physical units are attached (dimensionless).

## How to Use / Potential Outputs
- Create dashboards or pivot tables showing concentration ratios by site, date, and species.
- Compare element-specific bioaccumulation ratios across sites or over time.
- Join with Co_Located_Soil_Sample descriptions to provide context for each ratio calculation.
- Flag censored (<) values appropriately in analyses and visualizations to reflect data limitations.
- Use the data to identify elements with notably high or low transfer from soil to woodmice for ecological risk assessment or policy discussions.

## Data Integration Considerations
- When combining with soil context data, align by Site and Date_Sample_Collected to ensure accurate paired calculations.
- Handle missing values and censored data (less-than markers) in analysis pipelines.
- Maintain traceability to the specific soil sample used for each woodmice ratio via Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio.

## Data Support Considerations
- Time spent understanding the ask may be needed to identify appropriate site/date filters and the correct concentration-ratio columns.
- Data may exist in multiple formats or systems; plan for integration across sources.
- Communicate results clearly, especially for censored values and dual-column elements, to ensure interpretable outputs.
- Promote outputs to encourage reuse and consider collecting feedback for refining the data product.