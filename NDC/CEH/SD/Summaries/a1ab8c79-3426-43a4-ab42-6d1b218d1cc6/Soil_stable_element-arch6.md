# Supporting documentation for Soil_Stable_Element.csv

## Quick overview
- Provides metadata for the Soil_Stable_Element.csv data, focusing on sample identifiers, sample characteristics, collection date, and a comprehensive set of elemental concentrations on a dry-mass basis.
- Key replicates noted: RCN119, RCN120, and RCN121 are replicate soil samples.
- Concentrations are reported as milligrams per kilogram (mg/kg_dw) with corresponding detection-limit columns to indicate censoring (below detection).

## Data structure and fields
- Sample identifiers and descriptors
  - Sample_Code: Unique sample identifier
  - Sample_Type: Type of sample (soil-related)
  - Sample_Description: Additional explanation; notes that RCN119, RCN120, and RCN121 are replicate samples
  - Collection_Date: Date of collection (format: dd month yyyy)
- Element concentration fields
  - I-127_mg_kg_dw, Li_mg_kg_dw, Be_mg_kg_dw, B_mg_kg_dw, Na_mg_kg_dw, Mg_mg_kg_dw, Al_mg_kg_dw, P_mg_kg_dw, S_mg_kg_dw, K_mg_kg_dw, Ca_mg_kg_dw, Ti_mg_kg_dw, V_mg_kg_dw, Cr_mg_kg_dw, Mn_mg_kg_dw, Fe_mg_kg_dw, Co_mg_kg_dw, Ni_mg_kg_dw, Cu_mg_kg_dw, Zn_mg_kg_dw, As_mg_kg_dw, Se_mg_kg_dw, Rb_mg_kg_dw, Sr_mg_kg_dw, Mo_mg_kg_dw, Ag_mg_kg_dw, Cd_mg_kg_dw, Cs_mg_kg_dw, Ba_mg_kg_dw, Tl_mg_kg_dw, Pb_mg_kg_dw, U_mg_kg_dw
  - Each element has a corresponding Detection_Limit_<element>_mg_kg_dw column
  - Explanations for these columns describe the concentration on a dry mass basis and the detection-limit for the given sample
- Units and notes
  - Concentrations: Milligrams per kilogram (mg/kg_dw)
  - Detection-limit columns explain the detection threshold and when a value is considered detectable or below detection
  - Some notes indicate that a blank concentration implies the value was below the detection limit (see the corresponding detection-limit column)

## Key semantics and data quality considerations
- Below detection handling
  - If the concentration value is blank, it indicates the concentration was below the detection limit; the relevant detection-limit column should be used to understand the limit for that sample.
  - Detection-limit columns may include codes or notes (e.g., “1 = Detection limit …, 2 = Milligrams per kilogram, 3 = Where blank then concentration was detectable”), though formatting may vary by element.
- Replicates and data use
  - Replicates (RCN119, RCN120, RCN121) are embedded within the dataset and should be treated as separate samples or aggregated per analysis requirements.
- Data quality caveats
  - The provided text shows formatting inconsistencies and typographical errors in some sections, which may require careful parsing and validation when loading into a data workspace.
  - Column naming and notes sometimes contain truncated phrases; validation and standardization are advisable before downstream use.

## Practical guidance for data use
- Key identifier: Use Sample_Code to join with other datasets or metadata; align replication groups via the replicate notes (RCN numbers).
- Handling censored data
  - Treat blank concentrations as censored values; use the corresponding Detection_Limit_<element>_mg_kg_dw for analysis or imputation decisions.
  - When performing analyses (e.g., summary statistics), consider methods appropriate for left-censored data (e.g., substitution with detection limits, Tobit models, or survival-analysis-inspired approaches) depending on the analytical goal.
- Date parsing
  - Collection_Date uses the format "dd month yyyy"; ensure date parsing accommodates month names (e.g., "01 January 2020").
- Data integration and cleaning
  - Standardize column names and fix obvious formatting inconsistencies if integrating with other datasets.
  - Maintain provenance by preserving both concentration and its detection-limit column to retain censoring information.

## Recommendations for data improvements (if contributing)
- Standardize column naming and ensure consistent, complete notes across all element columns.
- Provide a concise, machine-readable data dictionary mapping each concentration column to its unit and interpretation (including censoring rules).
- Consider a separate explicit censored indicator column for each element (e.g., Is_I_127_below_detection) to simplify analysis.
- Validate and fix any typos or incomplete notes in the detection-limit descriptions to avoid misinterpretation.