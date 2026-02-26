# TREE_Northumbria_ICPMS_Bee_FM_Concentration_Ratio

## Overview
- A dataset detailing concentration ratios of multiple elements in bees (fresh mass concentration) relative to dry mass soil, used to understand uptake from soil.
- Captures both bee sample metadata and a large set of element-specific concentration ratio fields.
- Includes linkage to soil samples used to calculate each concentration ratio, enabling traceability of the calculation basis.

## Data Structure and Key Fields
- Sample and species metadata
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - Sample_Details
  - CEH_Sample_Description
  - Notes
- Calculation linkage
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Element concentration ratios (Bee fresh mass concentration / Dry mass soil)
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
- Special value indicators
  - Some columns may use a less-than marker (e.g., <Be, <Se, <U) to denote that the reported value is an upper bound rather than a precise ratio.
- Units
  - For many fields, Units = n/a; the primary focus is the ratio value rather than standardized units.

## Concentration Ratio Details
- Each element has a corresponding Concentration_Ratio column representing the ratio of Fresh Mass Bee (wholebody) concentration to Dry Mass Soil.
- Some elements use a dual-column or special marker (e.g., <Be) to indicate threshold values.
- The dataset explicitly ties each ratio to the soil sample used for its calculation, supporting reproducibility and auditability.

## Usage Scenarios for Data Support
- Build dashboards to compare concentration ratios across species, sites, and collection dates.
- Create pivot analyses to identify which elements show higher uptake in bees at particular sites or times.
- Cross-reference bee concentration ratios with soil sample data to explore relationships between soil metal content and bee exposure.
- Develop self-serve reports and visualizations for stakeholders (policy makers, environmental monitors) to inform monitoring and remediation strategies.

## Data Quality and Considerations
- Data may be patchy or variably formatted; watch for incomplete fields or missing units.
- The presence of less-than markers indicates upper-bound values rather than exact measurements, requiring careful interpretation.
- Clear provenance is provided via the soil sample used to calculate each concentration ratio, facilitating verification and reproducibility.

## Summary for Data Support Roles
- This dataset provides a structured, linkable schema for exploring bee uptake of multiple elements relative to surrounding soil, suitable for dashboards, reports, and data-driven insights.
- To maximize usefulness, focus on linking species/site/date metadata with element ratios, account for upper-bound values, and leverage the soil-sample linkage to contextualize findings.
- The data support workflow can benefit from clear definitions, consistent naming, and guidance on communicating complex ratio data to non-technical end users.