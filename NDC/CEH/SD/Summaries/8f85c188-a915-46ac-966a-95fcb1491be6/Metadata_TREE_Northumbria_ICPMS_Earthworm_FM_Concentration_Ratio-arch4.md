# TREE_Northumbria_ICPMS_Earthworm_FM_Concentration_Ratio

## Overview
- Dataset capturing concentration ratios of earthworms relative to soil, calculated as Fresh Mass Earthworm (wholebody) divided By Dry Mass Soil.
- Records include species identification (Latin and common names), sampling site, collection date, and associated CEH sample codes/descriptions.
- For each record, a description of the co-located soil sample used to calculate the concentration ratio is provided, along with optional notes.
- Contains concentration ratio fields for a wide range of elements (e.g., I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U).

## Key Data Elements
- Species and Site
  - Latin_Species_Name
  - Common_Species_Name
  - Site
- Sampling and Sample Metadata
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Notes
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration Ratios (per Element)
  - I_Concentration_Ratio
  - Li_Concentration_Ratio
  - Be_Concentration_Ratio
  - Na_Concentration_Ratio
  - Mg_Concentration_Ratio
  - Al_Concentration_Ratio
  - P_Concentration_Ratio
  - K_Concentration_Ratio
  - Ca_Concentration_Ratio
  - Ti_Concentration_Ratio
  - V_Concentration_Ratio
  - Cr_Concentration_Ratio
  - Fe_Concentration_Ratio
  - Co_Concentration_Ratio
  - Ni_Concentration_Ratio
  - Cu_Concentration_Ratio
  - Zn_Concentration_Ratio
  - As_Concentration_Ratio
  - Se_Concentration_Ratio
  - Rb_Concentration_Ratio
  - Sr_Concentration_Ratio
  - Mo_Concentration_Ratio
  - Ag_Concentration_Ratio
  - Cd_Concentration_Ratio
  - Cs_Concentration_Ratio
  - Ba_Concentration_Ratio
  - Tl_Concentration_Ratio
  - Pb_Concentration_Ratio
  - U_Concentration_Ratio (two fields noted: 1 and 2, with 2 defined as the U Concentration Ratio)

## Calculation and Provenance
- Ratio Definition: For each listed element, the concentration ratio is calculated as Fresh Mass Earthworm (wholebody) divided by Dry Mass Soil.
- Contextual Data: Includes co-located soil sample information used for ratio calculation to support traceability and interpretation.
- Sample Identification: CEH_Sample_Codes and CEH_Sample_Description provide traceable sample identifiers and preparation details.

## Metadata and Data Quality Considerations
- Metadata Gaps: Many fields show "Units = n/a" and descriptions that may vary in format; standardizing units and metadata terminology would improve discoverability.
- Data Quality Indicators: Presence of notes and co-located soil sample context supports data quality but requires consistent metadata for proper interpretation.
- Formatting Anomalies: Some field labels show minor inconsistencies (e.g., Tl_Concentration_Ratio_ vs Tl_Concentration_Ratio) which could affect data ingestion pipelines.
- Scope and Coverage: Wide range of elements suggests comprehensive metal/element profiling; ensure complete coverage across samples and consistent handling of missing values.

## Use and Data Governance Implications for Data Leaders
- System View: This dataset is a component of a broader data system linking species, location, timing, and multi-element concentration metrics; ensure it is integrated with other data products (e.g., soil characteristics, environmental context).
- User Needs and Access: Data users may include policy colleagues and researchers needing traceable sample provenance and clear calculation methods; provide clear data dictionary and data lineage.
- Discoverability and Discoverability Enhancements: Improve documentation of fields, units, and calculation methods; maintain a centralized metadata repository and data dictionary.
- Data Quality Governance: Standardize metadata (units, field definitions), enforce naming conventions, and implement validation checks for concentration ratio calculations and sample context.
- Collaboration: Consider cross-network coordination to align data standards for earthworm–soil concentration ratios, enabling broader comparability and reuse.