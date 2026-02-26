# TREE_Northumbria_ICPMS_Frog_Whole_Organism_FM_Concentration

## Overview
- A dataset of frog whole-organism concentrations measured by ICP-MS, with concentrations reported as mg/kg fresh mass.
- Captures both sample metadata and per-element concentration data for comprehensive cross-element analysis.
- Includes colony or study context fields such as Latin and common species names, sampling site, sample collection date, and descriptive notes.

## Key fields (data schema)
- Taxonomy and naming
  - Latin_Species_Name
  - Common_Species_Name
- Sampling and site metadata
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes (tissues used to calculate concentrations; other contextual remarks)
- Concentration data (per element; all in mg/kg fresh mass)
  - I_mg_kg_whole_organism_FM
  - Li_mg_kg_whole_organism_FM
  - Be_mg_kg_whole_organism_FM
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
- Data quality indicators (implicit in field names)
  - Some columns indicate non-detects with a “<” marker (e.g., <Be, <Ni, <U) to denote concentration values below reporting limits.
  - Some entries may include notes like “Not calculated” or descriptive explanations adjacent to concentration fields.

## Data quality and interpretation notes
- Concentrations are reported as mg/kg fresh mass, enabling direct comparisons across samples.
- Non-detects are flagged with a “<” marker for certain elements, requiring special handling in analyses (e.g., substitution or censored-data approaches).
- Some metadata fields may include formatting inconsistencies (e.g., “m g/kg” or spacing in unit names) that should be normalized during data cleaning.
- The Notes and CEH_Sample_Description fields provide context about tissues used and sampling conditions, which is important for proper interpretation and comparability.

## Potential uses for data support and end users
- Cross-sample comparisons:
  - Compare element burdens across frog species, sites, and collection dates.
- Data products and self-serve analysis:
  - Build dashboards or pivot tables to explore multi-element profiles by species or site.
  - Create summary reports and charts showing concentration distributions and trends.
- Data integration and quality improvement:
  - Harmonize units/formats, address non-detect handling, and standardize metadata for broader reuse.
  - Promote outputs and collect feedback to refine data products and encourage reuse.

## Practical considerations for working with this dataset
- Ensure consistent treatment of non-detects (< markers) in downstream analyses.
- Validate and standardize unit formatting (mg/kg fresh mass) across all concentration columns.
- Leverage the metadata (taxonomy, site, date, notes) to contextualize concentrations and support targeted analyses.
- Align data pipelines to reproduce the dataset’s structure when updating or extending with new samples.