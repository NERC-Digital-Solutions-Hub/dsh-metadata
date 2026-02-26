# TREE_Northumbria_ICPMS_Water_FM_Concentration

## Overview
- A dataset of ICP-MS measured concentrations of numerous elements in water from Northumbria (UKCEH context).
- Includes both the analytical results (concentrations in mg/L) and essential sampling metadata to enable spatial, temporal, and cross-element analyses.
- Core aim for data analysts: identify patterns, correlations, and build predictive insights about water chemistry and potential impacts.

## Data structure and key variables
- Sampling and sample metadata
  - CEH_Sample_Identifier: UKCEH sample code
  - CEH_Sample_Description: UKCEH sample description
  - Site: Sampling site
  - Sampling_Date: Date sample collected
  - Notes: Notes on preparation
- Concentration measurements (all in mg/L)
  - Al_mg_l, As_mg_l, B_mg_l, Ba_mg_l, Be_mg_l, Ca_mg_l, Cd_mg_l, Ce_mg_l, Co_mg_l, Cr_mg_l
  - Cs_mg_l (and a marker indicating a "<" value is used for below-detection cases)
  - Cu_mg_l, Fe_mg_l, K_mg_l, La_mg_l, Li_mg_l, Mg_mg_l, Mn_mg_l, Mo_mg_l
  - Na_mg_l, Ni_mg_l, Pb_mg_l, Pr_mg_l, Rb_mg_l, Sb_mg_l, Se_mg_l, Si_mg_l
  - Sn_mg_l, Sr_mg_l, Ti_mg_l, U_mg_l, V_mg_l, W_mg_l, Zn_mg_l
- Note: Each element has a corresponding explanation; the dataset includes some "<" notations indicating concentrations below a detection threshold for certain elements.

## Units, data quirks, and quality notes
- All concentration fields are in mg/L.
- Some fields use a less-than marker "<" to indicate censored/below-detection values (e.g., Cs_mg_l, Mo_mg_l, etc.).
- The metadata table contains a few typographical inconsistencies (e.g., wording around certain markers). Interpret cautious parsing for automated pipelines.
- Primary focus is on measured concentrations; administrative fields (sample code, site, date) enable linking to other datasets.

## Intended uses and analysis guidance
- Suitable for:
  - Exploring correlations among elemental concentrations across sites and over time.
  - Building predictive models of water chemistry from site, date, and preparation notes.
  - Identifying spatial patterns by site and temporal trends via Sampling_Date.
- Practical analysis steps:
  - Integrate with site metadata and temporal context (map by Site, plot by Sampling_Date).
  - Handle censored values appropriately (imputation or method appropriate for left-censored data).
  - Standardize units and ensure consistent handling of any typos or misformatted fields during ingestion.
  - Maintain data provenance by tracking CEH_Sample_Identifier and related metadata when sharing results.

## Data provenance and access considerations
- Source: UKCEH (Centre for Ecology & Hydrology) sample codes and descriptions; metadata includes sampling site and preparation notes.
- Enables reproducibility by linking concentrations to sample identifiers, sites, and collection dates.
- Best practice: upload datasets with metadata to data portals to improve discoverability and reusability; document data cleaning steps due to minor formatting inconsistencies in the table.