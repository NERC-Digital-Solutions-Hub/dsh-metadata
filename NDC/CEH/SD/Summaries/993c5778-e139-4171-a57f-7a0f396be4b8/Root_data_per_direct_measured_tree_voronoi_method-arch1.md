# DATA HEADER INFORMATION for: Root_data_per_direct_measured_tree_voronoi_method.csv

## Overview
- Records information on the sampling scheme (Voronoi) construction in the field and the collected data.
- Includes project and program context, and data provenance identifiers (DOI, ESPA, P4GES).

## Metadata, identifiers and location data
- Data provenance and project context:
  - DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
  - Programme: ESPA; Project: P4GES
  - Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo
- Zone and location descriptors:
  - ZOI (Zone of Interest) and Location Information: ZOI is categorical; Location is a text string.
  - Location_name fields: Location, Site_Id, Local_name (vernacular name of the inventoried species)
  - Site_Id: site code; Code_target_tree links site and species with diameter class
- Target tree identification:
  - Code_target_tree: code for each target tree (linked to site and species)
  - Diameter_class: Large (L), Medium (M), Small (S); Diameter: numeric value

## Voronoi sampling and excavation positioning
- Code_voronoi: code for Voronoi triangle associated with the sampling
- Position_slope: position of the chosen Voronoi triangle for excavation (Down/Top); note that for the small tree this may be listed as a dash

## Plant and root measurements by depth and type
- Fine roots (FR)
  - Depth intervals: 0-10 cm, 10-30 cm, 30-50 cm
  - Metrics per interval:
    - Total_Fresh_weight_FRx_y (g)
    - Sample_Fresh_weight_FRx_y (g)
    - Sample_Dry_weight_FRx_y (g)
- Medium roots (MR)
  - Depth intervals: 0-10 cm, 10-30 cm, 30-50 cm
  - Metrics per interval:
    - Total_Fresh_weight_MRx_y (g)
    - Sample_Fresh_weight_MRx_y (g)
    - Sample_Dry_weight_MRx_y (g)
- Coarse roots (CR)
  - Categories per depth:
    - Target tree coarse roots: Total_fresh_weight_CR_t0_10, CR_t10_30, CR_t30_50 (g); Sample_fresh_weight_CR_tx_y; Sample_Dry_weight_CR_tx_y
    - Neighbouring coarse roots: Total_Fresh_weight_CR_o_0_10, CR_o_10_30, CR_o_30_50 (g); Sample_fresh_weight_CR_o_x_y; Sample_Dry_weight_CR_o_x_y
  - Depth ranges correspond to 0-10 cm, 10-30 cm, 30-50 cm
- Leaf litter and mat root context
  - Thickness_leaf_litter: thickness of leaf litter (cm)
  - Fresh_total_weight_leaf_litter: fresh total weight of leaf litter (g)
  - Leaf_litter_sample_fresh_weight: leaf litter sample fresh weight (g)
  - Leaf_litter_sample_dry_weight: leaf litter sample dry weight (g)
  - Thickness_mat_root: thickness of mat root inside the Voronoi triangle (cm)
  - Fresh_total_weight_mat_root: fresh total weight of mat root (g)
  - Mat_root_sample_fresh_weight: mat root sample fresh weight (g)
  - Mat_root_sample_dry_weight: mat root sample dry weight (g)

## Data types and units
- Units:
  - Weight measurements: grams (g)
  - Thickness measurements: centimeters (cm)
  - Depth classes: 0-10, 10-30, 30-50 cm
- Variable types:
  - Numeric for weights and thickness
  - Categorical for diameter class, ZOI, and position slope
  - Text strings for location identifiers and codes

## Usage, provenance and data handling
- Dataset combines multiple data components (root biomass by type and depth, leaf litter, mat roots) within a Voronoi-sampling framework to support analyses of biomass allocation and root distribution.
- Emphasizes traceability: Code_target_tree, Code_voronoi, Location and Site identifiers enable linking to field records and other datasets.
- Guidance points:
  - Data quality and consistency are important when merging across root types and depths.
  - The dataset is designed for replication and cross-study comparisons; metadata and DOIs should be used to locate the full data context.

## Project context and notes
- Project: ESPA and P4GES
- Acknowledgements indicate required attribution to Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.
- Minor formatting inconsistencies present in the header (e.g., occasional line breaks and phrasing); content maintains clear definitions of variables, units, and their roles in the Voronoi-based sampling framework.