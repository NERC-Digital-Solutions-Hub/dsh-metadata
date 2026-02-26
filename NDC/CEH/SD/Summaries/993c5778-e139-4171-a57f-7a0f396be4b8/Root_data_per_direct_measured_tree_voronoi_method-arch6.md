# DATA HEADER INFORMATION for: Root_data_per_direct_measured_tree_voronoi_method.csv

## Overview
- Metadata description for a dataset documenting Voronoi-sampled field data and the associated measurements.
- Part of the ESPA programme and P4GES project; references a related manual (Belowground Root Survey) and requires specific acknowledgement for derived products.
- Records sampling scheme details, location metadata, and a wide range of belowground biomass measurements across depth intervals and root types, plus leaf litter and mat root metrics.

## Key metadata and structure
- Zone of Interest (ZOI): Categorical; values include Andasibe and Anjahamana.
- Location information: 
  - Location: Name of sampling point location (text).
  - Site_Id: Site code (text).
  - Local_name: Vernacular/local species name (text).
- Code_target_tree: Identifier linking site, species, and diameter class (text).
- Diameter_class: Categorical (L: Large >20 cm; M: Medium 10–20 cm; S: Small ≤10 cm).
- Diameter: Numeric (tree diameter in cm).
- Code_voronoi: Voronoi triangle code (text).
- Position_slope: Categorical (Down / Top / - for small trees).
- Data quality hints: The header emphasizes data cleaning, verification with topic experts, and combining datasets for end-user self-service.

## Root biomass and depth-specific measurements
- Fine roots (FR): Depth bands 0–10 cm (FR0_10), 10–30 cm (FR10_30), 30–50 cm (FR30_50).
  - Total_fresh_weight_FRx_y: Total fresh weight of fine roots (g).
  - Sample_fresh_weight_FRx_y: Sample fresh weight (g).
  - Sample_dry_weight_FRx_y: Sample dry weight (g).
- Medium roots (MR): Depth bands 0–10 cm (MR0_10), 10–30 cm (MR10_30), 30–50 cm (MR30_50).
  - Total_fresh_weight_MRx_y: Total fresh weight (g).
  - Sample_fresh_weight_MRx_y: Sample fresh weight (g).
  - Sample_dry_weight_MRx_y: Sample dry weight (g).
- Coarse roots (CR): Coarse root measurements at various depth ranges for target tree roots and neighboring trees.
  - Target tree depths: t0_10, t10_30, t30_50 (e.g., Total_fresh_weight_CR_t0_10, Sample_fresh_weight_CR_t0_10, etc.; all in g).
  - Neighboring tree depths: o_0_10, o_10_30, o_30_50 (e.g., Total_fresh_weight_CR_o_0_10, Sample_fresh_weight_CR_o_0_10, etc.; all in g).
  - Includes total and sample fresh/dry weights for each depth band.
- Coarse-neighboring vs. coarse-target distinctions: Variables differentiate between target and neighboring coarse roots, enabling comparative analyses.

## Other belowground and surface measurements
- Leaf litter:
  - Thickness_leaf_litter: Thickness of leaf litter in cm (measured in a 25 cm² quadra).
  - Fresh_total_weight_leaf_litter: Fresh total weight (g).
  - Leaf_litter_sample_dry_weight: Dry weight (g).
  - Leaf_litter_sample_fresh_weight: Fresh weight (g).
- Mat root (mat_root) measurements:
  - Thickness_mat_root: Thickness of mat root in cm.
  - Fresh_total_weight_mat_root: Fresh total weight (g).
  - Mat_root_sample_dry_weight: Dry weight (g).
  - Mat_root_sample_fresh_weight: Fresh weight (g).

## Data quality and considerations for use
- The header includes a mix of clearly defined fields and some typographical inconsistencies (e.g., unit labels and description phrasing). Users should validate label consistency (e.g., “Total_fresh_weight_FR30_50” vs. “Sample_fresh_weight_FR30_50”) and confirm unit conventions (grams vs. other units) during data cleaning.
- Depth ranges and naming conventions are critical for proper aggregation (e.g., FRx_y and MRx_y bands); ensure uniform interpretation across datasets.
- The dataset is intended to support “self-serve” exploration through dashboards or reports and may require harmonization with related datasets (e.g., direct belowground survey methods) for integrated analyses.
- Acknowledge data origin when deriving products, per the dataset’s project requirements.

## Practical uses for data support
- Data discovery and understanding the ask: identify data sources (Voronoi sampling) and the full suite of belowground measurements available for root biomass across species, diameter class, and depth.
- Data preparation: clean and harmonize units, resolve typos, align depth bands across root types, and map Code_target_tree to site/species data for integrated analyses.
- Data products: create dashboards or pivot tables showing biomass by depth, root type, diameter class, and zone of interest; enable cross-filtering by location and species.
- Stakeholder communication: provide clear metadata and usage notes to facilitate sharing outputs with policy-makers, researchers, and local decision-makers.

## References and acknowledgments
- Data header references a related manual: Manual_2_Belowground_Root_Survey, page 9, section 2.3.1.
- DOI for the dataset: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
- Programme and project: ESPA and P4GES.
- Acknowledgement requirement: Laboratoire des Radio Isotopes, Université d'Antananarivo.