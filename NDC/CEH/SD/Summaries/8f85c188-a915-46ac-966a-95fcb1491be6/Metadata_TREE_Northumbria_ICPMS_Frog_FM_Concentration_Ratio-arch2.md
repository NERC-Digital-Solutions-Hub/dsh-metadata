# TREE_Northumbria_ICPMS_Bee_FM_Concentration_Ratio

## Purpose and scope
- A dataset schema for concentration ratios of trace elements in bee samples, calculated as Fresh Mass Bee (whole body) concentration divided by Dry Mass Soil.
- Documents metadata and all elemental concentration ratio columns to support environmental monitoring of bioaccumulation at Northumbria.

## Key variables and structure
- Biological and sampling identifiers:
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Sample_Details, Notes
- Co-located soil linkage:
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio measurements (elemental suite):
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio
  - Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio
  - V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio
  - Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio
  - Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio
  - Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
- Notation specifics:
  - Some columns include a less-than marker (e.g., <Be, <Se, <U) to indicate values below a threshold.
  - Some elements have paired columns (e.g., 1 and 2 variants) for certain concentration ratio representations.
- Data descriptors:
  - Units often listed as n/a with accompanying Explanations detailing what each column represents.

## How this supports monitoring and analysis
- Provides a standard, auditable format to assess metal bioaccumulation in bees relative to soil across sites and times.
- Facilitates cross-site and temporal comparisons for environmental health assessments and policy performance.

## Data quality, processing and access
- Requires verification and quality assurance of sample metadata, soil-bee pairing, and date/site accuracy.
- Standardised cleaning and transformation should handle fields with n/a units, < values, and multiple ratio representations.
- Designed for storage in appropriate data portals to enable broad access to underlying data used for final outputs (maps, charts, reports).

## Analytical considerations and usage
- Enables synthesis with other datasets to enhance value beyond single-use analyses.
- Important to document handling of below-detection and < values, as well as any assumptions in ratio calculations.
- Potential outputs include element-by-site/time visualizations, species-specific bioaccumulation profiles, and trend analyses.

## Practical implications for stakeholders
- Supports transparent reporting on environmental contamination and bee exposure relative to soil conditions.
- Offers a reproducible framework for monitoring programs to track environmental health and policy outcomes over time.