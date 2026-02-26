# Supporting documentation for 10-Animal_Foodstuff_Stable.csv

- Purpose and scope
  - Metadata and field explanations for a dataset of stable element concentrations in animal-derived foodstuffs.
  - Measures include Cs, Sr, K, Na, Ca, Mg, P, Pb, U, and Th, reported as concentrations on a fresh mass basis (mg/kg_fm) or mg/L for milk.
  - Each analyte has associated uncertainty (Unc_ fields) and detection limit (Detection_Limit_ fields) to support data quality assessment and comparability.

- Key variables and structure
  - Core identifiers:
    - Sample_Code: Unique sample identifier.
    - Sample_Type: General description of the sample group.
  - Context and collection:
    - Location: Location where the sample was collected.
    - Collection_Date: Date of sampling (dd-mm-yyyy).
    - Sample_size: Amount analyzed (g fresh matter or mL for milk).
    - Sample_Description: Part of the organism analyzed (where applicable).
  - Analyte data (examples shown; each with corresponding Unc_ and Detection_Limit_ fields):
    - Cs_mg/kg_fm, Unc_Cs_mg/kg_fm, Detection_Limit_Cs_mg/kg_fm
    - Sr_mg/kg_fm, Unc_Sr_mg/kg_fm, Detection_Limit_Sr_mg/kg_fm
    - K_mg/kg_fm, Unc_K_Mg/kg_fm, Detection_Limit_K_mg/kg_fm
    - Na_mg/kg_fm, Unc_Na_mg/kg_fm, Detection_Limit_Na_mg/kg_fm
    - Ca_mg/kg_fm, Unc_Ca_Mg/kg_fm, Detection_Limit_Ca_mg/kg_fm
    - Mg_mg/kg_fm, Unc_Mg_mg/kg_fm, Detection_Limit_Mg_mg/kg_fm
    - P_mg/kg_fm, Unc_P_mg/kg_fm, Detection_Limit_P_mg/kg_fm
    - Pb_mg/kg_fm, Unc_Pb_mg/kg_fm, Detection_Limit_Pb_mg/kg_fm
    - U_mg/kg_fm, Unc_U_mg/kg_fm, Detection_Limit_U_mg/kg_fm
    - Th_mg/kg_fm, Unc_Th_mg/kg_fm, Detection_Limit_Th_mg/kg_fm
  - Units and conventions:
    - Primary units are mg/kg_fm (fresh mass basis) for most elements; mg/L is used for milk where applicable.
    - Non-detects are indicated by blanks or notes specifying concentration below the detection limit.
    - Uncertainty fields represent the combined uncertainty of the concentration measurement.

- Data quality and governance implications
  - Metadata completeness and clarity are crucial for reuse and comparability; some entries mix field naming and formatting (e.g., inconsistent numeration and labeling) which could hinder interoperability.
  - The explicit inclusion of detection limits and uncertainties enhances transparency and enables consistent data interpretation across datasets.
  - Clear documentation is needed for data sharing, metadata standards, versioning, and provenance to support governance and open data practices.
  - Standardized data formats and consistent naming conventions are important to avoid misinterpretation of fields and values.

- Relevance for monitoring frameworks
  - Provides a structured, auditable basis for monitoring environmental health indicators in animal-derived foods.
  - Facilitates assessment of exposure and regulatory compliance by offering quantified concentrations with uncertainties and detection thresholds.
  - Supports data-driven decision-making through metadata that clarifies sample context, measurement quality, and data limitations.

- Practical considerations for authors of monitoring frameworks
  - Ensure metadata quality: standardize field names, confirm units, and verify formatting.
  - Address data governance: plan for data sharing, access controls, and documentation updates.
  - Manage non-detect data consistently by defining and applying a uniform handling rule.
  - Maintain alignment between collection protocols (e.g., sample_type, collection_date, sample_size) and analytical reporting to enable reliable trend analysis.