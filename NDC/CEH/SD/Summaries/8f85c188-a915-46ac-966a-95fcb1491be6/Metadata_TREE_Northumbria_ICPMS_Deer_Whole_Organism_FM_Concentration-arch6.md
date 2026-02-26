# TREE_Northumbria_ICPMS_Deer_Whole_Organism_FM_Concentration

## Overview
- Dataset schema for deer whole-organism fresh mass concentrations of multiple elements measured by ICP-MS.
- Includes both metadata about samples (species, site, date, sample codes, descriptions, notes) and quantitative concentrations for a broad suite of elements.
- Concentrations are primarily reported in mg/kg fresh mass, with some fields allowing “less than” markers and dual-value columns for certain elements.

## Key metadata fields
- Latin_Species_Name: Latin name of deer species.
- Common_Species_Name: Common name of deer species.
- Site: Sampling site.
- Date_Sample_Collected: Date the sample was collected.
- CEH_Sample_Codes: UKCEH sample codes.
- CEH_Sample_Description: Description of the UKCEH sample.
- Notes: Notes related to tissues used to calculate deer whole-organism concentrations.

## Concentration data (mg/kg, fresh mass)
- I_mg_kg_whole-organism_FM
- Li_mg_kg_whole-organism_FM
- Be_mg_kg_whole-organism_FM (often with a preceding < marker to indicate a '<' value)
- Na_mg_kg_whole-organism_FM
- Mg_mg_kg_whole-organism_FM
- Al_mg_kg_whole-organism_FM (often with a preceding < marker)
- P_mg_kg_whole-organism_FM
- K_mg_kg_whole-organism_FM
- Ca_mg_kg_whole-organism_FM
- Ti_mg_kg_whole-organism_FM
- V_mg_kg_whole-organism_FM
- Cr_mg_kg_whole-organism_FM
- Mn_mg_kg_whole-body_FM (Note: pertains to whole-body, fresh mass)
- Fe_mg_kg_whole-organism_FM
- Co_mg_kg_whole-organism_FM
- Ni_mg_kg_whole-organism_FM (often with a preceding < marker)
- Cu_mg_kg_whole-organism_FM
- Zn_mg_kg_whole-organism_FM
- As_mg_kg_whole-organism_FM
- Se_mg_kg_whole-organism_FM
- Rb_mg_kg_whole-organism_FM
- Sr_mg_kg_whole-organism_FM
- Mo_mg_kg_whole-organism_FM (often with a preceding < marker)
- Ag_mg_kg_whole-organism_FM (often with a preceding < marker)
- Cd_mg_kg_whole-organism_FM
- Cs_mg_kg_whole-organism_FM
- Ba_mg_kg_whole-organism_FM (two related columns: Ba_mg_kg_whole-organism_FM_1 and _2)
- Tl_mg_kg_whole-organism_FM (two related columns: Tl_mg_kg_whole-organism_FM_1 and _2)
- Pb_mg_kg_whole-organism_FM (two related columns: Pb_mg_kg_whole-organism_FM_1 and _2)
- U_mg_kg_whole-organism_FM (often with a preceding < marker)

## Data quality and ambiguities to note
- Some columns include “<” markers indicating censored values.
- A few concentration fields have dual columns (e.g., Ba, Tl, Pb) likely representing replicate or split measurements.
- Mn and some other fields may reference “whole-body” vs. “whole-organism” terminology in formatting; ensure consistent interpretation.
- Several descriptive fields (Latin_Species_Name, Common_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Codes, CEH_Sample_Description, Notes) have non-numeric or free-text content that may require standardization for join/analysis.

## Practical guidance for data use (Data Support perspective)
- Data integration:
  - Normalize species names (Latin and common) and standardize site names for cross-dataset analyses.
  - Link CEH_Sample_Codes to broader sample records using CEH_Sample_Description and Notes.
- Data cleaning:
  - Properly interpret and convert “<” values to appropriate censored representations or numeric bounds.
  - Resolve dual-valued columns (Ba, Tl, Pb, etc.) into a consistent long format if needed for analysis.
  - Confirm unit consistency across all concentration fields (mg/kg, fresh mass).
- Data shaping:
  - Create a tidy dataset with one concentration variable per row per sample, plus metadata (species, site, date, codes, notes).
  - Separate tissue/tissue-usage notes if more than one tissue type is involved, as indicated by Notes.
- Use cases:
  - Build dashboards showing element concentration distributions by species, site, or date.
  - Enable self-serve exploration of metal burdens in deer via pivotable views (by element, site, or species).
  - Compare concentrations against reference thresholds or environmental quality indicators.
- Quality assurance:
  - Validate sample codes against the UKCEH catalogue and verify date formats.
  - Flag and document censored values and any anomalies in the dual-column entries.

## Alignment with Data Support archetype
- This dataset exemplifies a comprehensive data product that requires careful understanding of the ask (data for deer metal concentrations with rich metadata) and effective data transformation to enable end-user self-service.
- It highlights the common challenges of patchy or variably formatted data, multiple systems for sample tracking (CEH), and the need to communicate complex information (element concentrations) in a user-friendly way.
- Providing cleaned, standardized, and well-documented outputs from this schema would enable dashboards, reports, and explorations that can be shared and re-used across teams.