# DATA HEADER INFORMATION for: Root_data_per_direct_measured_tree_voronoi_method.csv

## Overview
- Documents the sampling scheme (Voronoi) construction in the field and the collected data.
- Associated with ESPA (European Union’s Ecosystem Services Partnership) and the P4GES project; includes a DOI.
- Acknowledgement is required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).
- The header provides metadata descriptions for location, tree targets, and various below-ground and litter measurements.

## Data Structure and Key Variables
- Spatial and site metadata
  - ZOI (Zone of Interest): Categorical (e.g., ZOI2: Andasibe; ZOI3: Anjahamana).
  - Location: Name of sampling point location (text).
  - Site_Id: Code for the sampling site (text).
  - Local_name: Vernacular/local name of the inventoried species (text).
  - Code_target_tree: Code linking site, species, and diameter class (text).
  - Diameter_class: Categorical (Large >20 cm; Medium 10–20 cm; Small <10 cm).
  - Diameter: Numeric (tree diameter).
  - Code_voronoi: Voronoi triangle code (e.g., V[number]).
  - Position_slope: Position of Voronoi triangles chosen for excavation (Down / Top / - for small tree).

- Measurements by root type and depth
  - Fine roots (FR): 
    - FR0_10, FR10_30, FR30_50 with Total_Fresh_weight, Sample_Fresh_weight, Sample_Dry_weight (all in grams).
  - Medium roots (MR):
    - MR0_10, MR10_30, MR30_50 with Total_Fresh_weight, Sample_Fresh_weight, Sample_Dry_weight (in grams).
  - Coarse roots for target tree (CR_t):
    - t0_10, t10_30, t30_50 with Total_fresh_weight, Sample_fresh_weight, Sample_Dry_weight (in grams).
  - Coarse roots for neighboring tree (CR_o):
    - o_0_10, o_10_30, o_30_50 with Total_Fresh_weight, Sample_Fresh_weight, Sample_Dry_weight (in grams).
  - General notes:
    - Depth ranges are specified in the variable names (0–10 cm, 10–30 cm, 30–50 cm; and neighboring vs target trees).
    - Some lines mix capitalization (e.g., Total_fresh_weight vs Total_Fresh_weight) and contain typographical inconsistencies (e.g., G vs g).

- Other below-ground and surface measurements
  - Thickness_leaf_litter: Litter thickness (cm).
  - Fresh_total_weight_leaf_litter: Total fresh weight of leaf litter (grams).
  - Leaf_litter_sample_dry_weight and Leaf_litter_sample_fresh_weight (grams).
  - Thickness_mat_root: Thickness of mat root inside the Voronoï triangle (cm).
  - Fresh/Mat_root weights:
    - Fresh_total_weight_of_mat_root (grams)
    - Mat_root_sample_dry_weight (grams)
    - Mat_root_sample_fresh_weight (grams)

- Documentation notes
  - The dataset includes explicit, descriptive notes for each field, including unit expectations and measurement scope.
  - Some entries explicitly state the intended depth, context (target vs neighboring trees), and the Voronoi triangle reference.

## Data Provenance, Access, and Governance
- Source and project context
  - DOI provided for the dataset.
  - Programme: ESPA; Project: P4GES.
- Usage and attribution
  - Acknowledgement required for products derived from these data.
- Metadata quality and caveats
  - The header includes detailed descriptions of many fields, but there are formatting inconsistencies and typos (e.g., inconsistent capitalization of weight variables, occasional "G" vs "g", and truncated descriptions).
  - Some entries imply reliance on raw field notes or manual transcription, suggesting a need for careful data cleaning and standardisation before reuse.
- Data sharing considerations
  - While not prohibiting sharing, the header hints at the importance of clear provenance and consistent metadata to support reuse in monitoring frameworks.

## Relevance for Monitoring Framework Authors
- Provides a comprehensive, spatially explicit dataset tailored for below-ground biomass and litter monitoring using a Voronoi-based sampling design.
- Demonstrates a structured approach to capturing multi-depth, multi-root-type biomass alongside surface litter and mat-root measurements, suitable for informing policy evaluation and decision-making.
- Highlights practical governance considerations:
  - Importance of robust metadata, data provenance (DOI, project), and clear attribution.
  - Potential barriers to data reuse due to metadata quality, unit inconsistencies, and formatting issues, reinforcing the need for early data standardisation and documentation in monitoring frameworks.
- Facilitates dissemination and stakeholder engagement through clear variable definitions, enabling dashboards and policy-relevant reporting.