# TREE_Northumbria_ICPMS_Deer_Whole_Organism_FM_Concentration

## Overview
- Dataset of concentrations for multiple elements in deer whole-organism tissue, measured on a fresh mass basis (mg/kg) using ICP-MS.
- Includes taxonomic, sampling, and metadata to contextualize concentrations (Latin and common species names, sampling site, date collected, UKCEH/CEH sample codes and descriptions, and notes on tissues used).

## Data Structure and Key Variables
- Metadata fields:
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
  - Notes (details about tissues used to calculate whole-organism concentrations)
- Concentration measurements (per element, all on mg/kg fresh mass):
  - I_mg_kg_whole-organism_FM
  - Li_mg_kg_whole-organism_FM
  - Be_mg_kg_whole-organism_FM
  - Na_mg_kg_whole-organism_FM
  - Mg_mg_kg_whole-organism_FM
  - Al_mg_kg_whole-organism_FM
  - P_mg_kg_whole-organism_FM
  - K_mg_kg_whole-organism_FM
  - Ca_mg_kg_whole-organism_FM
  - Ti_mg_kg_whole-organism_FM
  - V_mg_kg_whole-organism_FM
  - Cr_mg_kg_whole-organism_FM
  - Mn_mg_kg_whole-organism_FM
  - Fe_mg_kg_whole-organism_FM
  - Co_mg_kg_whole-organism_FM
  - Ni_mg_kg_whole-organism_FM
  - Cu_mg_kg_whole-organism_FM
  - Zn_mg_kg_whole-organism_FM
  - As_mg_kg_whole-organism_FM
  - Se_mg_kg_whole-organism_FM
  - Rb_mg_kg_whole-organism_FM
  - Sr_mg_kg_whole-organism_FM
  - Mo_mg_kg_whole-organism_FM
  - Ag_mg_kg_whole-organism_FM
  - Cd_mg_kg_whole-organism_FM
  - Cs_mg_kg_whole-organism_FM
  - Ba_mg_kg_whole-organism_FM
  - Tl_mg_kg_whole-organism_FM
  - Pb_mg_kg_whole-organism_FM
  - U_mg_kg_whole-organism_FM
- Notes on data structure:
  - Some elements have dual-related fields (e.g., “1” and “2”) indicating two-part entries or related measurements per element.
  - Some columns may use a “<” marker to denote values below detection limits.

## Measurement Details
- All concentrations are reported on a fresh mass basis (mg/kg).
- Notes may specify the tissues included in the whole-organism calculation.
- Occasional less-than values indicate censored/detectability limitations for certain elements.

## Data Quality and Provenance
- Metadata ties to UKCEH (UK Centre for Ecology & Hydrology) sampling and CEH sample codes/descriptions, enabling traceability to source samples.
- Designed to be discoverable with rich metadata; emphasis on tracking data sources and supplementing with descriptive notes.

## Practical Considerations for Analysts
- Data may have gaps at local scales or irregular coverage across sites or species.
- Handling "<" values will be necessary during analysis (e.g., imputation or censoring strategies).
- Two-part element fields (e.g., entries labeled “1” and “2”) require careful interpretation to ensure correct aggregation or comparison.
- Tissue-level notes are essential for accurate interpretation of whole-organism concentrations.

## Potential Uses
- Cross-element correlation analyses and ecological risk assessments for deer.
- Regulatory exposure assessments and environmental monitoring programs.
- Modelling to predict how actions may alter elemental burdens in deer populations.

## Limitations and Cautions
- Some column naming exhibits inconsistencies that may require careful data cleaning during integration.
- Presence of detection-limit indicators (“<”) requires transparent handling in any downstream analysis.
- Local-scale data availability and standardization across datasets may affect comparability.