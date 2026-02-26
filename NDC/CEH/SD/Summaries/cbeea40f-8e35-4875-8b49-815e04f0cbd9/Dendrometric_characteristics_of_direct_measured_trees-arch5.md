# DATA HEADER INFORMATION for Dendrometric_characteristics_of_direct_measured_trees.csv

## Overview
- Documents the direct measurements collected in the field for the pool "above ground biomass," including weights, diameters, heights, coordinates, distances, etc.
- Related to ESPA Programme and P4GES project; DOI provided for the dataset.
- Requires acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from the data.
- Refers to Manual 1_Classical_Survey for additional guidance.

## Provenance and access
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Programme: ESPA; Project: P4GES
- Acknowledgement requirement for derived products
- Data header information and field definitions are provided to support data discovery and reuse

## Dataset structure and key variables
- Site and location identifiers
  - Site_ID: P4GES WP4 site code
  - ZOI (Zone of Interest): categories such as Lakato, Andasibe, Anjahamana, Didy
  - Location: sampling point location name
- Taxonomy and naming
  - Species_name: vernacular name
  - Scientific_Name: scientific name
- Morphometrics and positioning
  - Diameter_class: Large (L, >20 cm), Medium (M, 10–20 cm), Small (S, <10 cm)
  - DBH: Diameter at Breast Height (cm)
  - Height_total: tree height (m)
  - H_trunk: trunk height (m)
  - X, X', Y, Y': distances from trunk to crown projections (meters or decameters)
  - Basal_diameter, Middle_diameter, Top_diameter: diameters at specified heights (cm)
  - Length_trunk, Total_length: trunk and overall tree length (m)
  - Crown_height: height of crown (m)
  - Nb_main_branches: number of main branches
- Sample weights (dry and fresh)
  - Dry_weight_of_basal_diameter_samples, Dry_weight_of_branches_samples, Dry_weight_of_DBH_diameter_samples, Dry_weight_of_DBH_samples, Dry_weight_of_leaf_samples, Dry_weight_of_Top_trunk_samples, etc. (numeric with grams as units)
  - Fresh_weight_of_basal_diameter_samples, Fresh_weight_of_branches, Fresh_weight_of_DBH_samples, Fresh_weight_of_leaf, Fresh_weight_of_Middle_trunk_samples, Fresh_weight_of_Top_trunk_samples, Fresh_weight_of_trunk (numeric with kilograms or grams as units)
  - Some entries specify multiple samples per type (e.g., 1, 2, 3, 4) indicating repeated measurements or sub-samples
- Field methods and resources
  - Field materials/resources include forester compass, botanist, local guides
- Data types and units
  - Variable_type includes Numeric and Categorical
  - Units vary by variable (cm, m, grams, kilograms, etc.)

## Data governance and stewardship considerations
- Metadata quality
  - Ensure consistency of variable names, descriptions, units, and data types across datasets
  - Address any inconsistencies or typos in units (e.g., “gramm” vs “gram”)
- Standardization and interoperability
  - Map Zone of Interest categories and site codes to standard vocabularies where possible
  - Align measurement units and ensure unit conversions are clearly documented
- Provenance and attribution
  - Maintain DOI reference and project details; enforce required acknowledgments for derived products
- Access and sharing
  - Document embargoes, proprietary issues, and update mechanisms for shared datasets
  - Ensure data uploads to portals and catalogues follow the defined metadata schema
- Data quality and validation
  - Implement checks for plausible ranges (e.g., DBH, heights, diameters)
  - Validate that coordinates and distances are consistently recorded (meters/decameters)
- Maintenance and updates
  - Provide clear update protocols and versioning; document any changes to header definitions or field mappings
- Documentation references
  - Manual 1_Classical_Survey and the dataset’s header information should be kept current for user guidance

## Practical implications for data stewards
- Prepare crosswalks to standard forest measurement vocabularies and ensure consistent coding for ZOI and Site_ID
- Implement validation rules for numeric fields (e.g., DBH, heights) and ensure units are explicit in the data dictionary
- Preserve and surface the provenance information (DOI, program, project, acknowledgments) in data portals and metadata records
- Facilitate discoverability by clearly linking to related manuals and project pages
- Plan for handling large, multi-field datasets with multiple sub-samples per measurement type

## References
- Data header information and field definitions for Dendrometric_characteristics_of_direct_measured_trees.csv
- Manual 1_Classical_Survey
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- ESPA Programme; Project P4GES