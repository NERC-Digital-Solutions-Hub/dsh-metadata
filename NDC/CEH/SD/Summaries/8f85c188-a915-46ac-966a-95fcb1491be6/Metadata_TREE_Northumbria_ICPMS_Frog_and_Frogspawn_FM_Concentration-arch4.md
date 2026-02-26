# TREE_Northumbria_ICPMS_Frog_and_Frogspawn_FM_Concentration

## Overview
- A data dictionary/schema for concentrations of elements measured by ICP-MS in frog tissue or frogspawn from Northumbria. The dataset links species information, sampling details, tissue type, and per-element concentration measurements in milligrams per kilogram of fresh mass (mg/kg_fresh_mass).

## Key Data Schema (main fields)
- Biological and taxonomic identifiers:
  - Latin_Species_Name
  - Common_Species_Name
- Sampling and sample identifiers:
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
- Tissue and sample characteristics:
  - Tissue (e.g., frog tissue or frogspawn)
  - Fresh_Mass_Dry_Mass_Ratio
- Element concentration measurements (mg/kg_fresh_mass):
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM
  - P_mg_kg_FM, K_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM
  - Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM
  - Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM
  - Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM
  - Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Data qualifiers and notes:
  - Some columns use “<” to indicate concentrations below detection limits (e.g., <Be, <Ni, <Se, <U, <Ag, <Ba)
- Metadata quality notes:
  - There are inconsistencies in the provided column explanations (some lines incorrectly map elements to “Concentration of Ca” in explanations), indicating documentation errors alongside the data.

## Data Quality and Metadata Considerations
- Units and mass basis:
  - Concentrations are reported as mg/kg_fresh_mass (FM); ensure consistent interpretation across analyses.
- Qualifiers:
  - Detection-limit indicators (<) must be handled appropriately in analyses (censored data considerations).
- Metadata integrity:
  - Several field descriptions appear corrupted or mislabelled (e.g., incorrect “Concentration of Ca” references). This affects clarity and automated processing; plan for metadata cleansing and field re-documentation.
- Gaps and accessibility:
  - Some fields show n/a for units; verify and standardize units metadata.
  - Sample identifiers (CEH_Sample_Codes) suggest linkage to broader metadata; ensure proper data lineage and discoverability.
- Data governance implications:
  - To support data products for policy or partner networks, provide corrected, consistent metadata, confirm unit consistency, and implement data quality checks prior to ingestion into data platforms.

## Uses and Implications for Data Strategy
- Potential uses:
  - Comparative analyses of elemental exposure across species, sites, and time.
  - Environmental monitoring and ecological risk assessments based on tissue contaminant burdens.
  - Integration with other datasets (e.g., location, habitat, or additional chemical suites) for broader environmental assessments.
- Data strategy considerations:
  - Establish a clean, machine-readable data dictionary with consistent field names, units, and validations.
  - Implement data quality rules for detection-limit handling, out-of-range values, and metadata completeness.
  - Link sample codes to richer metadata repositories to improve discoverability and reusability.
  - Align with data standards across the network to reduce duplication of effort and improve cross-site coordination.

## Challenges Highlighted
- Understanding and documenting data provenance and metadata quality (corrupted field explanations and potential mislabeling).
- Achieving consistent data standards across diverse measurements and potential downstream consumers.
- Ensuring complete and discoverable metadata (sample site, date formats, and sample descriptions) to support effective data sharing and reuse.