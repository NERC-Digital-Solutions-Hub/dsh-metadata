# DATA HEADER INFORMATION for: Root_data_per_direct_measured_tree_pit_method.csv

- The dataset documents information on target trees and their sampling locations using a direct measured tree pit method, as part of ESPA Project P4GES (DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8).
- Acknowledgement is required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Overview of purpose and scope

- Captures per-tree and per-site information, including zone of interest (ZOI) and sampling point locations.
- Provides detailed root biomass measurements across root size classes (fine, medium, coarse) and depth intervals, plus associated sample and dry weights.
- Includes additional belowground and litter measurements (leaf litter thickness and weights; mat root data) to support holistic environmental health assessments.
- Structured to support data provenance, traceability, and integration with monitoring workflows.

## Key fields and data structure

- Target tree and location identifiers
  - ZOI (Zone of Interest): Categorical, examples include Andasibe / Anjahamana.
  - Location: Text string describing sampling point location.
  - Site_Id: Text string code for the sampling site.
  - Local_name: Vernacular/local name of the inventoried species.
  - Code_target_tree: Code for each target tree, linked to site, species, and diameter class.
  - Diameter_class: Categorical, with classifications such as Large (L), Medium (M), Small (S).

- Pit and sampling details
  - Code_Pit: Code identifying pit location (P1/P2/P3).

- Root biomass measurements by size class and depth
  - Fine roots (FR): Depth bands 0-10 cm, 10-30 cm, 30-50 cm
    - Total_fresh_weight_FR_<depth>, Sample_fresh_weight__FR_<depth>, Sample_dry_weight__FR_<depth> (all Numeric, Unit: grams)
  - Medium roots (MR): Depth bands 0-10 cm, 10-30 cm, 30-50 cm
    - Total_fresh_weight_MR_<depth>, Sample_fresh_weight__MR_<depth>, Sample_dry_weight__MR_<depth> (all Numeric, Unit: grams)
  - Coarse roots (CR): Depth band 0-10 cm (with corresponding weights)
    - Total_fresh_weight_CR_0_10, Sample_fresh_weight__CR_0_10, Sample_dry_weight__CR_0_10 (Numeric, Unit: grams)

- Additional belowground and litter measurements
  - Thickness_leaf_litter: Measured in centimeters (depth of leaf litter within a quadrat)
  - Fresh_total_weight_of_leaf_litter: Total fresh weight (grams)
  - Leaf_litter_sample_fresh_weight, Leaf_litter_sample_dry_weight: Weights for leaf litter samples (grams)
  - Thickness_mat_root: Thickness of mat roots (centimeters)
  - Fresh_total_weight_of_Mat_root: Fresh weight of mat roots (grams)
  - Mat_root_sample_fresh_weight, Mat_root_sample_dry_weight: Mat root sample weights (grams)

- Data types and units
  - Variable types include Numeric, Text String, and Categorical (e.g., diameter_class)
  - Units commonly in grams (g), centimeters (cm), and depth bands in centimeters

## Data provenance and governance

- Data origin and project context:
  - ESPA programme; Project P4GES
  - DOI provided for the dataset: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
- Acknowledgement requirement:
  - Explicit acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## How this supports monitoring and environmental health frameworks

- Provides a structured, metadata-rich schema enabling consistent recording of per-tree belowground biomass and related measurements.
- Facilitates comparability across sites (via ZOI, site_id, code_target_tree, diameter_class) and across depth intervals and root size classes.
- Supports data quality and governance through clearly defined variable types, units, and descriptive field definitions.
- Enhances reproducibility and transparency in environmental monitoring by linking to data provenance (DOI, program/project context) and requiring proper attribution.