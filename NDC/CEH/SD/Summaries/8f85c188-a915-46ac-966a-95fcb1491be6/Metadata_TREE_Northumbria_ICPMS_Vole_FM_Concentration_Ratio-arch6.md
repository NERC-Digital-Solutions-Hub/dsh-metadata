# TREE_Northumbria_ICPMS_Vole_FM_Concentration_Ratio

## Overview
- Dataset capturing concentration ratios of metals in vole tissue relative to soil dry mass, used for environmental/biogeochemical insights.
- Concentration ratio defined as Fresh Mass Vole (whole body) divided By Dry Mass Soil.
- Includes species metadata (Latin and common names), sampling site, date, CEH sample identifiers/descriptions, and Notes.
- Primary derived variables are element-specific concentration ratios (e.g., Be_Concentration_Ratio, Li_Concentration_Ratio, Na_Concentration_Ratio, etc.) for a wide range of elements.

## Data structure and fields
- Latin_Species_Name, Common_Species_Name: species identifiers.
- Site, Date_Sample_Collected: sampling details.
- CEH_Sample_Code, CEH_Sample_Description: laboratory/sample metadata.
- Notes: sampling notes.
- Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: soil sampling location used for the ratio calculation.
- I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio: concentration ratios for each element.
- Many entries indicate “Concentration Ratio (Fresh Mass Vole (wholebody) divided By Dry Mass Soil)” in their explanations; units are shown as n/a.
- Some columns show less-than markers (e.g., <Be, <Ni, <U) indicating threshold values for those concentrations.
- Note: several column names contain formatting inconsistencies or typographical irregularities.

## Derived metrics
- Concentration Ratios across multiple elements enable cross-sample comparisons, ecological interpretation, and potential correlations with soil metal content or site/date/species factors.

## Data quality and considerations
- Units are n/a; ratios are dimensionless.
- Some column names and markers appear inconsistently formatted, and there are typographical irregularities.
- Presence of less-than markers (<Be, <Ni, <U) requires careful numeric handling during ingestion.
- Data may be patchy across metals or samples; consistent ingestion from multiple sources may be needed.
- Metadata fields (CEH_Sample_Code, CEH_Sample_Description) enhance traceability and QA.

## How this supports data use
- Supports self-serve exploration of metal uptake patterns in voles across sites, dates, and species.
- Facilitates comparisons of species-specific accumulation and potential links to soil metal content or environmental factors.

## Outputs and visualizations
- Dashboards/pivot tables for:
  - Concentration ratios by metal across samples.
  - Site-based comparisons for key metals.
  - Temporal trends by date collected and species.
  - Ratios in relation to co-located soil sample context.

## Data governance and access
- Rich metadata (sample codes, descriptions, locations) supports reproducibility and traceability.
- Clear definition of the primary derived variable (Concentration Ratio) ensures consistent interpretation.

## Practical recommendations for data support
- Cleanse data: standardize column names, fix typographical irregularities, and properly handle less-than markers.
- Enforce numeric data types for all ratio columns; flag non-numeric entries.
- Validate Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio against related soil datasets.
- Document any deviations or missing values; maintain dataset versioning and provenance.