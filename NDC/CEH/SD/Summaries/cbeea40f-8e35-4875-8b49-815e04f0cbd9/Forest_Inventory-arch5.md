# DATA HEADER INFORMATION for Forest_inventory.csv

## Purpose and context
- Describes characteristics of trees located on the Zone of Interest.
- Part of ESPA Programme and P4GES project.
- DOI provided; cross-reference to Manual 1_Classical_Survey.

## Project, provenance, and acknowledgments
- Programme: ESPA (http://www.espa.ac.uk/); Project: P4GES (https://www.p4ges.org).
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Data content and schema
- Dataset describes tree-level measurements within plots.
- Key fields (with descriptions, types, and units):
  - Site_ID
    - Information: P4GES site code
    - Variable type: Text String
    - Unit: not specified
  - trees_subplot
    - Information: Subplot where the sample has been collected, classified by radius
    - Variable type: Categorical
    - Unit: Not specified
    - Categories: Small, Medium, Large (based on radius: 5m < Small < 10m, 10m < Medium < 20m, 20m < Large)
  - trees_area
    - Information: Surface of the sampling area (circular plot)
    - Variable type: Numeric
    - Unit: square meters (m²)
  - trees_local_name
    - Information: Vernacular/local name of the inventoried species
    - Variable type: Text String
    - Unit: Not specified
  - trees_scientific_names
    - Information: Scientific name of the inventoried species
    - Variable type: Text String
    - Unit: Not specified
  - trees_genera
    - Information: Genera of the selected tree
    - Variable type: Text String
    - Unit: Not specified
  - trees_family
    - Information: Family of the selected tree
    - Variable type: Text String
    - Unit: Not specified
  - trees_DBH
    - Information: Breast height diameter of the tree (diameter at 1.3m from ground level)
    - Variable type: Numeric
    - Unit: Centimeter
  - trees_height
    - Information: Total height of the tree (from ground to top)
    - Variable type: Numeric
    - Unit: Meter

## Metadata and accompanying materials
- Field_materials Resources: referenced for several fields (e.g., subplot, area, names, etc.).
- Related reference: Cross-check with Manual 1_Classical_Survey for fuller methodology.

## Data sharing, governance, and standards
- Data hosted for discovery and reuse; intended to be uploaded to relevant portals and catalogues.
- Data creators/sharers are expected to meet standards (metadata, format) consistent with the project.
- Collaboration with botanists/foresters for taxonomic and structural data (scientific names, genera, family, DBH, height).
- Acknowledgement requirement suggests provenance tracking and credit must be maintained.

## Quality, availability, and update considerations
- Completeness and consistency of metadata are important (note: some fields show unspecified units, e.g., Site_ID).
- Standardization across records needed (unit consistency: DBH in cm, height in m, area in m²).
- The header references potential updates and the need to respect sharing limitations or embargoes, indicating ongoing data availability management.

## Practical notes for Data Stewards
- Validate that Site_ID units are clearly defined or standardized.
- Ensure consistency of units and data types across all variables.
- Maintain cross-references to the ESPA/P4GES documentation and the Manual 1_Classical_Survey.
- Ensure proper attribution/acknowledgment when data products are derived.