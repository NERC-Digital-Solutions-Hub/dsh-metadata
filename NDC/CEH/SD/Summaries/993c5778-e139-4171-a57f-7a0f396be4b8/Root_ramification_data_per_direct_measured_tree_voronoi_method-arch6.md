# DATA HEADER INFORMATION for: Root_ramification_data_per_direct_measured_tree_voronoi_method.csv Please also see Manual_2_Belowground_Root_Survey, page 10.

## Overview
- Records target tree root architecture: each coarse root (up to 1 cm diameter) branching is tagged and measured for every target tree.
- Measurements are taken using the Voronoi method, with ramification data associated to individual trees.

## Data structure and fields
- ZOI: Zone of Interest; Categorical; Unit: ZOI2 (Andasibe) / ZOI3 (Anjahamana)
- Site: Code for the site where the sample was collected; Text
- Local name: Vernacular/local name of the inventoried species; Text
- DBH Class: Diameter at Breast Height class; Categorical; Values: Large (L), Medium (M), Small (S)
- Code_target_tree: Identifier for each target tree (combines site, species, and diameter class); Text
- Number of ramification: Number of ramification branches from the north; Numeric
- DiH: Horizontal diameter at the beginning of each ramification; Numeric; Centimeters
- DiV: Vertical diameter at the beginning of each ramification; Numeric; Centimeters
- DfV: Vertical diameter at the end of each ramification; Numeric; Centimeters
- DfH: Horizontal diameter at the end of each ramification; Numeric; Centimeters
- DfM: Mean diameter ending of each ramification; Numeric; Computed as (DfH + DfV) / 2; Centimeters
- Total_weight: Weight of each ramification; Numeric; Grams
- Total_length: Length of each ramification; Numeric; Centimeters
- Orientation: Direction of ramification; Categorical; Values include Vor (from Voronoi triangle), PV (taproot), N, S, E, W, NA
- NA: Not available (unable to see ramification direction because root under tree or immobile stone); Categorical

## Data provenance and references
- DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
- Programme: ESPA
- Project: P4GES
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data

## Usage and integration notes for data support
- Purpose: Enable exploration of root architecture by tree, site, and diameter class; supports creation of data products for exploration (dashboards, pivot tables, reports).
- Linkability: Fields such as Site, Code_target_tree, and ZOI facilitate joining with other datasets (e.g., Manual_2_Belowground_Root_Survey) for richer analyses.
- Derived metrics: DfM can be computed if not stored; can build summaries of ramification size, length, and weight by category (DBH Class, Site, ZOI).

## Potential data quality and handling considerations
- Some Orientation values may be NA (unavailable due to obstruction); plan for missing data in analyses.
- Data may be patchy across sites or ramification records; implement validation when merging with other data sources.
- Ensure correct handling of units (cm, g) and consistent data types during transformations.

## How this supports data products
- Dashboards: summarize ramification counts, lengths, and weights by site, ZOI, or DBH Class.
- Self-serve analyses: enable filtering by Code_target_tree or Orientation to explore root architecture patterns.
- Reporting: generate per-tree or per-site summaries to inform belowground root studies and related policy or conservation decisions.