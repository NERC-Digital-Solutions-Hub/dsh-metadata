# TREE_Northumbria_ICPMS_Frog_Whole_Organism_FM_Concentration

## Overview
- Dataset describing concentrations of a broad suite of elements in frog whole-organism tissues (fresh mass basis).
- Data captured for context: Latin and common species names, sampling site, sample collection date, UKCEH/CEH sample descriptions, and notes on tissues used.
- Concentrations are reported as mg/kg fresh mass (FM) for a wide range of elements, with some entries marked as below detection (<) values.

## Data Structure and Key Variables
- Taxonomy and sample context
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes (tissues used to calculate concentrations)
- Concentration measurements (all mg/kg, fresh mass)
  - I_mg_kg_whole_organism_FM
  - Li_mg_kg_whole_organism_FM
  - Be_mg_kg_whole_organism_FM (and <Be indicator)
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
  - Ni_mg_kg_whole_organism_FM (and <Ni indicator)
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
  - U_mg_kg_whole_organism_FM (and <U indicator)

## Measurement and Scope
- Analytical method: ICP-MS (Inductively Coupled Plasma Mass Spectrometry) as indicated by the dataset title.
- Matrix: frog whole-organism tissue, concentrations normalized to fresh mass (FM).
- Species and sites: includes multiple frog species and sampling sites; date of collection recorded.
- Data qualifiers: "<" values denote concentrations below detection/quantification limits; some fields show n/a units.

## Data Quality and Metadata Considerations
- Metadata embedded in notes and CEH_Sample_Description aid interpretation of tissue types and preparation.
- Presence of censored (<) values requires appropriate handling in analyses (e.g., non-detect imputation).
- Units are specified as mg/kg FM for most elements; some fields indicate non-applicable or missing units (n/a).
- Documentation on data provenance and traceability emphasized by CEH/UKCEH context and sample descriptions.

## Potential Analyses and Use Cases
- Descriptive summaries by site and species to identify spatial patterns in metal burdens.
- Cross-element analysis to detect pollution signatures and potential co-accumulation patterns.
- Temporal trends if multiple collection dates exist; correlate with site conditions or management actions.
- Risk assessment for amphibians by comparing concentrations to ecological or regulatory guidelines (where available).
- Data integration with other environmental datasets (e.g., water/soil chemistry) to explore exposure pathways.
- Preparation for data sharing and reproducibility via clear metadata and traceable data sources.

## Practical Considerations for Analysts
- Address below-detection values appropriately (methods include substitution, substitution with half-detection limit, or modeling).
- Ensure harmonization of units and tissue descriptions when combining with other datasets.
- Maintain provenance by linking measurements to specimen identity, site, date, and CEH UKCEH descriptions.
- Leverage the wide element panel to explore multivariate relationships and contamination fingerprints.