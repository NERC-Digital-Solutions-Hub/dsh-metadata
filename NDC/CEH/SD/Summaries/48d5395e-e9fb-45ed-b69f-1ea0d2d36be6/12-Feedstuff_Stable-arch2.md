# Supporting documentation for 12-Feedstuff_Stable.csv

## Purpose and scope
- Provides the data dictionary and field-level explanations for the 12-Feedstuff_Stable.csv dataset.
- Outlines metadata, measurement outputs, uncertainties, and detection limits for multiple elements in feedstuff samples on a dry-mass basis.
- Aims to support consistent data ingestion, quality assurance, transformation, and presentation for environmental monitoring and policy assessment.

## Key metadata fields
- Sample_Code: Unique sample identifier.
- Sample_Type: General description of the feedstuff group.
- Location: Location where the sample was collected.
- Sample_Description: Part of the organism analyzed (e.g., where the whole organism was divided and analyzed).
- Collection_Date: Date of sample collection (format: dd-mm-yyyy).
- Sample_size: Amount of sample analyzed (units: g fresh matter).

## Analyte data structure (concentrations, uncertainty, detection limits)
- Elements covered: Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th.
- For each element, fields include:
  - [Element]_mg/kg_dm: Concentration on a dry mass basis (units: mg per kg dry mass).
  - Unc_[Element]_mg/kg_dm: Combined uncertainty of the concentration (units: mg per kg dry mass).
  - Detection_Limit_[Element]_mg/kg_dm: Detection limit on a dry mass basis (units: mg per kg dry mass).
- Notes on data values:
  - Where a concentration field is blank, the value is below the detection limit.
  - Field naming inconsistencies exist (e.g., Unc_K_Mg/kg_dm; Mg-related fields sometimes titled with Mg in the unit field), which may require harmonization during data cleaning.
  - For U and Th, some fields appear with sub-indices (1, 2, 3) indicating multiple related entries or parameterizations.
  - For Na, the documentation includes phrases such as "detection limit" and notes on how blanks relate to detection limits, emphasizing below-detection-limit handling.

## Units and data handling considerations
- Concentrations are reported on a dry mass basis (mg/kg_dm).
- Sample_size uses grams (fresh matter) as the basis for initial sampling.
- Below-detection-limit values are indicated by blank concentration fields and accompanied by the detection limit fields as the reference threshold.
- Some fields include textual notes within the documentation (e.g., detection-limit semantics) that should be parsed during data ingestion.

## Data quality and interoperability implications for Analysts Monitoring the Environment
- Emphasizes standardized data representation to enable cross-sample comparisons and trend analysis over time.
- Facilitates verification and quality assurance by documenting uncertainty and detection limits per analyte.
- Supports data sharing and portal upload by providing explicit metadata and measurement-context fields.
- Highlights the need to harmonize field names and units across datasets to maximize data value when integrating with other environmental monitoring data.

## Practical use for environmental monitoring and policy evaluation
- Enables consistent reporting of stable element concentrations in feedstuffs, aiding assessment of environmental exposure and dietary risk.
- Supports combining feedstuff data with other environmental datasets to enhance monitoring value (aligns with the aim of increasing data utility beyond single-use datasets).
- Provides a clear reference for data processing steps, including handling of non-detects and uncertainties, which is essential for reproducible analyses and policy performance scrutiny.