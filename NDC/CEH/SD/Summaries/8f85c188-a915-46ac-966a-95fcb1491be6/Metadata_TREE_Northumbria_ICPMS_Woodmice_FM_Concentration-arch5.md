# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration

## Overview
- Dataset documenting ICP-MS concentrations of multiple elements in wood mice, measured as mg/kg of fresh mass (FM).
- Captures contextual metadata to enable discovery and reuse:
  - Species identification (Latin and common names)
  - Sampling site and collection date
  - UKCEH sample codes and description
  - Tissue sampled and fresh:dry mass ratio
- Contains a wide suite of elements (I, Li, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) with tissue-specific notes.
- Some data gaps and caveats are noted (e.g., no data for Hind Leg Bone and woodmouse 8 liver; certain elements have tissue-specific applicability).

## Data structure and key fields
- Species and specimens
  - Latin_Species_Name, Common_Species_Name
  - Site, Date_Sample_Collected
- Sample identifiers and description
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue (name of sampled wood mouse tissue)
- Mass and measurement context
  - Fresh_Mass_Dry_Mass_Ratio
  - I_mg_kg_FM, Li_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Data conventions and qualifiers
  - Some columns include “<” markers indicating concentrations below the detection limit
  - “Tissue containing thyroid” notes apply to certain elements
  - Punctuation and header formatting inconsistencies (e.g., “Ra tio”) noted in the schema
  - Some datasets show paired columns where 1 = mg/kg and 2 = fresh mass

## Data quality and metadata quality considerations
- Completeness and gaps
  - Explicit note: No data for Hind Leg Bone and woodmouse 8 liver
  - Some tissues or measurements may be missing across samples
- Units and consistency
  - Concentrations presented as mg/kg_FM; ensure uniform verification across all records
  - Mixed header labeling and formatting issues requiring cleanup for machine readability
- Handling of below-detection values
  - "<" markers indicate concentrations below detection limits; require a consistent approach (e.g., censoring, NLPIR qualifiers, or metadata on detection thresholds)
- Tissue-specific applicability
  - Several elements flagged with “Tissue containing thyroid,” implying tissue-dependent reporting rules; harmonization needed for cross-tissue comparisons
- Metadata richness
  - Strong contextual fields (site, date, sample codes, tissue) supporting traceability and data lineage
  - Cross-references to UKCEH sample codes and descriptions support data integration across portals

## Data governance and sharing implications
- Publication and discoverability
  - Dataset is designed for uploading to relevant portals and cataloguing within a data holdings system
  - UKCEH sample codes and CEH_ fields support cross-dataset linking and reuse
- Standards and interoperability
- Versioning and provenance
  - Maintain clear version history to track updates to measurements, tissue categorizations, and metadata descriptions
- Access and rights
  - Consider embargo or proprietary constraints if any; align with organisational data sharing policies
- Documentation needs
  - Provide a clean, machine-readable metadata schema (standardized field names, units, and controlled vocabularies) to accompany the dataset

## Notable challenges to address
- Incomplete user needs picture could affect metadata granularity and suitability for reuse
- Timely ingestion of data from diverse sources and formats
- Achieving consistent adherence to data standards across data creators, especially for metadata like tissue types and date formats
- Interoperability across many elements and potential tissue-specific reporting rules
- Handling large, multi-element datasets across various tissues and samples

## Practical recommendations for Data Stewards
- data cleaning and standardization
  - Correct header typos and standardize field names (e.g., unify “Fresh_Mass_Dry_Mass_Ratio” spelling)
  - Enforce consistent units (mg/kg_FM) across all element fields
  - Normalize tissue names and ensure a controlled vocabulary
- metadata completeness and quality
  - Ensure presence of Latin_Species_Name, Common_Species_Name, Site, Date_Sample_Collected, CEH_Sample_Codes
  - Document tissue-specific notes clearly; separate tissue qualifiers from numeric data where possible
- handling below-detection limits
  - Capture detection limits per analysis and apply a consistent rule for < values (e.g., report as <DL and store DL, or use censoring approach)
- data lineage and provenance
  - Maintain a clear data provenance log (sampling method, ICP-MS method, calibration, QA/QC steps)
- data governance practices
  - Implement schema-driven validation rules before upload
  - Use controlled vocabularies and drop-down lists for site, tissue, and sample descriptors
  - Establish a clear process for updates and version control; document any data corrections
- accessibility and reuse
  - Provide a detailed data dictionary and an accompanying readme explaining units, qualifiers, and any tissue-specific caveats
  - Ensure portal-ready metadata with cross-references to UKCEH CEH_Sample_Codes and descriptions

## Summary for Data Stewards
- TREE_Northumbria_ICPMS_Woodmice_FM_Concentration is a multi-element, tissue-specific concentration dataset for wood mice, with rich contextual metadata and a focus on mg/kg_FM concentrations, including numerous detection-limit qualifiers and tissue-specific notes (e.g., thyroid-containing tissues). While comprehensive, the dataset includes data gaps and formatting irregularities that require careful metadata standardization, unit consistency, and robust handling of below-detection values. Implement structured governance, standardize metadata, and establish clear data quality checks to ensure the dataset is reliably discoverable, interpretable, and reusable by data users.