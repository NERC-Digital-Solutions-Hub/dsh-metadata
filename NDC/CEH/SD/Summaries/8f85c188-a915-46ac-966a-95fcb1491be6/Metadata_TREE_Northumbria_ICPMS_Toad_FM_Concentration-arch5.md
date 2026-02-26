# TREE_Northumbria_ICPMS_Toad_FM_Concentration

## Overview
- Metadata-backed dataset of ICP-MS concentrations in toad tissue from Northumbria, with associated taxonomic and sampling metadata.
- Concentrations are reported as milligrams per kilogram of fresh mass (FM) for a broad suite of elements, alongside sample descriptors and preparation notes.

## Dataset structure and key fields
- Core identifiers and taxonomy
  - Latin_Species_Name; Common_Species_Name
- Sampling and site information
  - Site; Date_Sample_Collected
- Sample identifiers and descriptions
  - CEH_Sample_Code; CEH_Sample_Description
- Sample characterization
  - Fresh_Mass_Ash_Mass_Ratio: ratio of whole-body fresh mass to ash mass
  - Notes: information related to toad preparation (e.g., whether separate tissues were prepared)
- Elemental concentrations (all in mg/kg_FM)
  - I_mg_kg_FM; Li_mg_kg_FM; Be_mg_kg_FM; Na_mg_kg_FM; Mg_mg_kg_FM; Al_mg_kg_FM; P_mg_kg_FM; K_mg_kg_FM; Ca_mg_kg_FM; Ti_mg_kg_FM; V_mg_kg_FM
  - Mn_mg_kg_FM; Fe_mg_kg_FM; Co_mg_kg_FM; Ni_mg_kg_FM; Cu_mg_kg_FM; Zn_mg_kg_FM; As_mg_kg_FM; Se_mg_kg_FM; Rb_mg_kg_FM; Sr_mg_kg_FM; Mo_mg_kg_FM
  - Ag_mg_kg_FM; Cd_mg_kg_FM; Cs_mg_kg_FM; Ba_mg_kg_FM; Tl_mg_kg_FM; Pb_mg_kg_FM; U_mg_kg_FM
- Data quality and consistency notes
  - Some field descriptions appear misaligned or contain typographical errors (e.g., explanations repeating “Concentration of Cr” for multiple elements). These should be validated against a consistent data dictionary.

## Data quality, metadata, and governance considerations
- Metadata completeness
  - Ensure species names, site, date collected, and UKCEH-related codes/descriptions are complete and traceable.
- Field consistency and validation
  - Validate that element field names match standard nomenclature (I, Li, Be, Na, Mg, …, U) and that units are consistently mg/kg_FM.
  - Resolve inconsistencies in Explanation text (avoid mislabeled descriptions such as repeated “Concentration of Cr”).
- Units and scale
  - All concentrations should be recorded as mg/kg_FM; confirm that Fresh Mass (FM) handling is consistent across records.
- Provenance and traceability
  - CEH_Sample_Code and CEH_Sample_Description link to UKCEH records; maintain these relationships for data provenance.
- Handling missing data
  - Address fields that may be n/a or missing; document any data gaps and retrieval status.
- Data sharing and interoperability
  - Prepare for ingestion into portals and data catalogs; ensure stable identifiers and clean metadata to support discovery and reuse.
- Embargoes and licensing
  - Confirm any data access restrictions or licensing before dissemination.

## Practical considerations for Data Stewards
- Data ingestion and curation
  - Validate and harmonize field names, units, and descriptions before publishing.
  - Cross-check element list against standard ICP-MS panels to ensure completeness.
- Documentation and explainers
  - Include clear notes on sample preparation, mass measurements, and any tissue-specific handling.
  - Provide a data dictionary mapping each field to a controlled vocabulary.
- Long-term stewardship
  - Version datasets when corrections are made; maintain audit trails linking CEH sample records with dataset entries.
- Reuse and downstream analyses
  - The dataset supports toxicology and nutritional assessments in amphibians; ensure metadata supports such analyses (e.g., sampling date, site context).

## Endnotes and cautions
- The document contains typographical inconsistencies in element explanations; verification against a canonical data dictionary is recommended to ensure accurate interpretation of all element fields.