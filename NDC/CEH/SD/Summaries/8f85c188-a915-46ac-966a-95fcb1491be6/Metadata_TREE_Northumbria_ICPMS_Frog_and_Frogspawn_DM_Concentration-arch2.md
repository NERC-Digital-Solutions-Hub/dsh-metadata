# TREE_Northumbria_ICPMS_Frog_and_Frogspawn_DM_Concentration

## Overview
- Dataset of element concentrations measured by ICP-MS in frog tissue or frogspawn samples.
- Sourced from Northumbria-related monitoring context with UKCEH identifiers; designed to support environmental health assessment over time.
- Focuses on dry-mass concentrations (mg/kg DM) across multiple elements; includes metadata for reproducibility and QA.

## Columns and Measurements
- Taxonomy and sample identifiers:
  - Latin_Species_Name, Common_Species_Name
  - Site (sampling location), Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue (frog tissue or frogspawn)
- Sample characteristics:
  - Fresh_Mass_Dry_Mass_Ratio
- Concentration data (mg/kg DM) for a large suite of elements, each with:
  - Element-specific column (e.g., I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, …, U_mg_kg_DM)
  - Explanation for each: "Concentration of [Element] in milligram per kilogram dry mass"
  - Some elements flagged with a < indicator (e.g., <Be, Ni, <Al, <Se, <Ag, <Ba, <U) indicating a censored value (less than detection limit) in the corresponding concentration column
- Notes on column formats:
  - Several columns include a marker explanation (e.g., "< marker is used to identify concentration given in column X_mg_kg_DM is a 'less than' value")
  - Units consistently mg/kg DM for concentrations; Fresh_Mass_Dry_Mass_Ratio is unitless

## Sampling Metadata and Context
- Tissue type specified to distinguish frog tissue vs. frogspawn
- Date and site information enable temporal and spatial comparisons
- CEH sample codes and descriptions provide traceability to UKCEH sample handling and documentation

## Data Quality, Standardisation and Usage
- Data are intended to be verified, quality assured, cleaned, and transformed as part of standardised monitoring workflows
- Outputs typically include reports, maps, and charts to illustrate environmental health against standards
- Datasets are stored/uploaded to appropriate data portals, enabling long-term monitoring and cross‑dataset analysis

## Accessibility and Reuse Considerations
- Emphasis on enabling access to underlying data used to create final outputs
- Encourages combining this dataset with other relevant data to increase its value for monitoring and policy evaluation
- Designed to support consistency in environmental health assessment over time and across sites through standardised fields and codes