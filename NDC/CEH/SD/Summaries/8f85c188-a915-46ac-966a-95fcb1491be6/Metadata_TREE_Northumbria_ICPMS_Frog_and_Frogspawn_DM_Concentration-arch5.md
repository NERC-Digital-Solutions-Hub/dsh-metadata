# TREE_Northumbria_ICPMS_Frog_and_Frogspawn_DM_Concentration

## Overview
- A dataset of ICP-MS-derived concentrations for numerous elements in frog and frogspawn tissues from Northumbria.
- Includes specimen-level metadata (Latin and common species names), sampling details (site, date), UKCEH sample codes and descriptions, tissue type, and mass-related metrics.
- Concentrations are reported as milligrams per kilogram dry mass (mg/kg DM), with explicit handling for detection limits.

## Dataset Structure
- Taxonomic fields: Latin_Species_Name, Common_Species_Name
- Sampling/Location metadata: Site, Date_Sample_Collected
- UKCEH/CEH metadata: CEH_Sample_Codes, CEH_Sample_Description
- Biological material: Tissue, Fresh_Mass_Dry_Mass_Ratio
- Concentration data (example elements): I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM (with <Be indicating a value below detection), B_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM (with <Al for below detection), P_mg_kg_DM, S_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM (with <Ni for below detection), Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM (with <Se), Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM (with <Ag), Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM (with <Ba), Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM
- Note: Some columns include markers indicating concentrations below detection limits and a few header explanations indicate n/a for units in those spots.

## Key Data Fields (highlights)
- Species identifiers: Latin_Species_Name, Common_Species_Name
- Sampling context: Site, Date_Sample_Collected
- Sample management: CEH_Sample_Codes, CEH_Sample_Description
- Tissue analysis: Tissue, Fresh_Mass_Dry_Mass_Ratio
- Concentration measurements: wide suite of elements (I, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U) with concentrations expressed as mg/kg DM
- Detection-limit indicators: entries prefixed with "<" (e.g., <Be, <Al, <Ni, <Ag, <Se, <Ba) to denote values below detection limits

## Metadata, Provenance, and Documentation
- CEH_Sample_Codes and CEH_Sample_Description provide traceability to UKCEH sample records
- Date_Sample_Collected and Site anchor the temporal and spatial context
- Latin_Species_Name and Common_Species_Name enable cross-referencing with taxonomic databases
- Documentation of what each concentration column represents (mg/kg DM) and the meaning of lower-detection values

## Data Quality and Standards Considerations
- Consistent unit usage: mg/kg DM across concentration fields
- Explicit handling of non-detects via <value markers
- Clear metadata for discoverability and reuse (species, site, date, sample codes)
- Some header explanations use n/a, highlighting spots where unit specification is not applicable
- Potential interoperability considerations due to the breadth of elements and legacy or multiple system formats

## Governance and Data Stewardship Implications
- Metadata completeness: maintain comprehensive data dictionary and field definitions (as provided)
- Standardization: ensure uniform units, column naming, and controlled vocabularies for Site, Tissue, and CEH sample descriptors
- Data provenance: track transformations, QA steps, and any data cleaning before sharing
- Update and sharing workflow: document update cycles, embargo status, and portal deposition processes
- Accessibility: ensure the dataset is uploaded to appropriate data portals and remains discoverable and reusable

## Challenges and Considerations for Data Stewards
- Incomplete picture of user needs and priorities for this multifield dataset
- Timeliness of data delivery and synchronization with related datasets
- Ensuring all data creators meet metadata and standardization expectations
- Managing multiple systems and formats, including handling non-interoperable elements
- Handling large concentration datasets and potential legacy databases

## Recommendations for Management and Reuse
- Maintain and publish a robust data dictionary and data quality checks
- Use consistent units (mg/kg DM) and clearly document any exceptions
- Explicitly document detection limits and their impact on analyses (e.g., record <value interpretations)
- Apply versioning and provenance tracking for each update
- Align with broader data governance practices: update workflows, embargo policies, and data access controls
- Facilitate data discovery by linking to species, site, and sample metadata across portals

- Use cases: environmental monitoring, ecological risk assessment, and biodiversity studies requiring comparable elemental concentration data in amphibian tissues