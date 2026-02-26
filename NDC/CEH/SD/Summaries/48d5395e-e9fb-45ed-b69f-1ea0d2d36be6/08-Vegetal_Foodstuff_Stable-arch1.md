# Supporting documentation for 08-Vegetal_Foodstuff_Stable.csv

## Purpose and scope
- Provides metadata and explanations for the 08-Vegetal_Foodstuff_Stable.csv dataset to ensure consistent interpretation, reuse, and quality assessment.
- Documents the meaning, units, and handling of all data fields, including measurements, uncertainties, and detection limits.

## Dataset overview
- Content: Stable element concentrations in vegetal foodstuff samples (Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th).
- Measurement basis: Primarily on a dry mass basis (mg/kg_dm); for olive oil and wine, units may be mg per litre.
- Metadata fields include identifying, contextual, and measurement-related information:
  - Sample identifiers, sample type, location, sample description, collection date, and sample size.
  - For each element: concentration, combined uncertainty, and detection limit.

## Key columns and data types
- Sample_Code: Unique sample identifier.
- Sample_Type: General description of the sample (foodstuff group).
- Location: Location where the sample was collected.
- Sample_Description: Part of the organism analyzed (e.g., specific tissue or whole organism portion).
- Collection_Date: Date of collection (format: dd-mm-yyyy).
- Sample_Size: Amount analyzed; units are g fresh matter or mL for olive oil and wine.
- Element concentration columns (all on dry mass basis unless noted):
  - Cs_mg/kg_dm
  - Sr_mg/kg_dm
  - K_mg/kg_dm
  - Na_mg/kg_dm
  - Ca_mg/kg_dm
  - Mg_mg/kg_dm
  - P_mg/kg_dm
  - Pb_mg/kg_dm
  - U_mg/kg_dm
  - Th_mg/kg_dm
- Unc_<Element>_mg/kg_dm: Combined measurement uncertainty for each element (same units).
- Detection_Limit_<Element>_mg/kg_dm: Detection limit for each element (same units).
- Notes on units: For olive oil and wine, some concentration and detection-limit fields may be in mg/L instead of mg/kg_dm.
- Data completeness cues: If a concentration value is blank, it indicates the concentration was below the detection limit.

## Measurement details and interpretation
- Concentrations indicate the amount of each element in the sample, reported with associated uncertainty and detection limits to support quality assessment and comparability.
- Blank values denote sub-detection-limit measurements; uncertainties and detection limits provide context for low-level detections.
- The documentation emphasizes standardized naming, units, and formatting to facilitate cross-sample comparisons and potential data integration.

## Sample context and collection details
- Sample description clarifies which part of the organism was analyzed, enabling appropriate interpretation relative to sample type.
- Collection date and sample size provide temporal and mass context for the measured concentrations.

## Data quality, accessibility, and transparency
- The metadata schema promotes data quality by distinguishing measured values from uncertainties and detection capabilities.
- Explicit Unc_ and Detection_Limit_ fields support rigorous interpretation, reporting, and potential meta-analyses.
- Comprehensive field explanations aim to improve discoverability and reuse of the dataset across diverse analyses.