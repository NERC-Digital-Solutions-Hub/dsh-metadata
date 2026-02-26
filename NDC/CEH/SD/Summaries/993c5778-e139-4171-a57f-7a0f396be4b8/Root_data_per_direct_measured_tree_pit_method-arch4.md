# DATA HEADER INFORMATION for: Root_data_per_direct_measured_tree_pit_method.csv

## Overview
- Metadata-driven dataset documenting target trees and their locations for a belowground root survey, linked to ESPA and P4GES projects.
- Includes identification, location, and sampling metadata to support analysis of root and related ecological measurements.
- DOI provided; acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data.

## Data scope and structure
- Zone of Interest (ZOI): Categorical, e.g., Andasibe, Anjahamana.
- Location: sampling point name; Site_Id: site code; Local_name: vernacular/species name.
- Code_target_tree: unique code tying site, species, and diameter class.
- Diameter_class: Large (>20 cm), Medium (10–20 cm), Small (<10 cm); measured with a forester compass.
- Code_Pit: pit identifier (P1, P2, P3).
- Measurements span root categories:
  - Fine roots (FR), Medium roots (MR), Coarse roots (CR)
  - Depth bands: 0–10 cm, 10–30 cm, 30–50 cm
  - For each category and depth: Total_fresh_weight, Sample_fresh_weight, Sample_dry_weight (units: grams)
- Depth/radius metadata encoded in variable names (e.g., FR_0_10, MR_10_30, CR_30_50).

## Additional ecological measurements
- Thickness_leaf_litter: leaf litter thickness per quadrat (cm).
- Fresh_total_weight_of_leaf_litter; Leaf_litter_sample_fresh_weight; Leaf_litter_sample_dry_weight (units: grams).
- Thickness_mat_root: mat root thickness inside sampling context (cm); Fresh_total_weight_of_Mat_root; Mat_root_sample_fresh_weight; Mat_root_sample_dry_weight (units: grams).

## Data types and units
- Variables include Numeric, Text String, and Categorical types.
- Units explicitly specified for weights (grams) and thickness (centimeters); diameter class and codes use categorical/text formats.

## Data governance and credits
- Data supported by ESPA and P4GES programs; includes formal DOI for dataset reference.
- Acknowledgement requirement specifies Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from the data.

## Implications for Data Leaders
- Rich, well-structured metadata enhances data quality, discoverability, and reusability for cross-team and cross-network collaboration.
- Enables standardized data products across studies through clear variable definitions, units, and coding schemes.
- Highlights the importance of formal governance (DOI, project attribution, acknowledgments) to maintain data integrity and proper use.

## Challenges and considerations
- Complex, multi-category root data across multiple depths may require strict standardization when integrating with other datasets.
- Ensure ongoing updates and versioning of metadata to maintain consistency across projects and time.
- Be mindful of data access and attribution constraints linked to project partners and acknowledgments.