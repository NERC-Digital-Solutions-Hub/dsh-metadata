# TREE_Northumbria_ICPMS_Toad_FM_Concentration_Ratio

## Overview
- A dataset describing toad (fresh mass) concentration ratios relative to soil (dry mass) for a suite of elements, alongside sample and site metadata.
- Includes taxonomic names, sampling site and date, CEH sample identifiers, preparation notes, and the soil sample used to calculate the concentration ratios.

## Key Fields and Data Structure
- Taxonomy and naming
  - Latin_Species_Name
  - Common_Species_Name
- Site and sampling details
  - Site
  - Date_Sample_Collected
- Sample identifiers and descriptions
  - CEH_Sample_Code
  - CEH_Sample_Description
- Preparation and notes
  - Notes (about preparation of toads)
- Soil context for calculations
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio variables (toad fresh mass divided by dry soil mass)
  - I_Concentration_Ratio
  - Li_Concentration_Ratio
  - Be_Concentration_Ratio
  - Na_Concentration_Ratio
  - Mg_Concentration_Ratio
  - Al_Concentration_Ratio
  - P_Concentration_Ratio
  - K_Concentration_Ratio
  - Ca_Concentration_Ratio
  - Ti_Concentration_Ratio
  - V_Concentration_Ratio
  - Cr_Concentration_Ratio
  - Mn_Concentration_Ratio
  - Fe_Concentration_Ratio
  - Co_Concentration_Ratio
  - Ni_Concentration_Ratio
  - Cu_Concentration_Ratio
  - Zn_Concentration_Ratio
  - As_Concentration_Ratio
  - Se_Concentration_Ratio
  - Rb_Concentration_Ratio
  - Sr_Concentration_Ratio
  - Mo_Concentration_Ratio
  - Ag_Concentration_Ratio
  - Cd_Concentration_Ratio
  - Cs_Concentration_Ratio
  - Ba_Concentration_Ratio
  - Tl_Concentration_Ratio
  - Pb_Concentration_Ratio
  - U_Concentration_Ratio
- Note on units
  - All Units = n/a (these are ratios)

## Data Semantics and Concentration Ratios
- Each element-specific field (e.g., I_Concentration_Ratio, Li_Concentration_Ratio, etc.) represents the ratio: Fresh Mass Toad (whole body) divided by Dry Mass Soil.
- This dataset pairs biological measurements with an environmental context (co-located soil) to enable assessment of element transfer/accumulation.

## Data Quality and Preparation Considerations
- Field name and description inconsistencies are present (e.g., minor typographical issues in Fe and Tl descriptions), so standardization may be needed.
- Units are listed as n/a; interpret as dimensionless concentration ratios, but verify measurement conventions used during ICPMS processing.
- Some formatting irregularities (e.g., Tl_Concentration_Ratio_, descriptive text) may require cleaning before integration with other datasets.
- If merging with other data, ensure consistent keys (e.g., CEH_Sample_Code) and harmonize date formats (Date_Sample_Collected).

## Potential Uses for Data Support Outputs
- Build self-serve dashboards showing per-site or per-species concentration ratios across elements.
- Create cross-element summaries to identify elements with unusually high transfer ratios.
- Link with site metadata to analyze spatial patterns of element transfer.
- Validate and quality-check inputs by cross-referencing CEH_Sample_Code and soil sample descriptors.
- Promote reproducibility by documenting data cleaning steps and any Standard Operating Procedures used for preparation notes.