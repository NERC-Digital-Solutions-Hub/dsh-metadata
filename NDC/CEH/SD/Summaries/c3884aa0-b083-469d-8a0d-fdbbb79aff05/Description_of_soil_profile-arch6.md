# DATA HEADER INFORMATION for Description_of_soil_profile.csv

## Overview
- Records soil profile pit descriptions collected during field sessions.
- Related documentation: Manual_1_Classical_Survey page 13, section 2.3.3.2; DOI provided.
- Programme: ESPA; Project: P4GES. Acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data.

## Data schema (fields, types, and units)
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
  - Depth interpretation: 0 to 10 means from the surface to 10 cm; 22 to 53 means the sample was taken at a depth of 23 cm down to 53 cm
  - Unit ok: cm
- color
  - Information: soil layer colour according to Munsell code
  - Variable Type: Text String
  - Unit ok: .
- texture
  - Information: soil texture estimated in the field
  - Variable Type: Categorical
  - Texture options: Clayey, Sandy, Sandy-Clayey, Silty-Clayey, Clay-sandy
  - Unit ok: .
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

## Data quality and handling
- Blank cells and NA denote no available data.

## Usage and applications
- Facilitates combining horizons within sites to build comprehensive soil profiles.
- Enables self-serve exploration of horizon properties (depth, color, texture, structure, root presence, porosity).
- Supports data curation tasks such as standardizing texture categories and harmonizing depth representations for cross-site analyses.
- Can be integrated with other soil datasets to analyze patterns across environments or management practices.

## Provenance and acknowledgement
- Site_ID corresponds to P4GES site codes; dataset sourced from ESPA/P4GES program.
- Proper acknowledgment required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).