# TREE_Northumbria_ICPMS_Deer_FM_concentration

## Overview
- A dataset of ICP-MS concentrations of a wide range of elements in deer tissue, measured as mg/kg fresh mass (FM).
- Includes accompanying sample metadata to support contextual analysis: Latin and common species names, sampling site, date collected, UKCEH sample codes and description, tissue type, and Fresh Mass Dry Mass Ratio.
- Featured elements include I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U, with notes on < (less-than) values for some measurements.

## Data structure and key fields
- Taxonomy and identity: Latin_Species_Name, Common_Species_Name.
- Sampling metadata: Site, Date_Sample_Collected, CEH_Sample_Codes, CEH_Sample_Description.
- Biological material: Tissue, Fresh_Mass_Dry_Mass_Ratio.
- Concentration data (all in mg/kg FM): I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM.
- Data quality indicators: Some columns are explicitly noted as “no data” for Roe deer 4 thyroid; many elements have “<” values indicating concentrations below detection/quantification limits (e.g., Be_mg_kg_FM, Al_mg_kg_FM, V_mg_kg_FM, K_mg_kg_FM as described in the documentation).
- Data format notes: Some field names include underscores and there are occasional formatting inconsistencies in the header descriptions, but the intended meaning is clear (element concentration per kilogram of fresh mass with accompanying metadata).

## Data quality and caveats
- Patchy data: Roe deer 4 thyroid data show missing values across many elements; several “No data” notes indicate incomplete records for this sample.
- Detection limitations: Certain concentrations are reported as less-than values (indicated by markers in respective columns).
- Data integration considerations: The dataset appears to come from multiple data sources/systems; harmonization may be required for consistent units, naming, and handling of missing values.
- Formatting irregularities: Some header/explanation lines are truncated or inconsistently formatted, requiring careful interpretation during data ingestion.

## How this data supports end users (Data Support perspective)
- Enables self-serve analysis through dashboards or pivot-table-type outputs by filtering on species, site, date, and tissue, and by comparing element concentrations.
- Supports normalization and comparisons by including tissue type and Fresh Mass Dry Mass Ratio.
- Provides provenance cues via CEH_Sample_Codes and CEH_Sample_Description to aid traceability and data quality checks.
- Facilitates pattern discovery and QA workflows: identify unusually high/low concentrations, detect potential data gaps, and assess consistency across samples and sites.
- Ready-to-use for creating concentration summaries, temporal or spatial trends, and cross-element comparisons once data gaps and < values are reconciled.

## Practical guidance for Data Support workflows
- Clarify the user ask to determine which species, sites, tissues, and time windows are of interest, and which elements to prioritize.
- Data cleaning and transformation steps:
  - Resolve Roe deer 4 thyroid gaps by documenting missingness and understanding whether data exist elsewhere.
  - Interpret and standardize <value markers across elements.
  - Harmonize units and ensure consistent mg/kg FM representations.
  - Align field names and descriptions to a stable schema for downstream tooling.
- Data product ideas:
  - Dashboards showing element concentration distributions by site and tissue, with filters for species and date.
  - Pivot-ready tables comparing concentrations across selected elements or samples.
  - Summaries and trend analyses that flag outliers or data gaps, with notes on detection limits.
- Feedback and improvement:
  - Gather end-user feedback on usability and data coverage.
  - Advocate for more complete data collection across all roe deer individuals and tissues to reduce gaps.