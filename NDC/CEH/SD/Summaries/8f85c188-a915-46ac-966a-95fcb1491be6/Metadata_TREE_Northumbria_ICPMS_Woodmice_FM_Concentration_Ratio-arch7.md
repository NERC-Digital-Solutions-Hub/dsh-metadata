# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

## Overview
- A data product describing concentration ratios of various elements in wood mice relative to the dry mass of soil, derived from Northumbria CEH sampling.
- Intended for map-based visualization and spatial analysis of metal bioaccumulation at sampling sites.
- Fields cover species identification, site/date context, related soil samples, and a suite of element-specific concentration ratios.

## Dataset structure and key fields
- Biological and sampling context
  - Latin_Species_Name, Common_Species_Name: scientific and common names of the wood mouse species.
  - Site: sampling location.
  - Date_Sample_Collected: date of sample collection.
  - CEH_Sample_Description, Notes: descriptive and contextual commentary for the sample.
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: description of the soil sample used to compute the ratio.
- Concentration ratio fields (for each element)
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
  - Each entry represents the Concentration Ratio (Fresh Mass Woodmice (wholebody) divided By Dry Mass Soil).
  - Units: n/a for all concentration ratio fields.
  - Special markers: Some columns include indicators of "less than" values (e.g., <I, <Be, <Ni, <Ag, <U) to denote censored data.
- Data relationships and provenance
  - The Concentration Ratios are tied to a co-located soil sample used for calculation.
  - The dataset includes a mix of elements, enabling multi-element spatial analysis.

## Data quality, standards, and limitations
- Units are listed as not applicable (n/a) since ratios are dimensionless.
- Some concentration values may be present as censored "<" values, requiring special handling in GIS (e.g., treating as bounds).
- Data may come from multiple sites and resolutions; consistent data standards and metadata quality may vary.
- Potential data challenges include gaps, varying sampling effort, and the need to merge with other spatial layers (soil maps, site boundaries).

## GIS and visualization considerations
- Mapping ideas
  - Visualize concentration ratios by Site or sampling location using color scales or graduated symbols per element.
  - Create multi-layer maps showing species, site, date, and multiple element ratios.
  - Use time-enabled maps to display changes across sampling dates.
- Data handling guidance
  - Treat "<" values as censored data; consider lower/upper bounds in analyses.
  - Link Concentration_Ratio fields to the Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio field for contextual queries.
  - Prepare data joins to base layers (site points, soil sampling areas) for integrated GIS work.
- Analytical opportunities
  - Identify spatial patterns of bioaccumulation across elements and sites.
  - Compare bioavailability proxies across species or sites using the ratio data.

## Practical usage notes
- This dataset serves as a structured data dictionary and a multi-element concentration-ratio table; ensure proper parsing of the mixed descriptive fields and the censored value indicators.
- When integrating into GIS projects, maintain links to sampling context (site, date, soil sample) to support interpretation and reproducibility.