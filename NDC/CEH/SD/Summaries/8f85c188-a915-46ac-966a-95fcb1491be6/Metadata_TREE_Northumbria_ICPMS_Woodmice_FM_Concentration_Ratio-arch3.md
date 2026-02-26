# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

## Purpose and scope
- Defines a data structure for concentration ratios of elements in wood mice (whole body) relative to soil dry mass.
- Aims to support environmental health monitoring by enabling interpretation of metal transfer from soil to a wildlife indicator species.

## Key fields and data relationships
- Species and location metadata
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes
- Sampling and context
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio (description of the paired soil sample)
- Concentration ratio data
  - I_Concentration_Ratio (with possible <I marker indicating a “less than” value)
  - Li_Concentration_Ratio; Be_Concentration_Ratio; Na_Concentration_Ratio; Mg_Concentration_Ratio; Al_Concentration_Ratio; P_Concentration_Ratio; K_Concentration_Ratio; Ca_Concentration_Ratio; Ti_Concentration_Ratio; V_Concentration_Ratio; Cr_Concentration_Ratio; Mn_Concentration_Ratio; Fe_Concentration_Ratio; Co_Concentration_Ratio; Ni_Concentration_Ratio (with possible <Ni marker); Cu_Concentration_Ratio; Zn_Concentration_Ratio; As_Concentration_Ratio; Se_Concentration_Ratio; Rb_Concentration_Ratio; Sr_Concentration_Ratio; Mo_Concentration_Ratio; Ag_Concentration_Ratio; Cd_Concentration_Ratio; Cs_Concentration_Ratio; Ba_Concentration_Ratio; Tl_Concentration_Ratio; Pb_Concentration_Ratio; U_Concentration_Ratio
  - Many elements include a second variant (denoted by 2) for corresponding concentration ratio fields, e.g., V_Concentration_Ratio, Cr_Concentration_Ratio, Ni_Concentration_Ratio, etc.
- Calculation basis
  - Concentration_Ratio = Fresh Mass Woodmice (wholebody) divided By Dry Mass Soil
- Data quality indicators
  - Use of “<” markers (e.g., <I, <Be, <Ni) to denote upper-bound values in the ratio fields.

## Data quality, metadata and accessibility considerations
- The dataset relies on paired woodmice and co-located soil samples to compute ratios, emphasizing metadata that links biological samples to corresponding soil samples.
- Handling of less-than values is specified in the field markers, impacting interpretation and analysis.
- Clear documentation of sample collection, site description, and sample notes is essential to enable reproducibility and data quality assessment.

## How it supports monitoring and decision-making
- Enables cross-site and temporal comparisons of metal uptake in a wildlife indicator species, informing soil contamination risk assessments.
- Data can feed into reports, dashboards, and governance processes to track environmental health, identify data gaps, and evaluate the effectiveness of remediation or policy measures.

## Practical considerations for implementation
- Ensure complete metadata for each Woodmice and soil pair (site, date, description, notes) to support traceability.
- Establish data governance and sharing practices to make underlying data openly accessible while maintaining quality.
- Develop data transformations to handle <value indicators and to harmonize units across sites for robust comparisons.