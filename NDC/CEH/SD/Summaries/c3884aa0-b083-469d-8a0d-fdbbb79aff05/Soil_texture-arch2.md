# DATA HEADER INFORMATION for Soil_texture.csv

## Overview
- Describes the dataset for soil granulometric (granulometric) analysis.
- Part of ESPA Programme and P4GES project; DOI provided for reference.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Data Provenance and References
- See also Manual_3_ Laboratory_works.rtf (page 2) for additional context.
- DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
- Programme: ESPA; Project: P4GES
- Acknowledgement required for derived products.

## Data Schema (Fields and Definitions)
- site_ID
  - Information: P4GES site code
  - Variable Type: Text String
  - Unit: (not specified)
- subplot
  - Information: Subplot where the sample was collected
  - Variable Type: Categorical
  - Unit: S1 / S2 / S3 / S4
- soil_fraction
  - Information: Granulometric class of soil particles (clay, silt or sand)
  - Variable Type: Categorical
  - Unit: Clay / Silt / Sand
- depth_cm
  - Information: Depth of the sample collection
  - Variable Type: Numeric
  - Unit: cm
- percentage_value
  - Information: Percentage of the granulometric fraction
  - Variable Type: Numeric
  - Unit: % (percentage)

## Data Use and Outputs
- Used to represent soil granulometry in a standardized format suitable for monitoring environmental health.
- Facilitates comparison across sites and depths by using consistent categories and units.
- Supports downstream analyses, reporting, mapping, and policy monitoring within the ESPA/P4GES framework.

## Data Quality and Accessibility
- Data should be verified, quality assured, cleaned, and transformed following standard procedures.
- Datasets are stored and uploaded to appropriate portals to enable access to underlying data and metadata.
- Emphasis on reusability and integration with other environmental datasets.

## Practical Implications for Analysts
- Ensure correct interpretation of site_ID, subplot, and soil_fraction categories when aggregating or comparing data.
- Maintain traceability to the source via the DOI and project references.
- Acknowledge the contributing laboratory (Laboratoire des Radio Isotopes, Université d'Antananarivo) for derived products.