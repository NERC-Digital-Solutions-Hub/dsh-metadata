# DATA HEADER INFORMATION for Forest_inventory.csv

## Overview
- Describes characteristics of trees located on the Zone of Interest.
- Related to ESPA programme and P4GES project; DOI provided.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Provenance and referencing
- Programme: ESPA; Project: P4GES.
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Documentation note: Please also see Manual 1_Classical_Survey.

## Data schema and key fields
- Site_ID
  - Type: Text string
  - Description: P4GES site code; serves as the site identifier.
  - Unit: None specified.

- trees_subplot
  - Type: Categorical
  - Description: Subplot where the sample was collected, classified by radius.
  - Categories (implied): Small, Medium, Large
  - Radius guidance: 5 m < Small < 10 m, 10 m < Medium < 20 m, 20 m < Large
  - Unit: None specified.

- trees_area
  - Type: Numeric
  - Description: Surface area of the sampling plot (circular).
  - Unit: square meters (m²)

- trees_local_name
  - Type: Text string
  - Description: Vernacular/local name of the inventoried species.
  - Unit: None

- trees_scientific_names
  - Type: Text string
  - Description: Scientific name of the inventoried species.
  - Unit: None

- trees_genera
  - Type: Text string
  - Description: Genus of the selected tree.
  - Unit: None

- trees_family
  - Type: Text string
  - Description: Family of the selected tree.
  - Unit: None

- trees_DBH
  - Type: Numeric
  - Description: Breast height Diameter of the tree (diameter at 1.3 m from ground level).
  - Unit: Centimeters (cm)

- trees_height
  - Type: Numeric
  - Description: Total height of the tree (from ground to top).
  - Unit: Meters (m)

## Data collection metadata
- Field_materials Resources (as listed per field)
  - Site_ID: not explicitly linked to a field resource.
  - trees_subplot: not specified.
  - trees_area: coloured flags used in documentation.
  - trees_local_name: botanist
  - trees_scientific_names: botanist
  - trees_genera: botanist
  - trees_family: botanist
  - trees_DBH: forester compass
  - trees_height: vertex

## Data quality, standards, and notes
- The header provides explicit units for most quantitative fields (e.g., area in m², DBH in cm, height in m).
- Some unit fields are left unspecified in the header (e.g., Site_ID, certain resources), indicating potential metadata gaps.
- The documentation points to an accompanying manual (Manual 1_Classical_Survey) for broader context.
- Data provenance and naming conventions suggest careful taxonomic recording (local name, scientific name, genus, family).

## Access, reuse, and acknowledgments
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.
- Related project and program information (ESPA, P4GES) provides context for data origins and potential reuse constraints.