# DATA HEADER INFORMATION for Delimitation_of_voronoi_polygon.csv

## Context and Purpose
- Presents the target tree environment for delimiting a Voronoi polygon around trees.
- Part of ESPA Programme, Project P4GES.
- DOI provided for the dataset.
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.
- Metadata defines Zone of Interest (ZOI) and various attributes used in delimiting polygons around trees.

## Key Fields and Metadata

- ZOI, Information = Zone of Interest; ZOI, Variable Type = Categorical; ZOI, Unit = ZOI2: Andasibe / ZOI3: Anjahamana.
- Code, Information = Code given to the target tree; Code, Variable Type = Text String; Code, Unit = . 
  - Code composition: site code + initial character of local name of target tree + L (large DBH ≥20 cm), M (medium 10–20 cm), S (small 5–10 cm).
- N°, Information = Number of neighbouring trees according to the direction of a hand of a watch; N°, Variable Type = Numeric; N°, Unit = Unitless.
- Neighbour tree name, Information = Name of neighbouring tree of target tree; Neighbour tree name, Variable Type = Text String.
- Distance_from target_tree, Information = Distance between target tree and each neighbour tree; Distance_from target_tree, Variable Type = Numeric; Distance_from target_tree, Unit = Meter.
- %, Information = Importance of the size of the target tree considering the neighbouring tree; % = (DBH_T + DBH_N) / (DBH_T) * 100; %, Variable Type = Numeric; % , Unit = Percentage.
- Distance of the picket, Information = Distance between target tree and location of picket; Distance of the picket, Variable Type = Numeric; Distance of the picket, Unit = Meter.
- Height neighbour tree, Information = Height total of each neighbour tree; Height neighbour tree, Variable Type = Numeric; Height neighbour tree, Unit = Meter.
- N° Picket 1, Information = Number/identifier of the first picket; N° Picket 1, Variable Type = Numeric.
- N° Picket 2, Information = Number/identifier of the second picket; N° Picket 2, Variable Type = Numeric.
- Distance between picket, Information = Distance between two neighbouring pickets; Distance between picket, Variable Type = Numeric; Distance between picket, Unit = Meter.
- Height of each triangle, Information = Height of each triangle formed with the target and two neighbouring pickets; Height of each triangle, Variable Type = Numeric; Height of each triangle, Unit = Meter.
- Base of each triangle, Information = Base length of each triangle; Base of each triangle, Variable Type = Numeric; Base of each triangle, Unit = Meter.
- Area of each triangle, Information = Area of each triangle; Area of each triangle, Variable Type = Numeric; Area of each triangle, Unit = m².

## Data Provenance and Standards
- Dataset linked to an explicit project framework (ESPA, P4GES) and a DOI for traceability.
- Field definitions include explicit units, data types, and the method of deriving certain values (e.g., the percentage calculation for tree size relative to neighbours).

## Analytical Use and Delimitation Method
- Target tree forms a triangle with two neighboring pickets; the height, base, and area of each triangle are computed to support delimitation of the Voronoi polygon around the target tree.
- Distances, heights, and DBH-based calculations (e.g., the % formula) inform the spatial delimitation and characterization of the tree’s environment.

## Governance, Sharing, and Acknowledgement
- Data use requires acknowledgement of the contributing laboratory and institutions.
- Clear guidance on metadata and data unit consistency is provided to support reproducibility and data integration in monitoring frameworks.

## Relevance for Monitoring Frameworks
- Provides a structured, metadata-rich approach to capturing spatial relationships around trees for environmental monitoring.
- Demonstrates explicit data governance, provenance, and standardized fields essential for evaluating and comparing environmental health measures across policies and sites.
- Addresses common monitoring challenges: clear variable definitions, data provenance, and explicit sharing and acknowledgement requirements.