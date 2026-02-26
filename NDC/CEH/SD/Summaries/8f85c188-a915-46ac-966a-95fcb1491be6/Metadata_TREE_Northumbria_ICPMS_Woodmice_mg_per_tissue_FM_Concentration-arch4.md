# TREE_Northumbria_ICPMS_Woodmice_mg_per_tissue_FM_Concentration

## Overview
- Dataset describing metal concentrations in wood mouse tissue, measured as mg per total tissue fresh mass (FM).
- Includes sample metadata (species, site, collection date, UKCEH sample codes and descriptions) and tissue type.
- Covers a wide range of elements measured via ICP-MS, with many columns supporting both exact values and less-than indicators.

## Data structure and content
- Identifiers and metadata
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes (UKCEH sample codes)
  - CEH_Sample_Description (UKCEH sample description)
  - Tissue (tissue type sampled)
- Measurement columns (mg_per_tissue_FM)
  - I_mg_per_tissue_FM
  - Li_mg_per_tissue_FM
  - Na_mg_per_tissue_FM
  - Al_mg_per_tissue_FM
  - P_mg_per_tissue_FM
  - K_mg_per_tissue_FM
  - Ca_mg_per_tissue_FM
  - Ti_mg_per_tissue_FM
  - V_mg_per_tissue_FM
  - Cr_mg_per_tissue_FM
  - Mn_mg_per_tissue_FM
  - Fe_mg_per_tissue_FM
  - Co_mg_per_tissue_FM
  - Ni_mg_per_tissue_FM
  - Cu_mg_per_tissue_FM
  - Zn_mg_per_tissue_FM
  - As_mg_per_tissue_FM
  - Se_mg_per_tissue_FM
  - Rb_mg_per_tissue_FM
  - Sr_mg_per_tissue_FM
  - Mo_mg_per_tissue_FM
  - Ag_mg_per_tissue_FM
  - Cd_mg_per_tissue_FM
  - Cs_mg_per_tissue_FM
  - Ba_mg_per_tissue_FM
  - Tl_mg_per_tissue_FM
  - Pb_mg_per_tissue_FM
  - U_mg_per_tissue_FM
- Notation and data quality notes
  - Some entries use “<” markers (e.g., <I, <Al, <V, <Cr, <Ni, <Mo, <Pb, <Ba) to indicate censored/less-than values.
  - “No data collected” notes for specific tissues (e.g., woodmice thyroid data missing for several elements) and for Hind Leg Bone and woodmice liver in certain cases.
  - Some cells explicitly marked as “No data” for particular tissue-element combinations.

## Provenance and accessibility
- Source context: Northumbria ICPMS Woodmice dataset with UKCEH (UK Centre for Ecology & Hydrology) sample codes and descriptions.
- Structure supports data discoverability via explicit field names and explanatory notes (e.g., where data are missing or censored).

## Data quality, gaps, and limitations
- Incomplete coverage: not all elements have data for all tissues or samples; several thyroid measurements are not collected.
- Missing tissue data: explicit absence for Hind Leg Bone and some liver measurements in certain samples.
- Censoring: presence of less-than values requires appropriate handling in analyses.
- Metadata clarity: some explanatory remarks are embedded in the field descriptions; ensure consistent interpretation across datasets.

## Opportunities and value for decision-makers
- Enables cross-site comparison of trace metal exposure in wood mice across tissues and time (where dates and sites exist).
- Supports environmental monitoring and assessment of metal contamination pathways in wildlife.
- Can inform data-driven policy discussions by providing a structured, coded dataset with provenance through UKCEH sample identifiers.

## Data governance and stewardship recommendations
- Standardize handling of censored (<) values in downstream analyses.
- Document exclusions explicitly (which tissues/elements are missing, and why) to aid data users.
- Harmonize tissue definitions and units across related datasets to improve interoperability.
- Establish a data quality checklist (completeness per site/tissue/element, metadata completeness, versioning, and update cadence).
- Promote co-ownership of the data product and engage with the wider data community to reduce duplication and improve standards.

## Practical next steps for data leaders
- Conduct a gap assessment to identify which tissue-element combinations lack data and plan targeted data collection or imputation strategies.
- Create a formal data dictionary or schema consolidating all field definitions, units, and censoring rules.
- Implement data quality rules and validation workflows (e.g., verify censoring markers, ensure consistent units, document missingness codes).
- Initiate metadata improvements to clearly describe sampling design, tissue handling, and ICP-MS methods.
- Facilitate cross-organizational collaboration to align standards and maximize the dataset’s utility across partners.