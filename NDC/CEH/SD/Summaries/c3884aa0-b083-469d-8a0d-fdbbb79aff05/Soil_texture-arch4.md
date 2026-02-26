# DATA HEADER INFORMATION for Soil_texture.csv

## Overview
- The dataset records information on soil granulometric analysis.

## Data structure and fields
- site_ID
  - Information: P4GES site code
  - Variable Type: Text String
  - Unit: (none)
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
  - Unit: %- percentage

## Metadata and provenance
- DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
- Programme: ESPA
- Project: P4GES
- Acknowledgement: Required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo)

## Usage guidance
- Data fields are clearly typed with explicit units to support validation and interoperability.
- The dataset is organized by site, subplot, granulometric class, collection depth, and fraction percentage.

## Data governance and quality considerations
- Ensure metadata completeness and consistency across records (site_ID, subplot, soil_fraction, depth_cm, percentage_value).
- Maintain discoverability and updates; verify data content and format when integrating with other data sources.
- Be mindful of appropriate acknowledgments in any derived products.

## Practical implications for Data Leaders
- Consider end-user needs (e.g., policy colleagues, researchers) when sharing or republishing; provide clear provenance and licensing.
- Plan for cross-site data integration by enforcing consistent categories (S1–S4; Clay/Silt/Sand) and units (cm, %).
- Coordinate with partners (P4GES/ESPA) to sustain data quality, standards, and metadata practices.