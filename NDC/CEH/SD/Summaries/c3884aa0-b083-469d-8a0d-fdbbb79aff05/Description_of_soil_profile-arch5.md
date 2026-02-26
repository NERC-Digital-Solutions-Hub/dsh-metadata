# DATA HEADER INFORMATION for Description_of_soil_profile.csv

## Overview
- This dataset records soil profile pit descriptions collected during field sessions.
- Related to the ESPA programme and the P4GES project.
- DOI provided for the data description: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
- Acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo is required for products derived from these data.

## Data fields and definitions
- Site_ID
  - Information: P4GES site code
  - Variable Type: Text String
  - Unit ok: .
- Horizon
  - Information: name of the soil horizon
  - Variable Type: Text String
  - Unit ok: .
- depth_cm
  - Information: depth of the soil horizon
  - Variable Type: Numeric
  - Unit ok: cm
  - Notes: ranges illustrate depths (e.g., 0 to 10 cm from surface; 22 to 53 cm for a sample between 23 and 53 cm)
- color
  - Information: soil layer colour according to the Munsell code value
  - Variable Type: Text String
  - Unit ok: .
- texture
  - Information: soil texture estimated in the field
  - Variable Type: Categorical
  - Unit ok: .
  - Categories: Clayey, Sandy, Sandy-Clayey, Silty-Clayey, Clay-sandy
- structure
  - Information: soil observed structure
  - Variable Type: Categorical
  - Unit ok: .
- root_importance
  - Information: coverage percentage of root observed in the soil layer
  - Variable Type: Numeric
  - Unit ok: %
- porosity
  - Information: percentage of small porosity holes observed in soil layer
  - Variable Type: Numeric
  - Unit ok: %

## Data quality and missing values
- Blank cells and NA indicate no available data.

## Metadata, provenance, and references
- Manual reference: Manual_1_Classical_Survey, page 13, section 2.3.3.2
- Programme: ESPA
- Project: P4GES
- DOI provided for dataset description
- Acknowledgement requirement for derivative products (Laboratoire des Radio Isotopes, Université d'Antananarivo)