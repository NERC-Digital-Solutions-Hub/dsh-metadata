# DATA HEADER INFORMATION for Forest_inventory.csv

## Overview
- Describes characteristics of trees located on the Zone of Interest within the ESPA Programme, Project P4GES.
- Data header includes field definitions, data types, units, and provenance for the Forest_inventory.csv.
- Acknowledgement requirement: products derived from these data must credit Laboratoire des Radio Isotopes, Université d'Antananarivo.
- References and access: DOI and project websites provided.

## Key fields and data schema
- Site_ID
  - Information: P4GES site code
  - Variable type: Text String
  - Unit: not specified
- trees_subplot
  - Information: Subplot where the sample has been collected; classified by radius: 5 m (Small) < 10 m, 10 m (Medium) < 20 m, 20 m (Large)
  - Variable type: Categorical
  - Unit: L: Large / M: Medium / S: Small
- trees_area
  - Information: Surface of the sampling area (circular plot)
  - Variable type: Numeric
  - Unit: square meters (m²)
- trees_local_name
  - Information: Vernacular/local name of the inventoried species
  - Variable type: Text String
  - Unit: not specified
- trees_scientific_names
  - Information: Scientific name of the inventoried species
  - Variable type: Text String
  - Unit: not specified
- trees_genera
  - Information: Genera of the selected tree
  - Variable type: Text String
  - Unit: not specified
- trees_family
  - Information: Family of the selected tree
  - Variable type: Text String
  - Unit: not specified
- trees_DBH
  - Information: Breast height Diameter of the tree (diameter at 1.3 m from ground level)
  - Variable type: Numeric
  - Unit: Centimeter
- trees_height
  - Information: Total height of the tree (from ground to top of tree)
  - Variable type: Numeric
  - Unit: Meter
- Field_materials Ressources (per field entries)
  - Examples: trees_area, Field_materials Ressources = . ; trees_local_name, Field_materials Ressources = botanist; trees_DBH, Field_materials Ressources = forester compass; trees_height, Field_materials Ressources = vertex
  - Note: Indicates data collection or reference resources associated with each field; formatting inconsistencies observed in the header.

## Provenance and references
- Programme: ESPA (Environmental Services for Africa)
  - Website: http://www.espa.ac.uk/
- Project: P4GES
  - Website: https://www.p4ges.org
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement: Required for products derived from these data; Laboratory of Isotopes (Laboratoire des Radio Isotopes), Université d'Antananarivo

## Data quality considerations
- Header includes both data definitions and metadata; some field labels contain inconsistencies (e.g., “Field_materials Ressources”).
- Units are specified for several fields, but some fields lack explicit units or have placeholders; verify before analysis.
- Some fields describe categorical or textual classifications (e.g., trees_subplot categories) that should be standardized (L/M/S vs. numeric radius ranges) for consistent analysis.
- The header provides structure but not actual data values; further data cleaning may be needed to ensure consistency across records.

## How Data Support can help (archetype perspective)
- Create a clear data dictionary from header metadata to support self-serve analysis and cross-dataset joins.
- Normalize field names and resolve inconsistencies (e.g., standardize Field_materials Ressources labels).
- Map units to a consistent scheme (DBH to cm, height to m) and identify any missing values indicators.
- Build dashboards and reports that summarize:
  - Species diversity by site and subplot
  - DBH and height distributions across radii classifications
  - Area-based metrics (plot areas) and their relation to species composition
  - Local vs. scientific names mapping and potential synonym issues
- Provide data quality checks and validation rules to ensure future data ingestions maintain schema consistency.
- Document data lineage and usage guidelines, including acknowledgment requirements for publications or products.