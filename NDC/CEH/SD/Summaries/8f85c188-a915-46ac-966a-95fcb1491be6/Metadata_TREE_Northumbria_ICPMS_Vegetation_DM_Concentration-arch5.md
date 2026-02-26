# TREE_Northumbria_ICPMS_Vegetation_DM_Concentration

- Dataset contains ICP-MS concentration measurements in vegetation from Northumbria, with detailed sample and specimen metadata.
- Purpose for data stewards: ensure dataset is well-governed, Discoverable, reusable, and interoperable across portals and downstream analyses.

## Key data model and fields

- Species and site metadata
  - Latin_Species_Name: Latin name of species
  - Common_Species_Name: Common name of species
  - Site: Sampling site
  - Date_Sample_Collected: Date sample collected
  - CEH_Sample_Identifier: UKCEH sample identifier
  - CEH_Sample_Description: UKCEH sample description
- Sample and description fields
  - n/a notes and explanatory placeholders
  - <I, <Li, <Be, <Cr, <As, <Tl, <Pb, <U: markers indicating that the corresponding concentration value is a 'less-than' value
- Concentration measurements (units = mg/kg dry mass, unless noted otherwise)
  - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM
  - Some elements have paired or numbered fields to express and capture less-than values (e.g., Se_mg_kg_DM, 1 and Se_mg_kg_DM, 2; similarly for other elements with the < marker)
- Data interpretation notes
  - Most concentration values represent the concentration of the element in milligrams per kilogram dry mass (mg/kg DM)
  - The dataset includes explanatory text for each field to support consistent interpretation, data quality, and reuse

## Measurement, units, and data quality considerations

- Primary units: mg/kg dry mass for elemental concentrations
- Date and site information critical for traceability and reproducibility
- Presence of both Latin and Common species names supports cross-database interoperability
- Special handling for non-detects or below-threshold values via dedicated less-than fields
- Rich metadata (sample identifiers, descriptions) aids provenance tracking and dataset integration with UKCEH systems

## Governance, sharing, and provenance considerations

- Metadata richness supports discovery, reuse, and interoperability across data portals
- Clear provenance: sampling site, collection date, and UKCEH identifiers enable end-to-end traceability
- Data sharing and update workflow should respect potential sharing limitations and embargo scenarios
- Upload to relevant portals and cataloguing of data holdings recommended; maintain record of data processing steps (quality assurance, cleaning, transformation)
- Documentation of work performed on datasets (e.g., QA/QC, transformations) advisable for reproducibility

## Challenges and considerations for Data Stewards

- Incomplete or inconsistent user needs or metadata may hinder discoverability and reuse
- Timely receipt of data from multiple creators or teams
- Ensuring consistent application of species naming conventions and metadata quality
- Managing multiple systems/formats and large, multi-element datasets
- Handling legacy databases that may require bespoke, non-interoperable solutions
- Ensuring up-to-date data sharing while respecting access and embargo constraints

## Practical takeaways for users and custodians

- The dataset provides a comprehensive schema for vegetation ICP-MS concentration data with robust metadata
- Key governance actions: enforce standard metadata, preserve provenance, manage less-than values consistently, and ensure data are accessible via appropriate portals
- Maintain documentation of data processing steps and update mechanisms to support ongoing usability and compliance with data governance standards