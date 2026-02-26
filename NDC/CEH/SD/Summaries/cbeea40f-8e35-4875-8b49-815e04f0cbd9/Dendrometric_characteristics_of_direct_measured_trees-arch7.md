# DATA HEADER INFORMATION for Dendrometric_characteristics_of_direct_measured_trees.csv

## Overview
- Dataset contains results of direct field measurements for the pool "above ground biomass," including weights, diameters, heights, coordinates, distances, and related attributes.
- Source and context: ESPA Programme, Project P4GES; DOI provided. Acknowledgement required for products derived from these data.
- Related documentation: Manual 1_Classical_Survey referenced.

## Key data fields (via themes)

- Identification and location
  - Site_ID: P4GES WP4 site code
  - ZOI: Zone of Interest (categorical; ZOI1 Lakato, ZOI2 Andasibe, ZOI3 Anjahamana, ZOI4 Didy)
  - Location: sampling point location (text)
  - Location field materials/resources: local guides, etc.
  - Species_name: vernacular tree name
  - Scientific_Name: scientific binomial name

- Spatial and measurement context
  - X, Y: coordinates/distance values related to crown projection and trunk position
  - X', Y': additional crown projection coordinates (left/right)
  - Diameter_class: Large (>20 cm), Medium (10–20 cm), Small (<10 cm)

- Dendrometric measurements
  - DBH: Diameter at Breast Height (cm)
  - Height_total: total tree height (m)
  - H_trunk: trunk height (m)
  - Length_trunk: length of tree trunk (m)
  - Crown_height: height of crown from ground (m)
  - Top_diameter, Middle_diameter, Basal_diameter: diameters at top, mid-trunk, and 30 cm above ground (cm)
  - Total_length: total length of tree (m)
  - Nb_main_branches: number of main branches

- Data capture details
  - Field materials/resources: forester compass, decameter, botanist, etc.

- Biomass and weight measurements (both fresh and dry, various components)
  - Dry_weight_of_basal_diameter_samples, Dry_weight_of_branches_samples, Dry_weight_of_DBH_diameter_samples, Dry_weight_of_DBH_samples, Dry_weight_of_leaf_samples, Dry_weight_of_Top_trunk_samples, Dry_weight_of_Middle_trunk_samples, Dry_weight_of_Top_trunk_samples, Dry_weight_of_trunk
  - Fresh_weight_of_basal_diameter_samples, Fresh_weight_of_branches, Fresh_weight_of_DBH_samples, Fresh_weight_of_leaf, Fresh_weight_of_Middle_trunk_samples, Fresh_weight_of_Top_trunk_samples, Fresh_weight_of_trunk
  - Units for weights are grams (g) or kilograms (kg) as indicated per field group
  - Each weight field often has replicated subfields (e.g., 1, 2, 3, 4) representing different sample sets or measurement instances

## Data provenance and structure

- Field origin: direct measurements during fieldwork; coordinates and physical dimensions collected on-site
- Data relations: combines measurements with species identifiers and zone classifications to support spatial analysis and biomass estimation
- Units and types: explicit in field descriptions (e.g., DBH in cm, heights in m, various diameters in cm, weights in g or kg)
- Documentation references: link to Manual 1_Classical_Survey and DOI for data retrieval and provenance

## Practical GIS applications

- Map and analyze tree spatial distribution by ZOI, Site_ID, and Location
- Link dendrometric attributes (DBH, heights, diameters) to spatial features for biomass modeling
- Integrate species data (vernacular and scientific names) with structural measurements
- Use X, Y, X', Y' coordinates and crown-related distances for canopy modeling and spatial profiling
- Utilize biomass weight fields (fresh/dry) to estimate above-ground biomass by location or stand
- Enable data quality checks by aligning units, data types, and replicate fields for reproducibility

## Notes and cautions

- Some fields contain replicated measurements (e.g., multiple weight samples per tree) indicated by numerical suffixes; ensure consistent interpretation when aggregating
- Minor formatting inconsistencies in field descriptions (typos) present; rely on the stated unit and field type guides for parsing
- Data are tied to specific zones and sites; when combining with other datasets, maintain ZOI and Site_ID schemas for correct joins