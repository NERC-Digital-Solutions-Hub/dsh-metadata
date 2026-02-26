# TREE_Northumbria_ICPMS_Bee_FM_Concentration_Ratio

## Overview
- Dataset describing concentration ratios of various elements in bees (fresh mass, Bee_FM) divided by dry mass soil, derived from ICP-MS measurements.
- Includes metadata about bee species, sampling site, collection date, and sample descriptions.
- Concentration ratios are intended to reflect soil-to-bee transfer, enabling analyses of uptake patterns across sites, species, and time.

## Key Fields and Structure
- Taxonomy and identity:
  - Latin_Species_Name
  - Common_Species_Name
- Sampling context:
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Sample_Details
  - Notes
- Provenance and linkage:
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio (link to the soil sample used for the ratio)
- Concentration ratio measurements (unitless):
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
- Special value indicators:
  - <Be, <Se, <U and related markers indicate concentration ratios that are less-than values
  - Codes such as 1 or 2 accompanying certain concentration ratio columns denote data handling for censored or specific value cases
- Data conventions:
  - Units = n/a for many fields; concentration ratios are treated as dimensionless (unitless)

## Data Interpretation and Use
- What the ratios represent:
  - Fresh Mass Bee concentration divided by Dry Mass Soil concentration for each element (unitless).
- Analytical opportunities:
  - Assess correlations between soil metal concentrations (via the Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio) and bee concentration ratios.
  - Compare uptake across bee species and sampling sites.
  - Explore temporal patterns using Date_Sample_Collected.
  - Identify potential hotspots of uptake or regulatory concerns for environmental health.
- Provenance and reproducibility:
  - The dataset links bee samples to specific soil samples and CEH codes, supporting traceability and reproducibility of concentration-ratio calculations.

## Data Quality, Gaps, and Challenges
- Common challenges aligned with analysts’ data needs:
  - Some fields lack explicit units (Units = n/a); interpret cautiously and document assumptions.
  - Censored data: less-than values indicated by < markers require appropriate statistical handling.
  - Scale and local specificity: data are likely local; careful consideration needed when generalizing beyond sites.
  - Data access and discoverability: metadata-rich structure is present, but actual data availability and integration with other datasets may require navigation of portals and standardized schemas.
- Quality assurance considerations:
  - Ensure consistent species naming and site identifiers across records.
  - Standardize date formats and verify alignment between bee samples and their linked soil samples.
  - Handle < value indicators appropriately in analyses and reporting.

## Practical Guidance for Analysts
- Start with data cleaning and harmonization:
  - Resolve any naming inconsistencies for Latin/Common names and Sites.
  - Align Date_Sample_Collected formats and verify CEH_Sample_Codes against a metadata registry.
  - Flag and separately analyze censored < values.
- Build analyses around:
  - Correlations between soil-linked concentrations and corresponding bee concentration ratios.
  - Multilevel comparisons by Site and by Latin_Species_Name (or Common_Species_Name).
  - Temporal trends across Date_Sample_Collected within and across sites.
- Documentation and reproducibility:
  - Maintain clear provenance for each ratio calculation (which soil sample was used, which bee sample, the exact extraction/measurement methodology implied by Sample_Details and Notes).
  - Preserve metadata in a searchable portal to enable discoverability and re-use.