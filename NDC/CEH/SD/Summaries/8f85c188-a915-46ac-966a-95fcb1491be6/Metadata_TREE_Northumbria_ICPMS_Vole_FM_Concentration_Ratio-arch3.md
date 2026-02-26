# TREE_Northumbria_ICPMS_Vole_FM_Concentration_Ratio

## Overview
- A data schema for concentration ratio measurements describing metal concentrations in vole tissue relative to surrounding soil.
- Aimed at environmental health monitoring to scrutinise policy, inform decisions, and support future planning.
- Captures the relationship between vole whole-body fresh mass and soil dry mass to derive concentration ratios for multiple elements.

## Key data fields and structure
- Biological identifiers
  - Latin_Species_Name, Common_Species_Name
- Sampling metadata
  - Site, Date_Sample_Collected
  - CEH_Sample_Code, CEH_Sample_Description
  - Notes about the vole sample
- Study and contextual data
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio (soil sample linked to vole collection)
- Concentration ratio variables
  - I_Concentration_Ratio (Iodine), Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
- Special value handling
  - Some elements have “<” markers indicating threshold or censored values (e.g., <Be, <Ni, <U)
  - Ba_Concentration_Ratio and Tl_Concentration_Ratio appear with variants (1, 2)
- Calculation definition
  - Concentration Ratio = Fresh Mass Vole (wholebody) divided By Dry Mass Soil
- Units and interpretation
  - Many concentration ratio fields use n/a units; the ratio itself is the primary metric

## Calculation and data provenance
- Core calculation: Fresh mass of vole whole body divided by the dry mass of the associated soil sample
- Data provenance indicators: linkage between vole sample and co-located soil sample; CEH sample code and description provide traceability
- Metadata considerations: explicit fields for sample context and notes to aid interpretation

## Data quality, access, and governance considerations
- Metadata completeness is essential to verify suitability of data for policy use
- Barriers to reuse may include the need to publicly share datasets and to overcome data silos
- Data must be quality assured and properly managed (cleaning, transformation, clear presentation)
- Open data sharing and robust data governance are important to enable reuse and comparability across sites and time

## How this supports monitoring and policy decisions
- Enables assessment of metal exposure in wildlife relative to environmental baselines
- Facilitates cross-site comparisons and temporal trend analysis through standardized concentration ratios
- Supports evidence-based decision-making on environmental health risks and regulatory priorities

## Challenges to be aware of (from the monitoring framework perspective)
- Data gaps and inconsistent metadata can hinder usability
- Access constraints and data silos impede timely analysis
- Complex data formats require careful transformation and harmonization
- Communicating complex findings (multi-element ratios) clearly to stakeholders and policymakers
- Implementing and maintaining data governance to keep datasets current and verifiable