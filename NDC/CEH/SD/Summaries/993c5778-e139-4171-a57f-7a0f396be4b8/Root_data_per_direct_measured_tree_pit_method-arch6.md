# DATA HEADER INFORMATION for: Root_data_per_direct_measured_tree_pit_method.csv

- Overview
  - The dataset records information on target trees and their locations, using a direct measured tree pit method.
  - Associated with the ESPA Programme and the P4GES project.
  - DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
  - Acknowledgement is required for products derived from these data to Laboratoire des Radio Isotopes, Université d'Antananarivo.

- Data contents and structure
  - Spatial/identity fields:
    - Zone of Interest (ZOI): Categorical (e.g., Andasibe, Anjahamana).
    - Location: Text string (sampling point location name).
    - Site_Id: Text string (site code for where the target tree was collected).
    - Local_name: Text string (vernacular/local name of the inventoried species).
    - Code_target_tree: Text string (code linking site, species, and diameter class).
    - Diameter_class: Categorical (L = Large, M = Medium, S = Small) based on diameter.
    - Code_Pit: Categorical (P1, P2, P3) identifying pit location.
  - Root measurement data by size class and depth:
    - Fine roots (FR), Medium roots (MR), Coarse roots (CR).
    - Depth intervals: 0–10 cm, 10–30 cm, 30–50 cm.
    - For each class/depth, fields include:
      - Total_fresh_weight_<class>_<depth> (g)
      - Sample_fresh_weight_<class>_<depth> (g)
      - Sample_dry_weight_<class>_<depth> (g)
    - Example prefixes include FR (fine), MR (medium), CR (coarse) with corresponding depth ranges (e.g., FR_0_10, FR_10_30, FR_30_50, and similarly for MR and CR).
  - Additional biomass and litter components:
    - Thickness_leaf_litter (cm): leaf litter thickness measured in a 25 cm² quadrat.
    - Fresh_total_weight_of_leaf_litter (g)
    - Leaf_litter_sample_fresh_weight (g)
    - Leaf_litter_sample_dry_weight (g)
    - Thickness_mat_root (cm): thickness of mat-root within a Voronoï triangle.
    - Fresh_total_weight_of_Mat_root (g)
    - Mat_root_sample_fresh_weight (g)
    - Mat_root_sample_dry_weight (g)

- Data types and units
  - Numeric measurements in grams (g) for weights.
  - Depth-related measurements in centimeters (cm).
  - Diameter_class is a categorized field (L, M, S).
  - ZOI, Location, Site_Id, Local_name, Code_target_tree, Code_Pit are textual/categorical identifiers.

- Sampling and naming conventions
  - Each row associates a target tree with its location and pit, including a code that links site, species, and diameter class.
  - Depth- and size-class based biomass measurements enable analysis of root biomass distribution by depth and root category.
  - Unit consistency (g, cm) is maintained across root and litter/mat-root measurements.

- Data provenance and usage notes
  - The header provides the dataset’s context, project affiliation, and acknowledgments.
  - The DOI and project information should be cited in derivative products.
  - Acknowledgement conditions apply for outputs derived from these data.