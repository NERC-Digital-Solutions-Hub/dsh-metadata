# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

## Overview
- Data dictionary for concentration ratios of elements in woodmice relative to soil, derived from ICP-MS analysis.
- Captures sampling metadata (species names, site, date, sample description) and the specific soil samples used to calculate ratios.
- Focuses on a set of elemental concentration ratios expressed as a ratio of Fresh Mass Woodmice (wholebody) to Dry Mass Soil, enabling environmental exposure assessment around Northumbria.

## Data Structure and Key Variables
- Core identifiers and descriptors:
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes
- Co-located soil context:
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio fields (per element):
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio
  - V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio
  - Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
- For each element, two related fields are present:
  - "<Element>_Concentration_Ratio, 1" and "<Element>_Concentration_Ratio, 2"
  - Explanation indicates that "2" holds the Concentration Ratio (Fresh Mass Woodmice divided by Dry Mass Soil); "1" is often indicated as n/a in the sample metadata.
- Special value handling:
  - Markers such as "<I" and "<Be" indicate concentration ratios expressed as "less than" a value (censored data).

## Concentration Ratio Definition and Scope
- Concentration Ratio definition: Fresh Mass Woodmice (wholebody) divided By Dry Mass Soil.
- Indicates reliance on paired woodmice tissue measurements and corresponding soil mass measurements for each sampling event.
- Data fields include notes about sample description and context to support interpretation of ratios.

## Data Quality, Metadata, and Formatting Notes
- Units for concentration ratio fields are generally n/a, reflecting a dimensionless ratio.
- Some entries include markers for censored values (e.g., less-than notation), highlighting detection limits.
- The structure suggests two sub-fields per element, with one intended to store the computed ratio and the other providing additional context or placeholder (often labeled as n/a in the provided extract).
- The presented table contains formatting irregularities and truncations, indicating potential data cleaning needs before reuse.

## Implications for Monitoring Framework Authors
- Provides a structured template for storing contaminant transfer measures from soil to small mammals, useful for policy evaluation and risk assessment.
- Demonstrates essential metadata components:
  - Species identification, sampling site, date, and descriptive notes.
  - Linkage between biological samples and the specific soil samples used for ratio calculation.
- Highlights data governance needs:
  - Clear provenance for each ratio, handling of censored data, and transparent documentation of measurement and calculation methods.
  - Consideration of data sharing and metadata completeness to support reuse in policy analysis and cross-site comparisons.