# DATA HEADER INFORMATION for: Root_data_per_direct_measured_tree_pit_method.csv

## Overview
- Dataset records information on target tree and target tree location using the direct measured tree pit method.
- Part of ESPA programme and P4GES project; DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8.
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.
- Information is organized by Zone of Interest (ZOI) and target tree measurements, including location and pit identifiers.

## Key variables and data structure
- ZOI (Zone of Interest): Categorical; examples include Andasibe and Anjahamana.
- Location: Name of the sampling point location; Text String.
- Site_Id: Code for the site where the target tree was collected; Text String.
- Local_name: Vernacular/local name of the inventoried species; Text String.
- Code_target_tree: Code linking to site, species name, and diameter class; Text String.
- Diameter_class: Categorical; L = Large (>20 cm), M = Medium (10–20 cm), S = Small (<10 cm); measured with a forester compass.
- Code_Pit: Code identifying the pit location; Categorical (P1, P2, P3).

## Measurements and units (roots by depth and type)
- Fine roots (FR):
  - 0–10 cm: Total_fresh_weight_FR_0_10 (g); Sample_fresh_weight__FR_0_10 (g); Sample_dry_weight__FR_0_10 (g).
  - 10–30 cm: Total_fresh_weight_FR_10_30 (g); Sample_fresh_weight__FR_10_30 (g); Sample_dry_weight__FR_10_30 (g).
  - 30–50 cm: Total_fresh_weight_FR_30_50 (g); Sample_fresh_weight__FR_30_50 (g); Sample_dry_weight__FR_30_50 (g).

- Medium roots (MR):
  - 0–10 cm: Total_fresh_weight_MR_0_10 (g); Sample_fresh_weight__MR_0_10 (g); Sample_dry_weight__MR_0_10 (g).
  - 10–30 cm: Total_fresh_weight_MR_10_30 (g); Sample_fresh_weight__MR_10_30 (g); Sample_dry_weight__MR_10_30 (g).
  - 30–50 cm: Total_fresh_weight_MR_30_50 (g); Sample_fresh_weight__MR_30_50 (g); Sample_dry_weight__MR_30_50 (g).

- Coarse roots (CR):
  - 0–10 cm: Total_fresh_weight_CR_0_10 (g); Sample_fresh_weight__CR_0_10 (g); Sample_dry_weight__CR_0_10 (g).

- Notes on MR_0_10 entries: The metadata shows a coding convention (1 = label, 2 = Numeric, 3 = g) indicating data type encoding for some fields.

## Additional biophysical measurements
- Thickness_leaf_litter: Thickness of leaf litter in a 25 cm² quadrat (cm); Numeric.
- Fresh_total_weight_of_leaf_litter: Fresh total weight of leaf litter (g); Numeric.
- Leaf_litter_sample_fresh_weight: Leaf litter sample fresh weight (g); Numeric.
- Leaf_litter_sample_dry_weight: Leaf litter sample dry weight (g); Numeric.

- Thickness_mat_root: Mat root thickness in the Voronoï triangle (cm); Numeric.
- Fresh_total_weight_of_Mat_root: Fresh total weight of mat root (g); Numeric.
- Mat_root_sample_fresh_weight: Mat root sample fresh weight (g); Numeric.
- Mat_root_sample_dry_weight: Mat root sample dry weight (g); Numeric.

## Data provenance and usage notes
- The header specifies that the dataset corresponds to direct measurements from tree pits and includes hierarchical identifiers (ZOI, location, site, pit, diameter class) to support stratified analyses.
- All weight measurements are in grams; depths and thicknesses are in centimeters.
- The dataset is intended to support analyses of root biomass by depth and root diameter class, and to enable linking root biomass data with litter and mat root measurements.

## Access, attribution, and metadata
- DOI provided for dataset: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8.
- Project context: ESPA (Environmental Services Programme) and P4GES.
- Acknowledgement requirement: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.