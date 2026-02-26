# DATA HEADER INFORMATION for: Root_data_per_direct_measured_tree_pit_method.csv

## Overview
- Metadata describing dataset that records information on target trees and their sampling locations, using a direct measured tree pit method.
- Associated with ESPA program and P4GES project; DOI provided for dataset access.
- Acknowledgement is required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Dataset structure and key variables
- Geographic and site identifiers
  - Zone of Interest (ZOI): Categorical with examples Andasibe, Anjahamana.
  - Location: Text string naming the sampling point location.
  - Site_Id: Text string code identifying the sampling site.
  - Local_name: Vernacular/local name of the inventoried species.
  - Code_target_tree: Text code linking site, species, and diameter class to each target tree.

- Tree and diameter information
  - Diameter_class: Categorical class of tree diameter (L: Large >20 cm, M: Medium 10–20 cm, S: Small <10 cm).

- Pit and sampling details
  - Code_Pit: Category code for pit location (P1, P2, P3).

- Root measurements by depth and type
  - Fine roots (FR)
    - Depth bands: 0–10 cm, 10–30 cm, 30–50 cm.
    - Variables include Total_fresh_weight_FR_<depth>, Sample_fresh_weight__FR_<depth>, Sample_dry_weight__FR_<depth> (all in grams).
  - Medium roots (MR)
    - Depth bands: 0–10 cm, 10–30 cm, 30–50 cm.
    - Variables include Total_fresh_weight_MR_<depth>, Sample_fresh_weight__MR_<depth>, Sample_dry_weight__MR_<depth> (gram units; numeric).
  - Coarse roots (CR)
    - Depth bands: 0–10 cm (and presumably additional bands as implied by FR/MR structure), with Total_fresh_weight_CR_<depth>, Sample_fresh_weight__CR_<depth>, Sample_dry_weight__CR_<depth> (grams; numeric).

- Litter and mat-root components
  - Thickness_leaf_litter: Measured thickness of leaf litter within a 25 cm² quadrat (cm); numeric.
  - Fresh_total_weight_of_leaf_litter: Fresh weight of leaf litter (grams); numeric.
  - Leaf_litter_sample_fresh_weight and Leaf_litter_sample_dry_weight: Weights for leaf litter samples (grams); numeric.
  - Thickness_mat_root: Thickness/weight context for mat roots within a Voronoï triangle (cm); numeric.
  - Fresh_total_weight_of_Mat_root, Mat_root_sample_fresh_weight, Mat_root_sample_dry_weight: Fresh and sample weights for mat roots (grams); numeric.

- Data types and units
  - Weights: Numeric (grams).
  - Thickness and depth-related classifications: Numeric (centimeters for thickness; depth bands specified).
  - Identifiers and names: Text/String.
  - Diameter_class and Code_Pit: Categorical.

## Data quality, standards, and governance notes
- Data alignment with object definitions
  - Ensure Code_target_tree correctly encodes site, species, and diameter class linkage.
  - Maintain consistent coding for Zone of Interest, Site_Id, Location, Local_name, Code_Pit across records.
- Metadata completeness
  - Units are explicitly specified (grams for weights; centimeters for thickness).
  - Depth categories are standardized (0–10, 10–30, 30–50 cm).
- Sharing and updates
  - Data may be shared via portals/catalogues; updates should preserve existing codes and units to avoid breaking links to Code_target_tree and Code_Pit.
- Accessibility considerations
  - Location and site identifiers should be managed with appropriate governance if embedding sensitive site information; follow project and institutional policies.

## Provenance and usage notes
- Original data source and project context
  - Data tied to ESPA program and P4GES project; DOI provided for dataset access and citation.
- Acknowledgement requirements
  - Any products derived from these data must acknowledge Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Practical takeaways for data stewardship
- Verify and maintain the integrity of linking fields (Code_target_tree, Code_Pit, Site_Id) to ensure accurate cross-referencing between trees, pits, and locations.
- Preserve unit conventions and depth definitions across all root and litter/mat-root measurements to enable reliable aggregation and comparison.
- Document any data processing steps that generate derived values (e.g., totals vs. samples) to support reproducibility and traceability.