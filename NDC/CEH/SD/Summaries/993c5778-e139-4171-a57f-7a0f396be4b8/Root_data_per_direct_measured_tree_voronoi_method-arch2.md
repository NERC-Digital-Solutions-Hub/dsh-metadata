# DATA HEADER INFORMATION for: Root_data_per_direct_measured_tree_voronoi_method.csv

## Overview
- Defines the schema and metadata for the Root_data_per_direct_measured_tree_voronoi_method.csv dataset, capturing field measurements and sampling scheme (Voronoi construction) used in the study.
- Linked references: Manual_2_Belowground_Root_Survey (section 2.3.1), DOI provided; ESPA programme and P4GES project.
- Acknowledgement requirement: Labouratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Data provenance and identifiers
- Zone of Interest (ZOI): Categorical (ZOI2: Andasibe; ZOI3: Anjahamana).
- Location: Text string (sampling point name).
- Site_Id: Text string (site code where the target tree was collected).
- Local_name: Text string (vernacular/local name of the species inventoried).
- Code_target_tree: Text string (code linking site, species name, and diameter class).
- Diameter_class: Categorical (L = Large, M = Medium, S = Small) with descriptive thresholds.
- Diameter: Numeric (tree diameter in unspecified units).
- Code_voronoi: Text string (Voronoi triangle code).
- Position_slope: Categorical (values such as Down, Top, or dash for small trees).

## Data types and structure
- Data types include Text String (locations and codes), Categorical (ZOI, Diameter_class, Position_slope), and Numeric (weights, diameters).
- Many fields describe measurement outputs and their units; data are arranged by depth bands and root type.

## Variables and measurements
- Root categories and depth bands (all weights in grams where specified):
  - Fine roots (FR): 0-10 cm, 10-30 cm, 30-50 cm
    - Total_Fresh_weight_FR<depth>, Sample_Fresh_weight_FR<depth>, Sample_Dry_weight_FR<depth>
  - Medium roots (MR): 0-10 cm, 10-30 cm, 30-50 cm
    - Total_Fresh_weight_MR<depth>, Sample_Fresh_weight_MR<depth>, Sample_Dry_weight_MR<depth>
  - Coarse roots (CR) associated with target tree (t) and neighbouring tree (o): depth bands 0-10 cm, 10-30 cm, 30-50 cm
    - Total_fresh_weight_CR_t<depth>, Sample_fresh_weight_CR_t<depth>, Sample_Dry_weight_CR_t<depth>
    - Total_fresh_weight_CR_o<depth>, Sample_fresh_weight_CR_o<depth>, Sample_Dry_weight_CR_o<depth>
  - Coarse target tree and related measures (t) and (o) descriptions include prefixes Total_fresh_weight_CR_tXX_YY, Sample_fresh_weight_CR_tXX_YY, etc., with depth indicators.
- Leaf litter and mat root context:
  - Thickness_leaf_litter: measured thickness (cm) for leaf litter within a specified area.
  - Fresh total weight of leaf litter; Leaf_litter_sample_dry_weight; Leaf_litter_sample_fresh_weight.
  - Thickness_mat_root: thickness (cm) of mat root inside the Voronoï triangle.
  - Fresh total weight of mat root; Mat_root_sample_dry_weight; Mat_root_sample_fresh_weight.
- Miscellaneous notes:
  - Some field names and descriptions show minor typographical inconsistencies (e.g., "Total_Fresh_weight_FR30_50" units labeled inconsistently as "G" or "g"). Weight-related fields consistently use grams in description.

## Standards, units, and conventions
- Depth ranges are in centimeters (e.g., 0-10, 10-30, 30-50 cm).
- Weights are in grams (g), with several fields explicitly indicating numeric values.
- Diameter_class uses concise categorical codes (L, M, S) with size thresholds.
- ZOI, Location, and Code fields use text/categorical types to support standardized filtering and mapping.

## Data quality, accessibility, and management
- Emphasises verification, quality assurance, cleaning, and transformation of data prior to analysis.
- Outputs are intended to be presented in clear formats (reports, maps, charts) and stored/uploaded to appropriate data portals.
- Encourages increasing data value by enabling integration with other relevant datasets and ensuring underlying data is accessible to others.

## Practical notes for analysts
- Use standardized variable definitions to enable cross-site comparisons and temporal analyses.
- Cross-check depth-band groupings and root-type classifications when aggregating data.
- Be mindful of minor inconsistencies in metadata labeling and ensure consistent units across analyses.
- Refer to the linked manual and DOI for methodological details and ensure proper citation and data usage compliance.