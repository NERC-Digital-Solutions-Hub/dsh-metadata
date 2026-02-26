# TREE_Northumbria_ICPMS_Frog_mg_per_tissue_FM_Concentration

## Overview
- Dataset of element concentrations in total frog tissue (fresh mass, mg_tissue_FM) measured by ICPMS.
- Includes multiple elements (I, Li, Be, Na, Mg, Al, P, K, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) across frog tissues.
- Associated metadata fields for species, sampling site, collection date, UKCEH sample codes/descriptions, and tissue type.
- Records may include “No data” indicators and occasional less-than qualifiers (e.g., <Be, <Ni).

## Data Schema and Metadata
- Core identifying fields:
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Code, CEH_Sample_Description
  - Tissue
- Concentration fields (mg_tissue_FM): I, Li, Be, Na, Mg, Al, P, K, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
- Notes on data values:
  - Some columns use a leading “<” to denote a below-detection or below-quantification value (e.g., <Be, <Ni).
  - “No data” indicates missing data for some tissues.
- Metadata quality observations:
  - Some explanations in the header appear misaligned (e.g., Ti_mg_tissue_FM, mg and its Explanation incorrectly refer to Ca; similarly, several entries have inconsistent or erroneous descriptor text).
  - Units are consistently mg, but data dictionary quality issues require correction to ensure interoperability.

## Data Governance and Sharing Considerations
- Data ownership and custody implied by CEH UK sample codes; appropriate disclosure controls and embargo considerations may apply.
- Anticipated workflow to publish: upload datasets to relevant portals and catalogues; maintain provenance and versioning; document data processing steps.
- Need to track data availability, embargoes, and any proprietary constraints before sharing.

## Quality Assurance and Curation Needs
- Data steward activities likely include:
  - Receiving data from creators and verifying accuracy, consistency, and metadata completeness.
  - Cleaning and transforming data before sharing; addressing unit and value qualifier inconsistencies.
  - Chasing up missing or incomplete data (e.g., unavailable concentrations or metadata gaps).
- Documentation requirements:
  - Compile a data dictionary and metadata schema.
  - Record data processing steps, transformations, and decisions.
  - Version-control for updates and corrections, especially given metadata mislabelings.

## Practical Implications for Data Stewards
- Ensure standardized metadata:
  - Validate species names (Latin and common), site identifiers, tissue types, and date formats.
  - Confirm alignment of CEH_Sample_Code with CEH_Sample_Description.
- Validate measurement data:
  - Correct handling of "<" qualifiers (e.g., retain as qualifiers or separate detection-limit field).
  - Resolve mislabelled explanations in the header to prevent misinterpretation of values (e.g., ensure Ti and Ca are not conflated).
  - Explicitly capture no-data cases and their implications for analyses.
- Documentation and discovery:
  - Create clear data dictionary and controlled vocabularies for species, sites, and tissues.
  - Document any data sharing restrictions and update mechanisms for new or corrected data.
- Data lifecycle:
  - Plan for updates as new samples are processed; maintain versioned releases.
  - Ensure data can be discovered and reused by others with sufficient metadata.

## Challenges and Recommendations
- Challenges highlighted (aligning with typical Data Steward concerns):
  - Incomplete user needs and priorities for this dataset.
  - Timely receipt of data from multiple creators.
  - Integration across different systems/formats and handling of large, potentially non-interoperable files.
  - Managing outdated or legacy data that require bespoke handling.
- Recommendations:
  - Implement a robust data dictionary and standardize column names and units across datasets.
  - Correct and document header metadata inconsistencies; fix misaligned explanations.
  - Establish consistent handling for below-detection values and clearly document detection limits.
  - Define governance for data availability, embargoes, and update workflows; ensure repeatable QA processes.
  - Create provenance trails and enable dataset versioning for future updates.