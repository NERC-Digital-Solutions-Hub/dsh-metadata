# Supporting documentation for 10-Animal_Foodstuff_Stable.csv

## Overview
- Data dictionary for a dataset of stable-element concentrations in animal-derived foodstuffs.
- Provides sample metadata (identifiers, description, collection details) and concentration measurements for multiple elements.
- Elements covered: Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th, with concentrations given on a fresh mass basis (mg/kg_fm) or, for milk, mg/L.
- Each element includes associated uncertainty (Unc_*) and detection limit (Detection_Limit_*) fields.
- Sample metadata includes Sample_Code, Sample_Type (foodstuff group), Location, Sample_Description (part analyzed), Collection_Date (dd-mm-yyyy), and Sample_size (g fresh matter or mL for milk).

## Data structure and key fields
- Metadata fields:
  - Sample_Code: Unique sample identifier
  - Sample_Type: General description of the sample (foodstuff group)
  - Location: Location where sample was collected
  - Sample_Description: Part of the organism analyzed (e.g., whole organism vs. specific tissue)
  - Collection_Date: Date of collection (dd-mm-yyyy)
  - Sample_size: Amount analyzed (g fresh matter or mL for milk)
- Measurement fields (one set per element; examples shown for Cs and Na):
  - Cs_mg/kg_fm: Concentration of stable Cs
  - Unc_Cs_mg/kg_fm: Combined uncertainty of Cs concentration
  - Detection_Limit_Cs_mg/kg_fm: Detection limit for Cs
  - Na_mg/kg_fm (and Unc_Na_mg/kg_fm, Detection_Limit_Na_mg/kg_fm): Similar trio for Na
  - Similar triplets for Sr, K, Ca, Mg, P, Pb, U, Th (each with corresponding Unc_* and Detection_Limit_* fields)
- Units:
  - Most elemental concentrations: mg/kg_fm (fresh mass basis)
  - Milk-specific concentrations: mg/L
  - Sample_size units: g fresh matter or mL for milk
- Notes on field content:
  - Some entries indicate concentrations below detection limits by being blank in the concentration field
  - Detection-limit fields may be blank in some records
  - Column naming shows some inconsistencies (e.g., varying capitalization or occasional mislabeling such as Unc_K_Mg/kg_fm); users may need harmonization during processing

## Measurement interpretation and data quality
- Below-detection values: When concentration is blank, it indicates the measurement is below the detection limit.
- Uncertainty fields: Provide the combined uncertainty for each concentration measurement.
- Inconsistencies to watch for:
  - Occasional typos or inconsistent naming (e.g., Na_mg/kg_fm, Unc_K_Mg/kg_fm) that may require standardization.
  - Some detection-limit fields may be missing or misaligned; confirm units and column mappings during data ingestion.
- Data scope: Focused on stable-element concentrations in animal-derived foods, with a structure suitable for cross-sample comparisons and subsequent modeling.

## Potential uses for analysis
- Descriptive statistics and comparisons of element concentrations across sample types, locations, and collection dates.
- Correlation analyses between elements (e.g., Cs vs. Sr) or with sample descriptors.
- Handling left-censored data (below-detection values) in statistical analyses and predictive modeling.
- Development of data pipelines that merge these measurements with other datasets (unifying formats and units) for broader environmental or nutritional assessments.

## Practical notes for analysts
- Prepare for unit harmonization across fields (mg/kg_fm vs. mg/L) and standardize column names to ensure consistency.
- Treat blank concentration fields as below detection limits; use corresponding Detection_Limit_* values where available for censoring in analyses.
- Maintain traceability to metadata (Sample_Code, Collection_Date, Location) to enable reproducible analyses and data provenance.
- Validate data quality by checking for missing detection limits and irregular field naming, then document any transformations.