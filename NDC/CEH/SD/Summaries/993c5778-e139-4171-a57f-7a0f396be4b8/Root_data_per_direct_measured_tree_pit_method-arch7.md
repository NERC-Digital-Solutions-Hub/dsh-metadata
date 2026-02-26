# DATA HEADER INFORMATION for: Root_data_per_direct_measured_tree_pit_method.csv

## Overview
- The dataset records information on target tree and its sampling location.
- It includes references to data provenance and acknowledgments, DOIs, and related projects.
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo must be cited for products derived from these data.
- Provenance: ESPA programme; P4GES project.

## Spatial and sampling context
- Zone of Interest (ZOI) is categorical, with examples: ZOI2: Andasibe; ZOI3: Anjahamana.
- Location information = name of the sampling point location (text).
- Site_Id = code assigned to the sampling site (text).
- Local_name = vernacular/local name of the inventoried species (text).
- Code_target_tree = code for each target tree; linked to site and species with diameter class information.
- Diameter_class = tree diameter category: Large (L, >20 cm); Medium (M, 10–20 cm); Small (S, <10 cm).

## Data fields and structure
- Code_Pit = pit identifier (P1, P2, P3).
- Root biomass by type and depth:
  - Fine roots (FR) across depth bands: 0–10 cm, 10–30 cm, 30–50 cm.
  - Medium roots (MR) across the same depth bands.
  - Coarse roots (CR) across the same depth bands.
- For each root type and depth band, fields include:
  - Total_fresh_weight_<type>_<depth> (g)
  - Sample_fresh_weight_<type>_<depth> (g)
  - Sample_dry_weight_<type>_<depth> (g)
- Units for weight measurements: grams (g); values are numeric.

## Additional ecological measurements
- Leaf litter measurements:
  - Thickness_leaf_litter (measured in cm; collected in a 25 cm² quadrat)
  - Fresh_total_weight_of_leaf_litter (g)
  - Leaf_litter_sample_fresh_weight (g)
  - Leaf_litter_sample_dry_weight (g)
- Mat root measurements (within a Voronoï triangle):
  - Thickness_mat_root (cm)
  - Fresh_total_weight_of_Mat_root (g)
  - Mat_root_sample_fresh_weight (g)
  - Mat_root_sample_dry_weight (g)

## Data provenance and usage notes
- DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
- Programme: ESPA
- Project: P4GES
- The header defines data types, units, and labeling conventions to support GIS-based integration and map visualizations of root and litter measurements by species, site, and depth.