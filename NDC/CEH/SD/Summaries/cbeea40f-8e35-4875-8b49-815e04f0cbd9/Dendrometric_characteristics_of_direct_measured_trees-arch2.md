DATA HEADER INFORMATION for Dendrometric_characteristics_of_direct_measured_trees.csv

## Overview
- Describes the direct field measurements for the pool "above ground biomass," including weights, diameters, heights, coordinates, distances, etc.
- Associated with the ESPA programme and P4GES project (DOI provided). Acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data.
- Serves as metadata for standardized environmental monitoring and analysis of tree dendrometric characteristics.

## Key Variables and Data Structure
- Site and location
  - Site_ID: P4GES WP4 site code (text)
  - ZOI: Zone of Interest (categorical) with values Lakato, Andasibe, Anjahamana, Didy
  - Location: sampled point location (text)
- Taxonomy
  - Species_name: vernacular name (text)
  - Scientific_Name: scientific name (text)
  - Diameter_class: Large (>20 cm), Medium (10–20 cm), Small (<10 cm) (categorical)
- Size and structure measurements
  - DBH: Diameter at Breast Height (cm) (numeric)
  - Height_total: total tree height (m) (numeric)
  - H_trunk: trunk height (m) (numeric)
  - X, X', Y, Y': distances related to crown projection to ground (m; with X referring to front, X' to crown; Y and Y' to left/right/rear projections) (numeric)
  - Basal_diameter, Middle_diameter, Top_diameter: diameters at 30 cm from ground, mid-trunk, and top (cm) (numeric)
  - Length_trunk: trunk length (m) (numeric)
  - Crown_height: crown height from ground to crown base (m) (numeric)
  - Total_length: total tree length (m) (numeric)
  - Nb_main_branches: number of main branches (numeric)
- Biomass and weights (fresh and dry)
  - Dry_weight_of_basal_diameter_samples, Dry_weight_of_branches_samples, Dry_weight_of_DBH_diameter_samples, Dry_weight_of_DBH_samples, Dry_weight_of_leaf_samples, Dry_weight_of_Top_trunk_samples: dry weights for respective samples (grams) (numeric)
  - Fresh_weight_of_basal_diameter_samples, Fresh_weight_of_branches, Fresh_weight_of_branches_samples, Fresh_weight_of_DBH_samples, Fresh_weight_of_leaf, Fresh_weight_of_leaf_samples, Fresh_weight_of_Middle_trunk_samples, Fresh_weight_of_Top_trunk_samples, Fresh_weight_of_trunk: fresh weights for respective parts (grams or kilograms as specified) (numeric)
  - Note: Some fields list multiple unit options or inconsistent spellings (gramm, Kilogramm, etc.); units are as indicated in the header.
- Field materials/resources
  - Forester compass (for diameter and diametral measurements)
  - Decameter (for distances/lengths)
  - Botanist, local guides (data collection support)

## Provenance and References
- Programme: ESPA
- Project: P4GES
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data
- Documentation: Please also see Manual 1_Classical_Survey

## Relevance to Environment Monitoring
- Provides standardized dendrometric data essential for assessing above-ground biomass and forest structure.
- Facilitates cross-site comparisons (via Site_ID and ZOI) and temporal tracking through consistent measurement definitions.
- Supports integration with other environmental datasets to evaluate forest health, carbon stocks, and policy outcomes.

## Data Quality, Standards, and Access
- Data are prepared to be verified, quality assured, cleaned, and transformed before analysis.
- Outputs can be presented as reports, maps, and charts; datasets are stored and uploaded to appropriate portals.
- One of the aims for Analysts Monitoring the Environment is enabling access to underlying data used to create final outputs and increasing dataset value by combining with other relevant data.

## Practical Notes for Analysts
- Use Site_ID and ZOI to aggregate analyses by location and zone.
- Refer to Diameter_class and DBH for size-based stratification of biomass estimates.
- Pay attention to unit variations across fresh and dry weight fields; harmonize units before aggregation.
- Leverage X, X', Y, Y' coordinates and location data for spatial analyses and mapping of tree measurements.
- Consult the associated DOI and Manual 1_Classical_Survey for methodological context and data collection procedures.