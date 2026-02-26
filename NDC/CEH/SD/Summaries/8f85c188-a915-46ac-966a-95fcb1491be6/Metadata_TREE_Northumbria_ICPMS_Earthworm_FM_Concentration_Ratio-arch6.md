# TREE_Northumbria_ICPMS_Earthworm_FM_Concentration_Ratio

## Overview
- Dataset describing concentration ratios of various elements in earthworms (fresh mass, whole body) to the dry mass of soil.
- Based on Northumbria ICP-MS earthworm sampling data.
- Includes both earthworm sample metadata and the co-located soil sample used to calculate each concentration ratio.

## Key fields and structure
- Taxonomy and identification
  - Latin_Species_Name
  - Common_Species_Name
- Sampling metadata
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Notes
- Co-located soil context
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio variables (created for each element)
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
- Calculation/definition
  - Concentration ratios are defined as Fresh Mass Earthworm (whole body) divided by Dry Mass Soil.
- Notes on data formatting
  - Most fields list Units as n/a.
  - Some header lines show formatting inconsistencies or typographical quirks (e.g., Tl_Concentration_Ratio_, Fe_Concentration_Ratio entries) which may require harmonisation during integration.

## Data quality and formatting considerations
- Data may be patchy or come in a mix of formats, reflecting diverse data sources or collection efforts.
- Some column names and descriptions contain typographical irregularities that should be cleaned before analysis.
- Alignment between earthworm samples, site, date, CEH codes, and the corresponding co-located soil sample is essential for correct concentration-ratio calculation.

## How to use
- Build dashboards or reports to compare metal uptake (concentration ratios) across species, sites, or collection dates.
- Use the co-located soil data to contextualise earthworm uptake and assess soil-to-biomass transfer patterns.
- Validate and harmonise field names and units to enable self-serve data exploration.

## Data governance and preparation guidance
- Verify mapping between CEH_Sample_Codes and CEH_Sample_Description for traceability.
- Ensure consistent handling of the multiple U_Concentration_Ratio entries (if there are variant definitions or duplications).
- Standardise units and field names where necessary to avoid misinterpretation in downstream analyses.
- Consider data quality flags or notes in Notes to capture any limitations related to sampling dates, site conditions, or data completeness.