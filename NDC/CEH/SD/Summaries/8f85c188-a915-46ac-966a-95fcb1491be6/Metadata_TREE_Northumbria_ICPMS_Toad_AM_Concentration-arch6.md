# TREE_Northumbria_ICPMS_Toad_AM_Concentration

## Overview
- A tabular dataset detailing ICP-MS elemental concentrations in toad ash mass samples from Northumbria.
- Includes both descriptive metadata (species, site, date, sample codes, preparation notes) and quantitative analyte measurements (multiple elements).

## Data Structure and Variables
- Sample and specimen metadata
  - Latin_Species_Name, Common_Species_Name
  - Site, Date_Sample_Collected
  - CEH_Sample_Code, CEH_Sample_Description
  - Fresh_Mass_Ash_Mass_Ratio (and noted formatting quirks)
  - Notes (related to toad preparation)
- Analyte concentrations (all in mg/kg ash mass)
  - I_mg_kg_AM, Li_mg_kg_AM, Be_mg_kg_AM, Na_mg_kg_AM, Mg_mg_kg_AM, Al_mg_kg_AM, P_mg_kg_AM, K_mg_kg_AM, Ca_mg_kg_AM, Ti_mg_kg_AM, V_mg_kg_AM, Cr_mg_kg_AM
  - Mn_mg_kg_AM, Fe_mg_kg_AM, Co_mg_kg_AM, Ni_mg_kg_AM, Cu_mg_kg_AM, Zn_mg_kg_AM, As_mg_kg_AM, Se_mg_kg_AM, Rb_mg_kg_AM, Sr_mg_kg_AM, Mo_mg_kg_AM, Ag_mg_kg_AM, Cd_mg_kg_AM, Cs_mg_kg_AM, Ba_mg_kg_AM, Tl_mg_kg_AM, Pb_mg_kg_AM, U_mg_kg_AM
- Notes on data formatting
  - Several fields show inconsistent or ambiguous formatting (e.g., "Fresh_Mass_Ash_Mass _Ratio" with a space; various column label typos such as "Mn_mg_kg_AM,  = mg/kg" and "Tl_mg_kg_AM_,  = mg/kg").
  - Some columns have accompanying explanations clarifying that the value is a concentration in mg/kg ash mass.

## Data Quality and Cleaning Considerations
- Potential inconsistencies to address
  - Formatting and naming inconsistencies in field headers and units for several columns.
  - Occasional missing or ambiguous unit annotations in the header (e.g., some units repeated as "n/a" or described inconsistently).
  - Notes field may contain preparation-related details critical for interpretation.
- Recommended data preparation steps
  - Standardize column names (remove stray spaces, fix typos) and unify case.
  - Normalize units (confirm all analyte concentrations are mg/kg ash mass) and convert if needed.
  - Validate and parse dates (Date_Sample_Collected) to a consistent date format.
  *Create a data dictionary mapping each field to its meaning and unit for end users.*

## How Data Supports Analysis and Insights
- Structure enables self-serve exploration
  - Compare metal concentrations across species, sites, and collection dates.
  - Analyze multi-element patterns to identify signatures or anomalies per sample.
  - Build dashboards or pivot tables to summarize concentrations by site, species, or date.
- Potential analyses
  - Descriptive statistics and distribution of each element by site/species.
  - Multielement profiling to detect patterns (e.g., correlation networks among elements).
  - Time/space trend exploration if dates and sites cover a meaningful range.
  - Data-driven dashboards showing concentration ranges with notes on preparation.

## Gaps, Limitations, and Future Work
- Data gaps
  - Missing or inconsistent field names and units require cleaning before aggregation.
  - Potential gaps in dates or site coverage are not explicitly stated.
- Recommendations
  - Produce a cleaned, query-friendly version with standardized field names and verified units.
  - Add a complete data dictionary and provenance notes to aid reproducibility.
  - Where possible, link CEH_Sample_Code to a broader sample metadata record for richer context.

## Access, Provenance, and Reuse
- CEH_Sample_Code and CEH_Sample_Description provide provenance for individual samples.
- The Notes field captures toad preparation specifics, important for interpretation of results.
- Prior to reuse, ensure a consistent, well-documented data dictionary is available to guide end users through the analyte list and their units.