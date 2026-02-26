# DATA HEADER INFORMATION for Delimitation_of_voronoi_polygon.csv

## Purpose and Context
- Metadata describing the target tree environment used for delimiting a Voronoï polygon in a belowground root survey.
- References: DOI, ESPA programme, Project P4GES.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Key Fields and Data Types
- ZOI (Zone of Interest)
  - Information: Zone of Interest
  - Variable Type: Categorical
  - Unit: ZOI2 (Andasibe) / ZOI3 (Anjahamana)
- Code
  - Information: Code for the target tree (site code + initial of local name + L/M/S)
  - Variable Type: Text String
  - Unit: (none)
- N° (Number of neighbouring trees)
  - Information: Number of neighboring trees per direction
  - Variable Type: Numeric
  - Unit: Unitless
- Neighbour tree name
  - Information: Name of the neighboring tree (northwards direction)
  - Variable Type: Text String
  - Unit: (none)
- Distance_from target_tree
  - Information: Distance between target tree and each neighbour tree
  - Variable Type: Numeric
  - Unit: Meter
- % (percentage)
  - Information: Importance of the size of the target tree relative to a neighbour
  - Calculation: % = (DBH_T + DBH_N) / DBH_T × 100
  - Variable Type: Numeric
  - Unit: Percentage
- Distance of the picket
  - Information: Distance between target tree and the picket location used for final delimitation
  - Variable Type: Numeric
  - Unit: Meter
- Height neighbour tree
  - Information: Total height of each neighbour tree (1.30 m DBH reference)
  - Variable Type: Numeric
  - Unit: Meter
- N° Picket 1
  - Information: Number of the first picket
  - Variable Type: Numeric
  - Unit: (none)
- N° Picket 2
  - Information: Number of the second picket
  - Variable Type: Numeric
  - Unit: (none)
- Distance between picket
  - Information: Distance between two neighbouring pickets
  - Variable Type: Numeric
  - Unit: Meter
- Height of each triangle
  - Information: Height of each triangle formed with the target and two pickets
  - Variable Type: Numeric
  - Unit: Meter
- Base of each triangle
  - Information: Base length of each triangle
  - Variable Type: Numeric
  - Unit: Meter
- Area of each triangle
  - Information: Area of each triangle
  - Variable Type: Numeric
  - Unit: m²

## Units and Measurements
- Distances: Meter
- Heights: Meter
- DBH-based categories referenced in code (L for large, M for medium, S for small)
- Area: square meters (m²)
- Percentage: percentage

## Data Provenance and Acknowledgments
- DOI: https://doi.org/10.5285/993c5778-e139-4171-a57f-7a0f396be4b8
- Programme: ESPA
- Project: P4GES
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data

## How Data Support Professionals Can Use This Data
- Understand the data structure to clean, verify, and integrate with other datasets describing tree environments and spatial delimitation.
- Create self-serve data products (dashboards, pivot tables, charts) to explore target trees, their neighbours, and Voronoi-based delimited areas.
- Compute derived metrics (e.g., triangle heights, bases, and areas) to support delimitation analyses and visualizations.
- Ensure consistent coding (Code field) and unit usage across analyses.
- Promote outputs, collect feedback, and iterate on data products; advocate for proper data creation and documentation.