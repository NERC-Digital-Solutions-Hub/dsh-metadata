# TREE_Northumbria_ICPMS_Vole_FM_Fresh_Mass_Concentration

- Purpose and scope
  - A data dictionary for a dataset of element concentrations measured in vole tissue using ICP-MS, reported as fresh mass (FM) concentrations.
  - Includes both sample metadata (species names, sampling site, collection date, UKCEH sample codes, sample preparation details, description, tissue type) and a wide panel of elemental concentrations.
  - UKCEH linkage: CEH_Sample_Codes and CEH_Sample_Description provide traceability to UKCEH records; Sample_Details describes preparation steps; Tissue notes indicate that only whole tissue was collected (no separate tissues prepared).

- Data structure and fields
  - Metadata fields:
    - Latin_Species_Name, Common_Species_Name
    - Site
    - Date_Sample_Collected
    - CEH_Sample_Codes
    - Sample_Details
    - CEH_Sample_Description
    - Tissue
    - Fresh_Mass_Ash_Mass_Ratio
  - Measurement fields (concentrations in mg/kg FM):
    - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
  - Special value handling:
    - Some columns use a less-than marker (e.g., <Be, <Ag, <U) to indicate concentrations reported as less than the detection limit.
  - Data quality notes embedded in headers:
    - Units specified as mg/kg_FM for elements; some fields use n/a or explanatory text in their descriptions.

- Metadata and provenance
  - Field explanations accompany many columns (e.g., what each species name represents, what CEH_Sample_Codes mean, what Sample_Details and Tissue describe).
  - Indicates UKCEH involvement and the use of standardized sample coding for traceability.
  - Tissue preparation note: “Notes on vole preparation (separate tissues were not prepared).”

- Data quality and governance considerations for Data Leaders
  - Handling of detection-limit values: plan for converting or flagging < values in analysis and reporting.
  - Unit consistency: ensure all measurements adhere to mg/kg_FM; verify that Fresh_Mass_Ash_Mass_Ratio is consistently calculated and interpreted.
  - Metadata completeness: confirm presence of site specifics, sampling dates, tissue type, and preparation details to support reproducibility and cross-dataset linking.
  - Data discovery and accessibility: dataset appears to be a data dictionary-style header; ensure full dataset is cataloged with clear field definitions for discoverability by policy colleagues and data consumers across networks.
  - Data quality gaps: potential issues include scattered data sources, variable data quality across sites or times, and the need for harmonization of detection limits and qualifying flags.

- Use cases and implications for decision-making
  - Ecotoxicology and wildlife exposure assessments: understanding elemental burdens in vole tissue across sites.
  - Environmental monitoring and risk assessment: supports interpretation of contaminant levels in small mammal tissue as indicators of environmental contamination.
  - Data integration and reporting: serves as a structured template to align with other datasets (e.g., other species, tissues, or regions) for comprehensive data products.

- Gaps, challenges, and recommended actions
  - Ensure complete, harmonized metadata (sampling method, site coordinates, tissue type, storage conditions, detection limits) to enable robust cross-dataset analyses.
  - Formalize treatment of non-detects (< values) and document detection limits per element.
  - Establish data stewardship roles to maintain consistency across future datasets and support iterative updates (e.g., updated sample descriptions, new sites).
  - Verify and document the provenance of the CEH_Sample_Codes and any transformations applied to raw concentrations for auditability.

- Quick takeaways for Data Leaders
  - This file represents a comprehensive data dictionary for vole tissue ICP-MS concentrations, combining rich metadata with a wide panel of elemental measurements in mg/kg fresh mass.
  - It highlights the need for clear metadata, consistent units, handling of non-detects, and strong data governance to enable reliable, discoverable data products for internal and cross-network use.