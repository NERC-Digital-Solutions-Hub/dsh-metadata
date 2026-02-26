# DATA HEADER INFORMATION for Forest_inventory.csv

## Overview
- Describes the characteristics of trees located on the Zone of Interest within Forest_inventory.csv.
- Associated with ESPA programme and P4GES project; includes a DOI reference.
- Acknowledgement is required for products derived from these data to Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Dataset context
- Serves as a structured data header defining the variables, data types, units, and provenance for forest inventories.
- Aims to support consistent monitoring of forest structure and composition across time.

## Core variables and data types
- Site_ID
  - Type: Text string
  - Information: P4GES site code
  - Unit: none
  - Field_materials_resources: .
- trees_subplot
  - Type: Categorical
  - Information: Subplot where the sample was collected; classified by radius: 5m < Small < 10m, 10m < medium < 20m
  - Unit: L (Large) / M (Medium) / S (Small)
  - Field_materials_resources: .
- trees_area
  - Type: Numeric
  - Information: Surface of the sampling area (circular plot)
  - Unit: square meters (m²)
  - Field_materials_resources: coloured flags
- trees_local_name
  - Type: Text
  - Information: Vernacular/local name of the inventoried species
  - Unit: none
  - Field_materials_resources: botanist
- trees_scientific_names
  - Type: Text
  - Information: Scientific name of the inventoried species
  - Unit: none
  - Field_materials_resources: botanist
- trees_genera
  - Type: Text
  - Information: Genus of the selected tree
  - Unit: none
  - Field_materials_resources: botanist
- trees_family
  - Type: Text
  - Information: Family of the selected tree
  - Unit: none
  - Field_materials_resources: botanist
- trees_DBH
  - Type: Numeric
  - Information: Breast height diameter of the tree (diameter at 1.3 m)
  - Unit: centimeters (cm)
  - Field_materials_resources: forester compass
- trees_height
  - Type: Numeric
  - Information: Total height of the tree (from ground to top)
  - Unit: meters (m)
  - Field_materials_resources: vertex

## Taxonomy and measurement details
- Taxonomic fields include local name, scientific name, genus, and family, all supported by botanist field resources.
- Physical measurements include DBH (cm) and total height (m), collected using specified field tools (e.g., forester compass for DBH, vertex for height).

## Data provenance and acknowledgments
- Data provenance links to ESPA and P4GES projects; DOI provided.
- Explicit acknowledgment required for products derived from these data to Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Data quality and reuse considerations
- Variables are defined with explicit data types, units, and descriptive information to enable consistent analysis.
- Field_materials_resources metadata indicate the tools or specialists involved in each measurement, supporting traceability.