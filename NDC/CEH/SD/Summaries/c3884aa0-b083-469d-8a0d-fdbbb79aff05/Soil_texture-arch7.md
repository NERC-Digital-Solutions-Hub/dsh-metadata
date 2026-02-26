# DATA HEADER INFORMATION for Soil_texture.csv

## Overview
- This dataset records information on soil granulometric analysis (particle-size distribution) and is referenced to related project and methodological documents.
- See Manual_3_ Laboratory_works.rtf page 2 for detailed procedures.
- Acknowledgement of the Laboratoire des Radio Isotopes, Université d'Antananarivo is required for products derived from these data.
- Project and programme context: ESPA; P4GES.

## Data fields and units
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
  - Unit: %

## Provenance and documentation
- Programme: ESPA
- Project: P4GES
- See DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
- Reference to data collection and laboratory context: Manual_3_ Laboratory_works.rtf

## GIS usage and integration
- Suitable for map-based visualization of soil textures by site, subplot, and depth.
- Can be joined to a geolocated site dataset via site_ID to create spatial layers showing the distribution of clay, silt, and sand fractions at different depths (depth_cm) and subplots (S1–S4).
- percentage_value provides the proportion of each granulometric fraction within a sample; multiple records may exist per site/subplot/depth for different fractions (e.g., clay, silt, sand).
- Considerations:
  - Coordinates or site geometry are not included in this header; integrate with a separate spatial dataset containing site locations.
  - Depth dimension enables vertical profiling when combined with other depth-labeled data.
  - Ensure consistent categorical coding for soil_fraction across datasets.

## Data quality and limitations
- Data may be distributed across multiple sources or formats; harmonization may be required (especially for site_ID and subplot coding).
- Consistency of units and categories (Clay/Silt/Sand) should be validated before GIS integration.
- The header points to additional methodological details in the referenced manual; review for sampling methods, measurement precision, and fraction definitions.
- Missing or inconsistent data could affect spatial analyses; plan for data cleaning and standardization.

## Related references and acknowledgements
- Manual_3_ Laboratory_works.rtf (page 2) for laboratory methods.
- ESPA Programme; P4GES Project; DOI provided above.
- Acknowledgement required for products derived from these data to Laboratoire des Radio Isotopes, Université d'Antananarivo.