# TREE_Northumbria_ICPMS_Vegetation_FM_Concentration_Ratio

## Overview
- Dataset focused on vegetation samples analyzed by ICPMS to compute concentration ratios.
- Captures both plant and soil context to support uptake assessments (Concentration Ratio = Fresh Mass Vegetation divided By Dry Mass Soil).
- Includes sample identifiers, descriptive notes, and links to co-located soil samples used for ratio calculations.

## Key Fields and Structure
- Species and site metadata
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
- Sample identifiers and descriptions
  - CEH_Sample_Identifier
  - CEH_Sample_Description
  - Notes (about preparation of vegetation)
- Soil linkage
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration Ratio fields (for multiple elements)
  - Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
  - Some columns include markers indicating a less-than value (e.g., <I_Concentration_Ratio, <Li_Concentration_Ratio, etc.), with explanations provided in corresponding fields.
  - Each Concentration_Ratio is defined as the ratio of Fresh Mass Vegetation to Dry Mass Soil.

## Data Structure and Calculation Details
- Concentration Ratio definition: Fresh Mass Vegetation divided By Dry Mass Soil.
- Markers such as <I, <Li, <Be, etc. denote that the corresponding concentration ratio is a 'less than' value, as indicated in the related marker column.
- Column explanations emphasize that units are typically not required (Units = n/a) and that some rows/columns include notes like n/a or special markers.

## Metadata and Preparation Notes
- CEH_Sample_Description provides context for the sample.
- Notes document preparation steps for vegetation samples, aiding reproducibility and data quality.
- The dataset includes a field describing the co-located soil sample used to calculate each concentration ratio.

## Data Use and Stakeholders
- Enables analysis of element uptake across plant species and sampling sites.
- Supports comparative studies of vegetation-to-soil element ratios over time and space.
- Provides structured metadata to improve discoverability, interpretation, and reuse of concentration-ratio data.

## Data Quality and Discovery Considerations
- Metadata captures essential provenance: species names, site, collection date, sample identifiers, and preparation notes.
- Some fields use n/a or less-than markers, requiring careful interpretation during analysis.
- The presence of a linked co-located soil sample supports traceability for concentration-ratio calculations.