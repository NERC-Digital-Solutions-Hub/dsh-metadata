# TREE_Northumbria_ICPMS_Bee_FM_Concentration

## Overview
- Dataset detailing ICPMS-measured metal concentrations in bee samples from Northumbria.
- Includes taxonomic identifiers, sampling site and date, UKCEH sample codes/descriptions, and sample details/notes.
- Concentrations are reported as mg/kg fresh mass (FM).

## Data columns and descriptions

### Taxonomy and sample identifiers
- Latin_Species_Name: Latin name of species
- Common_Species_Name: Common name of species
- Site: Sampling site
- Date_Sample_Collected: Date sample was collected
- CEH_Sample_Codes: UKCEH sample codes
- CEH_Sample_Description: UKCEH sample description
- Sample_Details: Additional sample details
- Notes: Notes on bees

### Concentration measurements (mg/kg_FM)
- I_mg_kg_FM
- Li_mg_kg_FM
- Be_mg_kg_FM
- Na_mg_kg_FM
- Mg_mg_kg_FM
- Al_mg_kg_FM
- P_mg_kg_FM
- K_mg_kg_FM
- Ca_mg_kg_FM
- Ti_mg_kg_FM
- V_mg_kg_FM
- Cr_mg_kg_FM
- Mn_mg_kg_FM
- Fe_mg_kg_FM
- Co_mg_kg_FM
- Ni_mg_kg_FM
- Cu_mg_kg_FM
- Zn_mg_kg_FM
- As_mg_kg_FM
- Se_mg_kg_FM
- Rb_mg_kg_FM
- Sr_mg_kg_FM
- Mo_mg_kg_FM
- Ag_mg_kg_FM
- Cd_mg_kg_FM
- Cs_mg_kg_FM
- Ba_mg_kg_FM
- Tl_mg_kg_FM
- Pb_mg_kg_FM
- U_mg_kg_FM

### Special indicators for less-than values
- <Be: marker indicating Be concentration is a "less than" value corresponding to Be_mg_kg_FM
- <Se: marker indicating Se concentration is a "less than" value corresponding to Se_mg_kg_FM
- <U: marker indicating U concentration is a "less than" value corresponding to U_mg_kg_FM

## Units and data conventions
- Concentrations: mg/kg_FM (milligrams per kilogram of fresh mass)
- Notes indicate that some markers denote below-detection or below-threshold values
- Some metadata fields contain minor typographical notes (e.g., description text) but the core fields are standard

## Context and potential uses
- Enables analysis of metal accumulation in bees by species, site, and collection date
- Facilitates cross-dataset integration via CEH sample codes and descriptions
- Supports correlations, exposure assessments, and predictive analyses relating bee contamination to environmental variables

## Practical considerations for analysts
- Be mindful of less-than values (<Be, <Se, <U)) in interpretation and statistical handling
- Ensure consistent handling of missing or ambiguous metadata (e.g., minor typos in descriptions)
- Consider harmonizing site, date, and sample-code mappings when merging with additional datasets
- Track data provenance and maintain metadata for reproducible analyses