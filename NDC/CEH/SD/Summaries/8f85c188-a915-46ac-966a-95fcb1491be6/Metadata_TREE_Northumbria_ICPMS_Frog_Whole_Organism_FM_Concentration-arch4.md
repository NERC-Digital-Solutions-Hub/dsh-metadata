# TREE_Northumbria_ICPMS_Frog_Whole_Organism_FM_Concentration

## Overview
- Dataset capturing concentrations of multiple elements in frog whole-organism tissue using ICP-MS, expressed on a fresh mass basis (mg/kg FM).
- Includes taxonomic identifiers (Latin and Common names), sampling metadata (Site, Date_Sample_Collected), and descriptive context (CEH_Sample_Description, Notes).
- Contains concentration columns for a wide suite of elements (I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) with explicit unit definitions and explanations.
- Some values appear as censored (< value) or marked as Not calculated, reflecting data nuances and measurement constraints.
- Aimed at supporting environmental monitoring, toxicology assessments, and cross-study data integration.

## Data Fields and Structure
- Identification and taxonomy:
  - Latin_Species_Name, Common_Species_Name
- Sampling metadata:
  - Site, Date_Sample_Collected
- Description and notes:
  - CEH_Sample_Description, Notes
- Concentration measurements (all on mg/kg fresh mass):
  - I_mg_kg_whole_organism_FM (Not calculated)
  - Li_mg_kg_whole_organism_FM
  - Be_mg_kg_whole_organism_FM (less-than markers used when applicable)
  - Na_mg_kg_whole_organism_FM
  - Mg_mg_kg_whole_organism_FM
  - Al_mg_kg_whole_organism_FM
  - P_mg_kg_whole_organism_FM
  - K_mg_kg_whole_organism_FM
  - Ca_mg_kg_whole_organism_FM
  - Ti_mg_kg_whole_organism_FM
  - V_mg_kg_whole_organism_FM
  - Cr_mg_kg_whole_organism_FM
  - Mn_mg_kg_whole_organism_FM
  - Fe_mg_kg_whole_organism_FM
  - Co_mg_kg_whole_organism_FM
  - Ni_mg_kg_whole_organism_FM (note: some entries may be < value)
  - Cu_mg_kg_whole_organism_FM
  - Zn_mg_kg_whole_organism_FM
  - As_mg_kg_whole_organism_FM
  - Se_mg_kg_whole_organism_FM
  - Rb_mg_kg_whole_organism_FM
  - Sr_mg_kg_whole_organism_FM
  - Mo_mg_kg_whole_organism_FM
  - Ag_mg_kg_whole_organism_FM
  - Cd_mg_kg_whole_organism_FM
  - Cs_mg_kg_whole_organism_FM
  - Ba_mg_kg_whole_organism_FM
  - Tl_mg_kg_whole_organism_FM
  - Pb_mg_kg_whole_organism_FM
  - U_mg_kg_whole_organism_FM (note: < value markers may apply)
- Data notes and conventions:
  - Some concentration values include “<” markers to denote censored data.
  - Some fields may be marked as Not calculated (e.g., I_mg_kg_whole_organism_FM).

## Data Quality and Handling Considerations
- Measurements are reported per kilogram of fresh mass, enabling comparability across samples.
- Presence of < markers requires special handling in analyses (censored data methods).
- Not calculated values indicate incomplete data for certain elements in some samples.
- Rich metadata (species names, site, date, tissue notes) supports traceability and reuse across studies and datasets.

## Relevance for Data Leaders
- Demonstrates a comprehensive, standardized data schema with explicit field explanations for each measurement.
- Emphasizes metadata completeness (taxonomy, site, date, sample description) to support data governance and user comprehension.
- Highlights common data-system challenges in environmental data, such as fragmented data and the need for clear handling of censored values and non-calculated fields.
- Provides a model for ensuring data discoverability, interoperability, and consistent unit usage across related datasets.

## Recommended Actions for Data Governance and Use
- Standardize column naming, units (mg/kg FM), and metadata across datasets to enable cross-study comparisons.
- Implement clear handling rules for censored data (e.g., < values) and for Not calculated fields in analyses and reports.
- Maintain detailed provenance and tissue-level notes to support reproducibility and accurate interpretation.
- Enhance data catalogs with this schema to improve discoverability for policy colleagues and partner networks.
- Establish data quality checks to flag missing values, inconsistent units, and unexplained censored values, enabling timely remediation.