# TREE_Northumbria_ICPMS_Woodmice_Whole_Organism_FM_Concentration

## Overview
- Dataset capturing concentrations of a broad panel of elements in wood mouse whole-organism tissue, expressed as mg/kg fresh mass (FM), using ICP-MS measurements.
- Includes both specimen metadata and a wide range of elemental concentrations (I, Li, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U).
- Metadata fields cover species identifiers, sampling site, collection date, CEH sample description, and notes about tissues used to calculate the concentrations.
- Notes field contains context about tissues and any other relevant sampling details, aiding interpretation and reproducibility.

## Data structure and fields
- Metadata (descriptive information about samples)
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes (notes relating to tissues used to calculate wood mouse whole-organism concentrations)
- Concentration measurements (one row per sample; wide format)
  - I_mg_kg_whole_organism_FM
  - Li_mg_kg_whole_organism_FM
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
  - Ni_mg_kg_whole_organism_FM
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
  - U_mg_kg_whole_organism_FM
- Notes on special values
  - Some columns include “<” markers (e.g., <I, <Ni, <Ag, <U) indicating concentrations reported as below detection limits.

## Measurement method and units
- Measurement technique implied by title: ICP-MS (Inductively Coupled Plasma Mass Spectrometry).
- Concentrations are reported on a mg/kg fresh mass basis (FM).

## Data quality and interpretation considerations
- The Notes field provides tissue-level context essential for interpreting whole-organism concentration values.
- Presence of “less-than” values requires appropriate handling in analyses (censoring or imputation strategies).
- Metadata completeness (species identifiers, site, date, sample description) is crucial for cross-sample comparisons and temporal/spatial analyses.

## Use cases and outputs
- Enables cross-sample comparisons of elemental burdens in wood mice across sites and collection dates.
- Supports exposure assessments, ecological risk analyses, and data products (dashboards, pivot tables) for end users to explore metal burdens.
- Can be integrated with other datasets (e.g., site characteristics, environmental measurements) for broader ecological interpretations.

## Alignment with Data Support aims
- Demonstrates end-to-end data handling: identifying relevant data (species, site, date, tissue notes) and verifying/compiling a comprehensive panel of concentration measurements.
- Provides a ready-to-use data product enabling end users to self-serve analyses via tables or dashboards.
- Highlights the need to communicate data provenance (sample description, tissue used) to ensure correct interpretation and reuse.

## Key considerations for ingestion and curation
- Harmonize sample metadata (Latin_Species_Name, Common_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Description, Notes).
- Normalize concentration values, carefully handling less-than entries and any missing data.
- Maintain references to tissue description notes to preserve context for concentration calculations.
- Ensure traceability to ICP-MS methodology and any laboratory QA/QC documentation implied by the dataset.