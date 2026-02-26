# TREE_Northumbria_ICPMS_Deer_FM_concentration

## Overview
- Data dictionary / dataset description for ICP-MS concentrations in deer tissues.
- Captures taxonomy (species), sampling metadata (site, date, sample codes and descriptions), tissue type, and concentrations of numerous elements as mg/kg fresh mass (FM).
- Includes flags and qualifiers such as "<" (less-than) values and explicit notes of missing data (e.g., "No data for Roe deer 4 thyroid" for several fields).

## Data Schema and Key Fields
- Species and site information
  - Latin_Species_Name: Latin name of species
  - Common_Species_Name: Common name of species
  - Site: Sampling site
  - Date_Sample_Collected: Date the sample was collected
  - CEH_Sample_Codes: UK CEH sample code
  - CEH_Sample_Description: Description of the UKCEH sample
  - Tissue: Deer tissue sampled
  - Fresh_Mass_Dry_Mass_Ratio: Fresh-to-dry mass ratio

- Concentration data (mg/kg FM)
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
  - Explanation and units: Each field represents the concentration of the corresponding element in milligrams per kilogram of fresh mass.
  - Notes on data qualifiers: Several fields include "<" markers indicating a 'less than' value; some entries are explicitly labeled as "<marker is used to identify concentration given in column X_mg_kg_FM is a 'less than' value."
  - Data gaps: Repeated notes such as "No data for Roe deer 4 thyroid" indicate missing data for Roe deer 4 thyroid across multiple elements.

## Data Quality, Gaps, and Data Management Considerations
- Data quality notes
  - Mixed formatting and some typographical inconsistencies in the field explanations (e.g., spacing and underscores).
  - Presence of non-detects or censored data indicated by "<" qualifiers.
  - Frequent explicit missing data notes for Roe deer 4 thyroid across many elements.

- Data coverage and granularity
  - Contains broad suite of elements but with targeted gaps (e.g., Roe deer 4 thyroid data missing for numerous analytes).
  - Metadata provides sampling context but may require harmonization for cross-dataset comparability.

- Metadata and discoverability implications
  - Clear field-level descriptions are present, but parsing requires consistent naming and handling of non-detects.
  - Provenance hints (CEH UK codes, Northumbria context) are present but could be better captured in a structured metadata record.

## Metadata, Provenance, and Intended Use
- Provenance signals
  - CEH_SAMPLE_CODES and CEH_SAMPLE_DESCRIPTION indicate UK CEH origin.
  - Date_Sample_Collected and Site provide temporal and spatial context.
  - Latin and Common species names enable cross-referencing with taxonomic data.

- Intended use
  - Mapping and comparing trace element concentrations across deer tissues and samples.
  - Integration with broader data on wildlife exposure, environmental monitoring, and public health assessments.

## Practical Guidance for Data Leaders
- Data governance and standardization
  - Harmonize field names and ensure consistent unit usage (mg/kg FM across all element columns).
  - Establish a standard approach for non-detects and '<' values (e.g., censoring method, reporting limits).

- Data quality improvements
  - Address visible formatting inconsistencies to improve machine readability.
  - Fill in known data gaps (notably Roe deer 4 thyroid) or clearly annotate as missing with metadata.

- Metadata enrichment and discoverability
  - Create a structured metadata record detailing dataset origin, sampling protocol, tissue types, and analytical methods (ICP-MS).
  - Link to related datasets (e.g., site characteristics, animal demographics, sampling methods) to enable holistic analysis.

- Data integration and governance actions
  - Maintain explicit notes for missing data by sample/id to support downstream analyses.
  - Ensure qualifiers (such as "<" values) are consistently represented in downstream data apps or analyses.