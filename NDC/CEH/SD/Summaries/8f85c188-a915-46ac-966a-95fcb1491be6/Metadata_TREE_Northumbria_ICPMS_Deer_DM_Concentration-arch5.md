# TREE_Northumbria_ICPMS_Deer_DM_Concentration

## Overview
- Metadata for a dataset of deer tissue concentrations measured by ICP-MS, focusing on elemental concentrations expressed as mg/kg dry mass (DM).
- Includes sample identifiers, taxonomic information, sampling site and date, UKCEH sample codes and descriptions, tissue type, and mass ratio (fresh vs dry).
- Indicates presence of censored values (less-than markers) and notes data gaps for certain samples (e.g., Roe deer 4 thyroid).

## Dataset Scope and Structure
- Species and naming:
  - Latin_Species_Name and Common_Species_Name (Latin name and common name of deer species).
- Sampling metadata:
  - Site and Date_Sample_Collected (sampling location and collection date).
  - CEH_Sample_Codes and CEH_Sample_Description (UKCEH-related identifiers and descriptions).
  - Tissue (type of deer tissue sampled).
- Sample measurements:
  - Fresh_Mass_Dry_Mass_Ratio (ratio of fresh mass to dry mass).
  - Element concentrations:
    - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM.
- Data qualifiers:
  - Some entries include “<” markers indicating concentrations reported as less-than values.
  - Several rows indicate “No data for Roe deer 4 thyroid,” highlighting sample-specific data gaps.

## Data Quality, Standards, and Conformity
- Units:
  - Most element concentrations are reported as mg/kg dry mass (DM); some fields list Units as n/a with explanations.
- Metadata completeness:
  - Core fields present (species, site, date, sample codes, tissue, mass ratio).
  - Explicitly notes data gaps for Roe deer 4 thyroid across multiple elements.
- Qualifiers:
  - Presence of censored values indicated by less-than markers (<) for several elements.
- Data consistency considerations:
  - Some metadata lines show formatting inconsistencies (e.g., duplicated or garbled field descriptions), which should be harmonized in a data dictionary.
- Implications for reuse:
  - Users should account for censored values and known data gaps when analyzing across Roe deer 4 tissue samples.
  - Ensure consistent interpretation of units and qualifiers across datasets for discovery and reuse.

## Provenance, Sampling, and Handling
- Provenance elements:
  - UKCEH-related sampling codes and descriptions indicate alignment with a broader collection or project framework.
- Sampling and handling notes:
  - Tissue type and mass-related metrics captured; date and site provide contextual provenance.
  - Fresh-to-dry mass ratio available to support normalization and comparability of concentrations.

## Access, Sharing, and Updates
- Publication and discovery:
  - Data appears intended for upload to relevant portals and catalogues (e.g., UKCEH data portals) as part of a governed data sharing process.
- Updates and governance:
  - Emphasizes systems for updates and respecting sharing limitations; implies need for versioning and change-tracking in dissemination.

## Known Gaps, Limitations, and Risks
- Data gaps:
  - No data for Roe deer 4 thyroid for many measured elements.
- Measurement qualifiers:
  - Numerous less-than values require explicit handling in analyses (censoring).
- Data quality risks:
  - Formatting inconsistencies in the metadata (duplicated descriptions, stray punctuation) may hinder automated ingestion or mapping to a standard data model.
- Interpretation cautions:
  - “n/a” units with explanations require careful mapping to a formal data dictionary to avoid misinterpretation.

## Recommendations for Data Stewardship
- Standardize metadata:
  - Clean and unify field names, units, and descriptions; ensure a formal data dictionary with consistent terminology.
- Preserve qualifiers:
  - Maintain all < values as censored data with appropriate flags in the data model (e.g., detection limits, censoring method).
- Document gaps:
  - Clearly annotate sample-specific data absence (e.g., Roe deer 4 thyroid) and provide rationale or provenance notes.
- Ensure data quality checks:
  - Validate that units are consistent across the dataset (mg/kg DM), with explicit handling for cases where units are n/a but explained.
- Improve discoverability:
  - Attach complete metadata to enable discovery across portals; ensure sample codes and descriptions align with UKCEH or other governance frameworks.
- Plan for updates:
  - Establish versioning, change logs, and update workflows to incorporate new measurements or corrections without breaking existing analyses.
- Facilitate downstream use:
  - Provide a machine-readable data dictionary, standardized variable names, and clear guidance on handling censored data to support robust re-use.