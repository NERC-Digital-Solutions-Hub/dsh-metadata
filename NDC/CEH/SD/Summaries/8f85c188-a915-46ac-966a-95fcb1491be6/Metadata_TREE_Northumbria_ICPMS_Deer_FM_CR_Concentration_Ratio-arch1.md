# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

## Purpose and scope
- Describes a dataset of concentration ratios for elements in woodmice, calculated as the ratio of the woodmouse’s fresh mass (whole body) to the dry mass of soil from a co-located sample.
- Metadata includes species names, sampling site, date of collection, CEH sample description, and notes related to each woodmice sample.
- Used to support analyses of bioaccumulation and potential correlations with site characteristics, sampling date, and soil context.

## Data structure and key fields
- Rows represent individual woodmice samples; each row links to a co-located soil sample used to compute the concentration ratio.
- Core metadata fields:
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio fields (element-specific):
  - I_Concentration_Ratio (and indicators for less-than values)
  - Li_Concentration_Ratio
  - Be_Concentration_Ratio (with possible less-than marker)
  - Na_Concentration_Ratio
  - Mg_Concentration_Ratio
  - Al_Concentration_Ratio
  - P_Concentration_Ratio
  - K_Concentration_Ratio
  - Ca_Concentration_Ratio
  - Ti_Concentration_Ratio
  - V_Concentration_Ratio (has two variants; two entries labeled 1 and 2)
  - Cr_Concentration_Ratio (two variants: 1 and 2)
  - Mn_Concentration_Ratio (two variants: 1 and 2)
  - Fe_Concentration_Ratio (two variants: 1 and 2)
  - Co_Concentration_Ratio (two variants: 1 and 2)
  - Ni_Concentration_Ratio (two variants: 1 and 2; with potential less-than marker)
  - Cu_Concentration_Ratio (two variants: 1 and 2)
  - Zn_Concentration_Ratio (two variants: 1 and 2)
  - As_Concentration_Ratio (two variants: 1 and 2)
  - Se_Concentration_Ratio (two variants: 1 and 2)
  - Rb_Concentration_Ratio (two variants: 1 and 2)
  - Sr_Concentration_Ratio (two variants: 1 and 2)
  - Mo_Concentration_Ratio (two variants: 1 and 2)
  - Ag_Concentration_Ratio (two variants: 1 and 2; with potential less-than marker)
  - Cd_Concentration_Ratio (two variants: 1 and 2)
  - Cs_Concentration_Ratio (two variants: 1 and 2)
  - Ba_Concentration_Ratio (two variants: 1 and 2)
  - Tl_Concentration_Ratio (two variants: 1 and 2; note potential labeling inconsistencies)
  - Pb_Concentration_Ratio (two variants: 1 and 2)
  - U_Concentration_Ratio (two variants: 1 and 2)
- Value formatting notes:
  - Some concentration values appear with a leading “<” marker to denote censored or below-detection values.
  - For certain elements, there are dual ratio columns (labeled with “1” and “2”), indicating multiple ratio representations or data sources per element.

## Calculation and units
- Concentration ratio definition: Fresh Mass Woodmice (whole body) divided By Dry Mass Soil.
- Units for most fields are listed as n/a, reflecting that these are dimensionless ratios rather than physical concentrations.

## Data provenance and context
- Dataset appears to originate from Northumbria in conjunction with ICPMS measurements (Inductively Coupled Plasma Mass Spectrometry) and CEH (Centre for Ecology & Hydrology) sample metadata.
- Designed to enable cross-sample comparisons of element accumulation in woodmice relative to soil context.

## Key uses and analyses
- Identify correlations between woodmice tissue-to-soil ratios and:
  - Sampling site
  - Date of sample collection
  - Woodmice species
  - Soil characteristics from co-located samples
- Develop predictive models of bioaccumulation for multiple elements.
- Handle censored data (less-than values) and multiple ratio representations per element.
- Integrate with other datasets to enhance interpretation of spatial and temporal trends in metal/element uptake.

## Data quality and considerations
- Presence of censored (“less-than”) values requiring appropriate statistical treatment.
- Some elements have multiple concentration-ratio columns, requiring careful alignment and interpretation.
- Metadata completeness (species, site, date, soil co-location) is essential for reliable analysis and comparability across samples.

## Practical guidance for analysts
- Clean and harmonize censored values before modeling (consistent handling of < indicators).
- Map dual-element ratio columns to a clear data schema to avoid misinterpretation (which 1 vs 2 variant applies to which analysis).
- Maintain linkage to co-located soil samples to ensure correct soil mass context for each woodmice ratio.
- Document data sources and metadata provenance to preserve traceability for reproducible analyses.