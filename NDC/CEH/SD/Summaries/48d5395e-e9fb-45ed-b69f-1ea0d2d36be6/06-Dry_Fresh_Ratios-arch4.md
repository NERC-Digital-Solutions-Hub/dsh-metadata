# Supporting documentation for 06-Dry_Fresh_Ratios.csv

- This document provides metadata and field-level descriptions for the dataset 06-Dry_Fresh_Ratios.csv.
- It outlines the structure of the data, including field names, explanations, units, and notes.

## Dataset structure and key fields

- Sample_Type
  - Explanation: General description of the sample (e.g., foodstuff group)
  - Units: n/a
  - Notes: n/a
- Sample_Description
  - Explanation: Part of the organism analysed (e.g., where the whole organism was divided and analysed separately)
  - Units: n/a
  - Notes: n/a
- Mean_Value_Dry/Fresh_Ratio
  - Explanation: Mean value of the ratio between dry mass and fresh mass
  - Units: Unitless
  - Notes: n/a
- Min_Value_Dry/Fresh_Ratio
  - Explanation: Minimum value of the ratio between dry mass and fresh mass
  - Units: Unitless
  - Notes: n/a
- Max_Value_Dry/Fresh_Ratio
  - Explanation: Maximum value of the ratio between dry mass and fresh mass
  - Units: Unitless
  - Notes: n/a

## Metadata and data quality considerations for Data Leaders

- The file provides explicit explanations, units, and notes for each field, supporting data provenance and discoverability.
- All values are unitless for the ratio fields, ensuring consistency across records.
- The Notes fields are consistently marked as n/a, indicating no additional caveats documented in this schema.

## Implications for data strategy and governance

- Enables clear documentation of what each column represents, aiding user understanding and correct usage of the dataset.
- Facilitates data cataloging, metadata standardization, and easier data quality checks.
- Highlights the need for broader metadata (e.g., methodology, sample size, measurement conditions) if expanding the dataset for stronger data governance and cross-dataset compatibility.

## Practical next steps for implementation

- Integrate this metadata schema into the data catalog or data governance framework to improve discoverability and reuse.
- Consider enriching with additional metadata (e.g., measurement methods, date of collection, sample source) to strengthen data standards and interoperability.
- Establish data quality checks for the ratio fields (range plausibility, missing values, consistency across Sample_Type and Sample_Description).