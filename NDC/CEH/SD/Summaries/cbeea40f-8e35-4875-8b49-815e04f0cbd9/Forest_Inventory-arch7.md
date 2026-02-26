# DATA HEADER INFORMATION for Forest_inventory.csv

## Overview
- This dataset describes the characteristics of trees located on the Zone of Interest.
- Part of the ESPA Programme with the P4GES project; includes DOI and project websites.
- Acknowledgement to Laboratoire des Radio Isotopes, Université d'Antananarivo is required for products derived from these data.

## Data schema and attributes
- Site_ID
  - Information: P4GES site code
  - Variable type: Text String
  - Unit: .
- trees_subplot
  - Information: Subplot where the sample has been collected
  - Variable type: Categorical
  - Unit: L (Large) / M (Medium) / S (Small)
  - Notes: Classified by radius; 5m < Small < 10m, 10m < Medium < 20m radius
- trees_area
  - Information: Surface of the sampling area (circular plot)
  - Variable type: Numeric
  - Unit: square meters (m²)
- trees_local_name
  - Information: Vernacular/local name of the inventoried species
  - Variable type: Text String
  - Unit: .
- trees_scientific_names
  - Information: Scientific name of the inventoried species
  - Variable type: Text String
  - Unit: .
- trees_genera
  - Information: Genera of the selected tree
  - Variable type: Text String
  - Unit: .
- trees_family
  - Information: Family of the selected tree
  - Variable type: Text String
  - Unit: .
- trees_DBH
  - Information: Breast height Diameter of the tree (diameter at 1.3m from ground level)
  - Variable type: Numeric
  - Unit: Centimeter
- trees_height
  - Information: Total height of the tree (from ground to top of tree)
  - Variable type: Numeric
  - Unit: Meter
- Field_materials Ressources
  - Notes: Indicates data provenance for each field (e.g., botanist)

## Data quality and standards
- The header includes explicit units for most quantitative fields (DBH in cm, height in m, area in m²) and categorical classifications for subplot radii.
- Some fields list missing or unspecified units (e.g., Site_ID with Unit = .), which should be harmonized during ingestion.
- Taxonomic fields cover local names, scientific names, genera, and families to support cross-referencing and mapping in GIS.

## Spatial relevance and use
- The dataset provides plot-level and taxonomic attributes suitable for GIS mapping and analysis.
- Can be linked to spatial layers via Site_ID and subplot category (trees_subplot) to visualize species distribution, tree sizes (DBH, height), and plot areas (trees_area) across the Zone of Interest.
- Useful for biomass estimation, species richness analyses, and spatial planning related to forest inventories.

## Provenance, usage constraints, and references
- Data originate from the ESPA Programme, Project P4GES.
- DOI provided: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement requirement for products derived from these data to Laboratoire des Radio Isotopes, Université d'Antananarivo.
- Related resources: ESPA (http://www.espa.ac.uk/), P4GES (https://www.p4ges.org)