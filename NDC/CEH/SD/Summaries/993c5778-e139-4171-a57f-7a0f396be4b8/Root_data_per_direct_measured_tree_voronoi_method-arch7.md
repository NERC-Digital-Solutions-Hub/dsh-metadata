# DATA HEADER INFORMATION for: Root_data_per_direct_measured_tree_voronoi_method.csv

- Purpose and scope
  - Records information on the sampling scheme (Voronoi) construction in the field and the collected data.
  - Related documentation: Manual_2_Belowground_Root_Survey, page 9, section 2.3.1, c.
  - DOI provided for the dataset and project context.
  - Acknowledgement requirement for products derived from these data.

- Project and access context
  - Programme: ESPA
  - Project: P4GES
  - Data product lineage and attribution details included in the header.

- Spatial and sampling metadata
  - Zone of Interest (ZOI): Categorical; examples include ZOI2: Andasibe, ZOI3: Anjahamana.
  - Location: Name of the sampling point location; Text string.
  - Site_Id: Code for the site where the target tree was collected; Text string.
  - Local_name: Vernacular/local name of the inventoried species; Text string.

- Target tree and sampling identifiers
  - Code_target_tree: Code assigned to each target tree; Text string (links to site/species/diameter context).
  - Diameter_class: Categorical class for diameter (Large, Medium, Small) with thresholds >20 cm, 10–20 cm, etc.
  - Diameter: Numeric value for tree diameter.
  - Code_voronoi: Code for the Voronoi triangle (e.g., V+number of pickets).
  - Position_slope: Categorical indicator of which Voronoi triangle was excavated (Down / Top / - for small trees).

- Data types and units
  - Field data types include Text String, Numeric, and Categorical.
  - Units include grams (g) for weights, centimeters (cm) for thickness/depth, and dimensionless or unspecified units where noted.
  - Several fields have consistent naming conventions across root size classes and depths to facilitate GIS-based joining and visualization.

- Root measurements by depth and type
  - Fine roots (FR) by depth: FR0_10, FR10_30, FR30_50
  - Medium roots (MR) by depth: MR0_10, MR10_30, MR30_50
  - Coarse roots (CR) by depth for various contexts:
    - CR_t0_10, CR_t10_30, CR_t30_50 (coarse target tree roots)
    - CR_o_0_10, CR_o_10_30, CR_o_30_50 (coarse neighbouring tree roots)
  - For each root category and depth, the dataset includes:
    - Total_fresh_weight (g)
    - Sample_fresh_weight (g)
    - Sample_dry_weight (g)
  - Depth ranges cover 0–10 cm, 10–30 cm, and 30–50 cm (with some naming variances in the header text).

- Leaf litter and mat root measurements
  - Thickness_leaf_litter (cm)
  - Fresh_total_weight_leaf_litter (g)
  - Leaf_litter_sample_dry_weight (g)
  - Leaf_litter_sample_fresh_weight (g)
  - Thickness_mat_root (cm)
  - Fresh_total_weight_mat_root (g)
  - Mat_root_sample_dry_weight (g)
  - Mat_root_sample_fresh_weight (g)

- Additional measurement fields
  - Thickness and weight metrics for mat roots and various root components, with explicit references to depth ranges and sample types.
  - Some fields include notes indicating the measurement context (e.g., “from 0 to 10 cm,” “from 30 to 50 cm,” etc.) and occasional textual placeholders where units or definitions are not provided.

- Data quality and usage considerations
  - Emphasizes data cleaning and transformation as part of preparing GIS-ready data.
  - Highlights potential challenges in aggregating fine, medium, and coarse root data across multiple depths and Voronoi triangles for visualization and analysis.

- References and acknowledgments
  - DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
  - ESPA and P4GES project references included for context and attribution.
  - Acknowledgement of the Laboratoire des Radio Isotopes, Université d'Antananarivo required for derived products.