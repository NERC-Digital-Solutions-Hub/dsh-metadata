# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

## Overview
- Metadata and data dictionary for a dataset on ICP-MS concentration ratios in wood mice from Northumbria.
- Primary focus: concentration ratio defined as Fresh Mass Woodmice (wholebody) divided By Dry Mass Soil.
- Captures taxonomic identifiers, sampling context, and a wide range of element-specific concentration ratios.
- Includes indicators for special cases such as “less than” values.

## Data Structure and Key Fields
- Taxonomy and identification
  - Latin_Species_Name
  - Common_Species_Name
- Sampling context
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes
- Data provenance
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
  - I marker indicators for concentration ratio values (e.g., <I)
- Concentration ratio fields (for multiple elements)
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
  - Some elements have dual entries (e.g., V_Concentration_Ratio 1 and 2) or similar dual forms (Cr_Concentration_Ratio 1 and 2), indicating alternative measurements or representations.
  - Markers such as <I, <Be, <Ni, <U denote “less than” values for the corresponding concentration ratios.

## How to Use the Dataset
- Data preparation
  - Verify alignment of species, site, date, and soil reference for each wood mouse sample.
  - Normalize and harmonize any multiple-format fields (e.g., dual concentration ratio columns).
  - Flag and handle less-than values appropriately in analyses.
- Analysis and reporting
  - Compare concentration ratios across elements, sites, and sampling dates.
  - Create self-service outputs: dashboards, pivot tables, and charts to explore metal/metalloid uptake patterns.
  - Combine with soil data to assess bioconcentration or transfer factors using the defined ratio.
- Outputs and dissemination
  - Generate site-by-site summaries, element-focused heatmaps, or time-series views of key ratios.
  - Produce reports and visualizations with clear explanations of how ratios were calculated and any data caveats.

## Data Quality, Challenges, and Considerations
- Data quality
  - Data may be patchy and come in multiple formats, requiring careful cleaning and standardization.
  - Units are listed as not applicable (n/a); emphasis on the defined ratio calculation rather than physical units.
- Accessibility and integration
  - Data may reside in multiple systems; ensure access paths to the wood mice and co-located soil samples are consistent.
- Communication and interpretation
  - Some concentration ratio values may be represented as less-than values; ensure stakeholders understand how to interpret and use these in analyses.
- Output usage
  - There is a need to promote and share outputs more widely to encourage reuse and broader data impact.

## Practical Guidance for Data Support Roles
- Understand the ask
  - Confirm what comparisons or insights stakeholders need (elements of interest, sites, dates, or species).
- Data preparation and quality assurance
  - Clean and transform data into consistent formats; verify the co-located soil references.
  - Clearly document any less-than values and how they were handled in downstream analyses.
- Product development
  - Create intuitive dashboards and reports that enable self-service exploration of concentration ratios by site, date, and element.
  - Provide guidance on using the outputs and collect feedback for iterative improvement.
- Data stewardship
  - Maintain a data dictionary and versioning; track data provenance from sample collection to final outputs.
- Advocacy and improvement
  - Highlight opportunities to improve data creation and collection processes to reduce patchiness and format variety.