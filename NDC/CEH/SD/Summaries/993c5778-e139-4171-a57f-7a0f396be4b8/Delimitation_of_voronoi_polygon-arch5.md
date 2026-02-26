# DATA HEADER INFORMATION for Delimitation_of_voronoi_polygon.csv

- Purpose: Describes the header metadata for the Delimitation_of_voronoi_polygon.csv dataset, which presents the target tree environment and is linked to related manuals and project outputs.
- References and provenance:
  - DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
  - Programme: ESPA
  - Project: P4GES
  - Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo
  - Related manual: Manual_2_Belowground_Root_Survey, page 7, section 2.3.1

## Key metadata and governance considerations

- Data stewardship focus: metadata completeness, standardization of field definitions, and traceability to project and DOI for discovery and reuse.
- Sharing and citation: clear attribution requirements and link to project information and acknowledgements.
- Cross-reference needs: consult the linked manual for additional data standards and context.

## Data structure and variable definitions (header content)

- ZOI (Zone of Interest)
  - Information: Zone of Interest
  - Variable Type: Categorical
  - Unit: ZOI2 (Andasibe) / ZOI3 (Anjahamana)
- Code
  - Information: Unique code for the target tree (site code + local name initial + size indicator L/M/S)
  - Variable Type: Text String
  - Unit: (not specified)
- N° (Number of neighboring trees)
  - Information: Number of neighboring trees in the direction of a watch hand
  - Variable Type: Numeric
  - Unit: Unitless
- Neighbour tree name
  - Information: Name of the neighboring tree
  - Variable Type: Text String
  - Unit: (not specified)
- Distance_from_target_tree
  - Information: Distance from the target tree to each neighbour
  - Variable Type: Numeric
  - Unit: Meter
- % (Importance of target tree size relative to neighbour)
  - Information: Calculated as % = (DBH_T + DBH_N) / DBH_T × 100
  - Variable Type: Numeric
  - Unit: Percentage
- Distance of the picket
  - Information: Distance from the target tree to the picket location (defining the final Voronoi delimitation)
  - Variable Type: Numeric
  - Unit: Meter
- Height neighbour tree
  - Information: Total height of each neighbouring tree (1.30 m DBH reference)
  - Variable Type: Numeric
  - Unit: Meter
- N° Picket 1
  - Information: Number/identifier of the first picket
  - Variable Type: Numeric
  - Unit: (not specified)
- N° Picket 2
  - Information: Number/identifier of the second picket
  - Variable Type: Numeric
  - Unit: (not specified)
- Distance between picket
  - Information: Distance between two neighbouring pickets
  - Variable Type: Numeric
  - Unit: Meter
- Height of each triangle
  - Information: Height of each triangle formed with the target tree and pickets
  - Variable Type: Numeric
  - Unit: Centimeter
- Base of each triangle
  - Information: Base of each triangle
  - Variable Type: Numeric
  - Unit: Meter
- Area of each triangle
  - Information: Area of each triangle (based on the triangle formed with target and neighbour trees)
  - Variable Type: Numeric
  - Unit: m²
- Forester compass fields
  - Information: Associated orientation/tools (e.g., forester compass) for several fields
  - Variable Type: Various (not fully specified)
  - Unit: (not specified)
- Field and materials resources
  - Information: Resources or materials used for each field
  - Variable Type: (not specified)
  - Unit: (not specified)
  - Note: Several fields contain no listed resources (denoted by "."); governance guidance is to document or populate these where applicable to improve provenance.

## Data provenance, publication, and usage considerations

- Publication and citation:
  - Ensure proper citation via the provided DOI and project references (ESPA, P4GES).
  - Acknowledge Laboratoire des Radio Isotopes, Université d'Antananarivo for derived products.
- Documentation and manuals:
  - Cross-check with Manual_2_Belowground_Root_Survey (page 7, section 2.3.1) for related data structures and conventions.
- Versioning and updates:
  - Maintain clear versioning and update notes to reflect changes in header definitions or variable interpretations.

## Data quality, completeness, and gaps

- Completeness:
  - The header includes many descriptive fields, but several "Field and materials resources" entries are blank, indicating gaps in provenance documentation.
  - Some units and field descriptors (e.g., forester compass, certain resources) are inconsistently populated.
- Consistency and interoperability:
  - Ensure consistent unit usage (e.g., meters vs. Centimeters) and consistent naming for ZOI categories across datasets.
  - Validate computed fields (e.g., the % formula) against actual DBH data to ensure accuracy.
- Recommendations for data stewards:
  - Fill in missing metadata in all fields where possible (especially Field and materials resources, units, and forester compass references).
  - Standardize units and ensure clear definitions for all variables.
  - Maintain a data dictionary aligned with these headers to support discoverability and reuse.