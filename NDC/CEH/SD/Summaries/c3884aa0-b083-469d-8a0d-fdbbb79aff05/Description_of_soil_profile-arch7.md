# DATA HEADER INFORMATION for Description_of_soil_profile.csv

- The dataset captures soil profile pit descriptions collected during field sessions as part of the ESPA P4GES project.
- Related documentation: Manual_1_Classical_Survey (page 13, section 2.3.3.2); DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05.
- Acknowledgement requirement: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Data fields and definitions

- Site_ID
  - Information: P4GES site code
  - Variable Type: Text String
- Horizon
  - Information: name of the soil horizon
  - Variable Type: Text String
- depth_cm
  - Information: depth of the soil horizon
  - Variable Type: Numeric
  - Unit: cm
  - Notes: Examples – 0 to 10 means surface to 10 cm; 22 to 53 means sample taken from 23 cm to 53 cm depth
- color
  - Information: soil layer colour according to Munsell code
  - Variable Type: Text String
- texture
  - Information: soil texture estimated in the field
  - Variable Type: Categorical
  - Categories: Clayey / Sandy / Sandy-Clayey / Silty-Clayey / Clay-sandy
- structure
  - Information: soil observed structure
  - Variable Type: Categorical
- root_importance
  - Information: coverage percentage of root observed in the soil layer
  - Variable Type: Numeric
  - Unit: %
- porosity
  - Information: percentage of small porosity holes observed in soil layer
  - Variable Type: Numeric
  - Unit: %

## Data quality and handling

- Missing data: Blank cells and NA indicate no available data for that field.
- Standards and consistency:
  - color uses Munsell color notation; may require standardization or conversion for some GIS visualizations.
  - texture and structure are categorical; ensure consistent class labels across datasets.
  - depth_cm represents the horizon’s sampling depth, often as a range; interpret and visualize as vertical extent where applicable.
- Data integration considerations:
  - Site_ID is the key to link to spatial locations (points or polygons representing sampling sites).
  - Horizon-level data can be stored as separate records per Site_ID to reflect stratigraphy; suitable for 2D attribute tables or 3D soil modeling when paired with depth ranges.

## GIS usage and visualization guidance

- Linking data:
  - Use Site_ID to join the soil profile attributes to spatial site features (points/polygons).
  - For multiple horizons per site, create multiple records linked to the same Site_ID with different horizon and depth_cm values.
- Visualizations:
  - Depth-based stratification: create vertical profiles or 3D representations using depth_cm as the vertical axis.
  - Color field: display Munsell color values (may require conversion to RGB/hex for map rendering).
  - Texture and structure: symbolize as categorical layers or attribute-based filters.
  - Root_importance and porosity: visualize as percentage-based attributes, suitable for graduated symbology or pop-ups.

## Provenance and references

- Project and program: ESPA; Project - P4GES.
- Documentation reference: Manual_1_Classical_Survey (section cited above).
- Acknowledgement: required when producing products from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).