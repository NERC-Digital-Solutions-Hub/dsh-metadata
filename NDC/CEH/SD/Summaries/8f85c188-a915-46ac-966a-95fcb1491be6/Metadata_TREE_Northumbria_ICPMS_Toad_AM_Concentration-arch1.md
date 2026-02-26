# TREE_Northumbria_ICPMS_Toad_AM_Concentration

## Overview
- A dataset of ICP-MS derived elemental concentrations in ash mass from toads sampled at Northumbria.
- Includes taxonomic identifiers, sampling metadata, and a broad suite of elements quantified as mg/kg_Ash.
- Captures sample preparation notes and the ratio of fresh mass to ash mass.

## Key fields and data structure
- Biological and contextual identifiers:
  - Latin_Species_Name; Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Code; CEH_Sample_Description
  - Notes (related to toad preparation)
  - Fresh_Mass_Ash_Mass_Ratio (ratio of whole-organism fresh mass to ash mass)
- Concentration data (mg/kg_Ash):
  - I_mg_kg_AM, Li_mg_kg_AM, Be_mg_kg_AM, Na_mg_kg_AM, Mg_mg_kg_AM, Al_mg_kg_AM
  - P_mg_kg_AM, K_mg_kg_AM, Ca_mg_kg_AM, Ti_mg_kg_AM, V_mg_kg_AM
  - Cr_mg_kg_AM, Mn_mg_kg_AM, Fe_mg_kg_AM, Co_mg_kg_AM, Ni_mg_kg_AM
  - Cu_mg_kg_AM, Zn_mg_kg_AM, As_mg_kg_AM, Se_mg_kg_AM, Rb_mg_kg_AM
  - Sr_mg_kg_AM, Mo_mg_kg_AM, Ag_mg_kg_AM, Cd_mg_kg_AM, Cs_mg_kg_AM
  - Ba_mg_kg_AM, Tl_mg_kg_AM, Pb_mg_kg_AM, U_mg_kg_AM
- Note: Some field labels show formatting inconsistencies in the source (e.g., extra spaces, punctuation), but they represent standard ICP-MS trace element concentrations in ash.

## Data quality and potential issues
- Metadata inconsistencies:
  - Units often marked as n/a, and some parsing artifacts (e.g., “1 = . , 2 = milligram per kilogram ash mass”) indicate data import issues.
- Scope and formatting:
  - Fields are designed for ash-mass concentration reporting; cross-walking to tissue-mass data requires conversion.
  - Possible variability in sample codes and descriptions across entries.
- Data completeness:
  - Some elements may have missing values or detection-limit-related gaps typical of ICP-MS datasets.

## How analysts can use this data
- Explore spatial and temporal patterns in element concentrations across Northumbria sampling sites and dates.
- Identify correlations among elements (e.g., potential co-occurrence of metals) and relate to toad preparation/ash mass ratio.
- Build predictive models of contaminant exposure by site, date, or species-related factors.
- Compare to other matrices or species by normalising to ash mass or converting to fresh mass basis if needed.
- Integrate with metadata portals, ensuring proper documentation of data sources and preparation notes for reproducibility.

## Preparation and modeling considerations
- Normalize concentrations if comparing to non-ash baselines; adjust for Fresh_Mass_Ash_Mass_Ratio as needed.
- QA steps to address garbled metadata: standardize field names, verify units, and document any corrections.
- Handle missing values and consider detection limits typical of ICP-MS when performing statistical analyses.
- Maintain traceability of sample metadata (site, date, sample code) to support reproducible correlations and predictions.