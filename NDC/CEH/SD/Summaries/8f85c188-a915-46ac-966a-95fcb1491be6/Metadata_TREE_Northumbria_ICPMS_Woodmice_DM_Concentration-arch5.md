# TREE_Northumbria_ICPMS_Woodmice_DM_Concentration

## Overview
- Dataset of concentration measurements for various elements in wood mouse tissues, acquired via ICP-MS.
- Contains metadata to aid discovery and reuse: Latin and common species names, sampling site, date collected, and UKCEH sample identifiers and descriptions.
- Concentrations are reported in milligrams per kilogram dry mass (mg/kg DM).
- Includes tissue type sampled and a Fresh Mass to Dry Mass ratio for context.
- Notes on data flags and data completeness (e.g., below-detection values, missing tissue data).

## Data Structure and Fields
- Species and identifiers
  - Latin_Species_Name
  - Common_Species_Name
- Sampling and sample metadata
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - CEH_Sample_Description
- Biological/material context
  - Tissue
  - Fresh_Mass_Dry_Mass_Ratio
- Concentration data (elements; all in mg/kg DM)
  - I_mg_kg_DM
  - Li_mg_kg_DM
  - Na_mg_kg_DM
  - Mg_mg_kg_DM
  - Al_mg_kg_DM
  - P_mg_kg_DM
  - K_mg_kg_DM
  - Ca_mg_kg_DM
  - Ti_mg_kg_DM
  - V_mg_kg_DM
  - Cr_mg_kg_DM
  - Mn_mg_kg_DM
  - Fe_mg_kg_DM
  - Co_mg_kg_DM
  - Ni_mg_kg_DM
  - Cu_mg_kg_DM
  - Zn_mg_kg_DM
  - As_mg_kg_DM
  - Se_mg_kg_DM
  - Rb_mg_kg_DM
  - Sr_mg_kg_DM
  - Mo_mg_kg_DM
  - Ag_mg_kg_DM
  - Cd_mg_kg_DM
  - Cs_mg_kg_DM
  - Ba_mg_kg_DM
  - Tl_mg_kg_DM
  - Pb_mg_kg_DM
  - U_mg_kg_DM
- Data quality and notation
  - "<" markers indicate values below a detection or reporting threshold for the corresponding concentration column.
  - Some tissues (e.g., Hind Leg Bone, woodmouse 8 liver) have missing data.
  - Some columns include notes like “tissue containing thyroid,” indicating context where relevant.
  - Several entries mention “dry mass” context or related encoding (e.g., <Sr and <Ni entries with data coding 1/2).

## Data Quality and Handling Considerations (for Data Stewards)
- Metadata completeness
  - Ensure Latin_Species_Name, Common_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Codes, and CEH_Sample_Description are consistently populated.
- Units and consistency
  - All concentrations should be standardized to mg/kg DM where applicable.
  - Verify any “dry mass” specific variants are correctly aligned with the corresponding tissue samples.
- Below-detection values
  - Properly flag and document all "<" values to preserve censoring information for downstream analyses.
- Tissue data completeness
  - Identify and document gaps (e.g., Hind Leg Bone, woodmouse 8 liver) and determine if imputation or exclusion is appropriate.
- Contextual notes
  - Respect notes about “tissue containing thyroid” where present; ensure analyses account for tissue-specific reporting differences.
- Interoperability and updates
  - Maintain provenance by documenting sample codes and descriptions; establish processes for updating the dataset while preserving versioning.
- Data governance alignment
  - Align with organisational data governance on sharing limits, data sensitivity, and catalogue integration (UKCEH/CEH metadata standards).

## Practical Use and Stewardship Guidance
- Data discovery and reuse
  - Use the metadata (species, site, date, sample codes) to filter datasets for metal exposure studies in small mammals.
- Data preparation
  - Normalize and verify units; handle below-detection values; document any tissue-specific differences (e.g., thyroid-containing tissues).
- Documentation
  - Maintain a data dictionary and data provenance notes to accompany the dataset, aiding discoverability and reproducibility.
- Quality assurance
  - Cross-check against any related datasets (e.g., other tissues or species) for consistency in measurement methods and reporting formats.
- Sharing considerations
  - Ensure access controls and sample descriptions conform to the UKCEH/CEH data sharing conventions; preserve traceability of sample codes through to publication.