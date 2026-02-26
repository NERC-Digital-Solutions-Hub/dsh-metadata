# DATA HEADER INFORMATION for Description_of_soil_profile.csv

## Overview
- Records soil profile pit descriptions collected during field sessions.
- Related guidance: Manual_1_Classical_Survey, page 13, section 2.3.3.2.
- Programme/Project: ESPA and P4GES.
- Acknowledgement required: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.
- Key identifiers and measurements are provided with defined types, units, and value expectations.

## Data fields and definitions
- Site_ID
  - Information: P4GES site code
  - Variable Type: Text String
  - Unit: none
- Horizon
  - Information: name of the soil horizon
  - Variable Type: Text String
  - Unit: none
- depth_cm
  - Information: depth of the soil horizon
  - Variable Type: Numeric
  - Unit: cm
  - Note: 0 to 10 means surface to 10 cm; 22 to 53 means 23 cm to 53 cm depth
- color
  - Information: soil layer colour according to Munsell code
  - Variable Type: Text String
  - Unit: none
  - Reference: Munsell color system
- texture
  - Information: soil texture estimated in the field
  - Variable Type: Categorical
  - Unit: none
  - Categories: Clayey, Sandy, Sandy-Clayey, Silty-Clayey, Clay-sandy
- structure
  - Information: soil observed structure
  - Variable Type: Categorical
  - Unit: none
- root_importance
  - Information: coverage percentage of root observed in the soil layer
  - Variable Type: Numeric
  - Unit: %
- porosity
  - Information: percentage of small porosity holes observed in soil layer
  - Variable Type: Numeric
  - Unit: %

## Data quality and data handling
- Blank cells and NA indicate no available data.

## Provenance and references
- DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
- Programme: ESPA (http://www.espa.ac.uk/)
- Project: P4GES (https://www.p4ges.org)
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo