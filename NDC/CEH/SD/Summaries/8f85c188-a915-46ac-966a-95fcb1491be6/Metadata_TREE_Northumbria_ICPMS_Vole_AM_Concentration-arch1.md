# TREE_Northumbria_ICPMS_Vole_AM_Concentration

## Overview
- Dataset documenting ICP-MS concentrations of multiple elements in vole ash, linked to sampling at Northumbria (UK CEH context).
- Includes taxonomic identifiers, sampling metadata, sample preparation notes, and ash-mass–based element concentrations.
- Designed for extracting patterns, correlations, and potential predictive relationships relevant to ecological exposure and contaminant assessment.

## Key Data Fields
- Taxonomy and naming
  - Latin_Species_Name
  - Common_Species_Name
- Sampling and site context
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes (UKCEH sample codes)
  - CEH_Sample_Description
  - Sample_Details (preparation notes)
  - Notes (e.g., vole preparation details)
- Fresh/ash mass relation
  - Fresh_Mass_Ash_Mass_Ratio
- Element concentrations (all in mg/kg, ash mass basis)
  - I_mg_kg_AM
  - Li_mg_kg_AM
  - Be_mg_kg_AM (and <Be_mg_kg_AM for censored values)
  - Na_mg_kg_AM
  - Mg_mg_kg_AM
  - Al_mg_kg_AM
  - P_mg_kg_AM
  - K_mg_kg_AM
  - Ti_mg_kg_AM
  - V_mg_kg_AM
  - Cr_mg_kg_AM
  - Mn_mg_kg_AM
  - Fe_mg_kg_AM
  - Co_mg_kg_AM
  - Ni_mg_kg_AM
  - Cu_mg_kg_AM
  - Zn_mg_kg_AM
  - As_mg_kg_AM
  - Se_mg_kg_AM
  - Rb_mg_kg_AM
  - Sr_mg_kg_AM
  - Mo_mg_kg_AM
  - Ag_mg_kg_AM (and 1/2 replicates for Ag_mg_kg_AM)
  - Cd_mg_kg_AM (and 1/2 replicates for Cd_mg_kg_AM)
  - Cs_mg_kg_AM (and 1/2 replicates for Cs_mg_kg_AM)
  - Ba_mg_kg_AM (and 1/2 replicates for Ba_mg_kg_AM)
  - Tl_mg_kg_AM (and 1/2 replicates for Tl_mg_kg_AM)
  - Pb_mg_kg_AM (and 1/2 replicates for Pb_mg_kg_AM)
  - U_mg_kg_AM (and 1/2 replicates for U_mg_kg_AM)
- Data nuances
  - Some columns use a less-than indicator (e.g., <Be_mg_kg_AM, <Ag_mg_kg_AM, <U_mg_kg_AM)
  - Certain column descriptions contain inconsistencies (e.g., descriptions referencing "Concentration of Ca" where the column is a different element); these should be treated as metadata issues during cleaning.

## Data Quality and Cleaning Considerations
- Presence of censored values (< value) requiring special handling (limit of detection considerations).
- Replicate columns (e.g., Ag_mg_kg_AM, 1 and 2; Cd_mg_kg_AM, 1 and 2; etc.) necessitate alignment and aggregation rules.
- Some descriptive text inconsistencies in the metadata (likely copy/paste errors) to be reconciled during data preparation.
- Notes indicate sample preparation details (no separate tissues prepared), which is important for interpretation of concentrations.

## How to Use
- Compare element profiles across sites, dates, and vole species.
- Correlate element concentrations with Fresh_Mass_Ash_Mass_Ratio to explore mass-basis effects.
- Conduct multivariate analyses (PCA, clustering) to identify patterns in exposure or trophic transfer.
- Build predictive models of contaminant burden based on site, date, and sample characteristics.
- Handle censored data appropriately (imputation or Tobit-type models) and account for replicates in analyses.

## Provenance and Access
- Linked to UK Centre for Ecology and Hydrology (UKCEH) sample coding; data appear structured for discoverability and reproducibility with metadata and source tracking.

## Practical Considerations for Analysts
- Validate unit consistency (mg/kg on ash mass basis) and reconcile any inconsistent element descriptors.
- Develop a clear strategy for censored (<) values and replicate columns before modeling.
- Consider local-scale scope and potential data integration challenges with other datasets (as noted in typical analyst challenges).