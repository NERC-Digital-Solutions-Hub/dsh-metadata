# Supporting documentation for 12-Feedstuff_Stable.csv

- Provides column definitions and metadata for the dataset 12-Feedstuff_Stable.csv, documenting concentrations of stable elements in feedstuff samples, with uncertainties and detection limits.

## Dataset and measurement scope

- Analyte focus includes Cs, Sr, K, Na, Ca, Mg, P, Pb, U, and Th measured on a dry mass basis (mg per kg dry mass, with related uncertainties and detection limits).
- Concentrations reported as mg/kg_dm; when blank, indicates concentration below the detection limit.
- Sample-level metadata included to support traceability and reuse in analyses.

## Key sample metadata fields

- Sample_Code: unique sample identifier.
- Sample_Type: general description of the sample (feedstuff group).
- Location: location where the sample was collected.
- Sample_Description: part of the organism analyzed (e.g., tissue or whole organism portion).
- Collection_Date: date of sample collection (format dd-mm-yyyy).
- Sample_size: amount analyzed (g fresh matter).

## Analyte data structure

For each element (example shown; similar structure applies to all listed elements):

- Cs_mg/kg_dm: concentration of stable Cs on a dry mass basis.
  - Unc_Cs_mg/kg_dm: combined uncertainty.
  - Detection_Limit_Cs_mg/kg_dm: detection limit on a dry mass basis.
- Sr_mg/kg_dm, K_mg/kg_dm, Na_mg/kg_dm, Ca_mg/kg_dm, Mg_mg/kg_dm, P_mg/kg_dm, Pb_mg/kg_dm, U_mg/kg_dm, Th_mg/kg_dm: same sub-fields as Cs.
  - Unc_*: combined uncertainty for each element.
  - Detection_Limit_*: detection limit for each element.
- Notes indicate that blank values correspond to concentrations below the detection limit.

## Data quality and formatting notes

- Field names are descriptive but contain inconsistencies in a few lines (e.g., Unc_K_Mg/kg_dm, and some Na/U/Th entries with spacing/typo irregularities).
- The documentation emphasizes reporting on dry mass basis and clearly marking below-detection observations.
- This file serves as a reference for data cleaning, transformation, and subsequent statistical analyses, including correlation assessment and model development.

## How analysts can use this documentation

- Use the defined fields to validate and harmonize datasets, ensuring consistent units (mg/kg_dm) and handling below-detection values appropriately.
- Track sample provenance and collection details to support reproducibility and metadata discoverability.
- Combine with other datasets, apply quality checks, and develop predictive insights about feedstuff compositions and potential correlations among elements.