# Supporting documentation for 18-Transfer_Parameter_Animal_Gamma_Spectrometry.csv

- The document provides field-by-field metadata and explanations for a Gamma Spectrometry dataset related to animal transfer parameters.
- It defines each column, its purpose, expected units, and notes on special values (e.g., below detection limits).

## Overview of the dataset structure

- Sample_Code: Unique identifier for each sample.
- Sample_Type: Indicates the material analyzed (e.g., Soil).
- Location: Name of the sampling site.
- Sample_Description: Specifies the part of the organism analyzed (e.g., specific tissue or organ).
- Collection_Date: Date the sample was collected (format dd-mm-yyyy).
- Radionuclide activity concentrations (CR values) and related fields:
  - Ra-226_CR, Cs-137_CR, Ra-228_CR, K-40_CR: Central requested values (unitless or kg dry matter per L for milk).
  - Unc_Ra-226_CR, Unc_Cs-137_CR, Unc_Ra-228_CR, Unc_K-40_CR: Uncertainties for the corresponding CR values.
  - Detection_Limit_Ra-226_CR, Detection_Limit_Cs-137_CR, Detection_Limit_Ra-228_CR, Detection_Limit_K-40_CR: Detection limits for each radionuclide’s CR value.
- Notes indicate that blanks or missing entries imply the CR value was below the detection limit.

## Data quality and metadata details

- The document provides explicit explanations for each column to support consistent interpretation and reuse.
- It specifies units (where applicable) and handling of undetectable values (below detection limit).
- It highlights the need for clear provenance and consistent metadata to enable reliable analysis.

## Data governance, usability, and gaps

- Importance of a unified data dictionary to ensure consistent naming, units, and acceptable missing-value semantics across datasets.
- Emphasizes discoverability and metadata completeness to support cross-referencing with the primary data file (18-Transfer_Parameter_Animal_Gamma_Spectrometry.csv).
- Potential improvements for data leaders:
  - Standardize units and ensure they align with domain conventions (noting that some unit descriptions reference milk, which may require clarification for soil samples).
  - Enforce consistent date formats and sample descriptions to aid search and filtering.
  - Explicitly capture data provenance, measurement methods, and data collection context.
  - Record and maintain detection limits alongside corresponding CR values to support interpretation of non-detects.
  - Implement validation rules to flag blanks, inconsistent units, or missing uncertainty values.

## Recommendations for Data Leaders

- Establish a formal data dictionary and metadata schema that covers all fields, units, and handling of below-detection values.
- Ensure data assets are discoverable by linking this metadata document to the main CSV and by providing versioning and data lineage information.
- Align units and descriptions across datasets; resolve any ambiguous references (e.g., milk-related units in a soil context).
- Implement data quality checks and governance processes, including clear roles for data stewardship, to maintain accuracy, completeness, and usability over time.
- Create feedback loops with end-users to verify that metadata supports their analytical and reporting needs, enabling co-ownership of data products.