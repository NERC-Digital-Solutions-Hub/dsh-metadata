# DATA HEADER INFORMATION for: Root_data_per_direct_measured_tree_voronoi_method.csv

- Purpose and scope
  - Documents the sampling scheme (Voronoi) used for field collection and the associated data. Records the sampling construction, locations, and a comprehensive set of root and related ecological measurements derived from direct measurement around target trees.

- Key metadata fields (highlights)
  - Spatial and location identifiers: Zone of Interest (ZOI), Location name, Site_Id, Local_name (vernacular species name).
  - Target and sampling geometry: Code_target_tree, Diameter_class (Large L, Medium M, Small S), Diameter (numeric), Code_voronoi, Position_slope (Down/Top/-).
  - Root biomass measurements by root type and depth:
    - Fine roots (FR): Total and Sample weights for depth bands 0-10 cm, 10-30 cm, 30-50 cm; both fresh and dry weights (units: grams).
    - Medium roots (MR): Same structure as fine roots across depth bands and weight types.
    - Coarse roots (CR): Total and Sample weights for 0-10 cm, 10-30 cm, 30-50 cm; also separate for coarse target tree roots and neighbouring tree roots; includes fresh and dry weights.
  - Additional components and measurements:
    - Leaf litter: Thickness (cm) and Fresh/Dry weights (total and samples).
    - Mat roots: Thickness (cm) and Fresh/Dry weights (total and samples).
    - Variable naming includes some inconsistencies and typos (e.g., unit notations and partial descriptions) but follows a wide, hierarchical structure by root type and depth.

- Provenance, access, and attribution
  - DOI provided for dataset access: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
  - Programme and project: ESPA; Project P4GES
  - Acknowledgement requirement: Laboratoire des Radio Isotopes, Université d'Antananarivo must be acknowledged for products derived from these data.

- Data quality and metadata considerations
  - Field names and descriptions are extensive but contain formatting inconsistencies and some incomplete phrases (e.g., some unit labels and descriptive text).
  - Data appear to be a wide, flat schema with multiple root categories and depth-based biomass measurements; careful validation needed to ensure consistent units and mappings across records.

- Data governance and reuse guidance
  - Useful for assessing root biomass distribution around target and neighboring trees, root-system architecture, and related soil-litter context.
  - Requires alignment with internal data standards for units, depth band definitions, and root-type classifications to ensure interoperability.
  - Encourages clear attribution and adherence to data-use requirements given the provenance and acknowledgment needs.

- Practical recommendations for Data Leaders
  - Implement data standardization across root type (FR/MR/CR), depth bands, and measurement units (confirm grams and depth intervals).
  - Establish metadata quality checks to resolve inconsistencies in field descriptions and unit labeling.
  - Promote co-ownership and user-centric iteration for data products, ensuring the dataset supports policy and cross-network collaboration.
  - Integrate with broader data systems to improve discoverability (utilize the DOI and project affiliations) and support data sharing with partners.