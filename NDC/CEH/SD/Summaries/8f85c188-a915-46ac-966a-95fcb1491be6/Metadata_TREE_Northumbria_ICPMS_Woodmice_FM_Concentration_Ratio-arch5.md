# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

## Overview
- A dataset describing concentration ratios of multiple elements in woodmice (whole body) relative to dry soil mass, using a co-located soil sample to calculate the ratio.
- Includes detailed sample metadata to support traceability and reuse.
- Captures a wide range of elemental concentration ratios (e.g., I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) with qualifiers for special cases (e.g., less-than indicators).

## Key Dataset Elements
- Species and identification
  - Latin_Species_Name
  - Common_Species_Name
- Sampling and location
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes (related to Woodmice sample)
- Data lineage and context
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio (description of the soil sample used)
  - I_Concentration_Ratio and multiple element-specific Concentration_Ratio fields
    - Examples include Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
  - For several elements, there are two related columns (denoted 1 and 2) with 1 often indicating a non-applicable placeholder and 2 providing the actual concentration ratio description (e.g., “Concentration Ratio (Fresh Mass Woodmice (wholebody) divided By Dry Mass Soil)”).

## Data Quality and Governance Considerations
- Metadata completeness and clarity
  - Some units are listed as n/a; ensure consistent unit definitions or provide a formal data dictionary.
  - Ensure all field explanations are explicit and aligned with the dataset’s metadata schema.
- Data accuracy and standardization
  - Standardize species names (Latin and common) and site identifiers for interoperability across systems.
  - Ensure correct handling of less-than qualifiers in concentration ratios (e.g., “<I”, “<Be”, “<Ni”, “<Ag”, “<Tl”, “<U”) and clearly document their interpretation.
- Provenance and traceability
  - Maintain clear linkage between woodmice samples and the co-located soil samples used to compute the ratios.
  - Document any data transformations or cleaning steps applied before sharing.
- Data sharing and access
  - Prepare clear data usage licenses and sharing conditions to enable discoverability and reuse while respecting any embargoes or sensitivities.
  - Upload to appropriate data portals and ensure dataset is discoverable via the included metadata fields.
- Data lifecycle and updates
  - Establish a process for updating records as new samples are collected or recalculations are performed.
  - Implement versioning and change-log practices to preserve historical states.

## Practical Considerations for Data Stewards
- Interoperability and formats
  - Consider mapping to a common schema (e.g., a standard environmental metadata model) to facilitate cross-dataset analyses.
  - Resolve any inconsistencies in the element column naming (e.g., items with dual-column representations) to ensure consistent downstream usage.
- Documentation and accessibility
  - Provide a comprehensive data dictionary that covers all Concentration_Ratio fields, including the meaning of 1 vs 2 suffixes and any qualifiers.
  - Include examples or a data snippet to illustrate how ratios are calculated (e.g., “Fresh Mass Woodmice divided by Dry Mass Soil”).
- Quality assurance workflows
  - Validate that each row includes required metadata (species, site, collection date, soil reference) before sharing.
  - Implement checks for out-of-range or implausible concentration ratios and annotate any known issues in the Notes field.

## Potential Risks and Limitations
- Incomplete or ambiguous metadata (e.g., missing units) could hinder reuse; address with a formal data dictionary.
- Complex or inconsistent representation of concentration ratio columns (1 vs 2) may cause misinterpretation without clear guidance.
- Large numbers of elemental fields increase the burden of consistent data curation and quality control.

## Recommended Actions for Data Stewards
- Create and publish a complete data dictionary for all fields, especially Concentration_Ratio columns and their qualifiers.
- Standardize units or explicitly declare unit meanings where n/a is currently used.
- Document data lineage from sample collection through to ratio calculation and sharing.
- Establish a robust update and versioning policy and apply it to all dataset revisions.
- Ensure the dataset is accessible via appropriate data portals with clear licensing and usage terms.