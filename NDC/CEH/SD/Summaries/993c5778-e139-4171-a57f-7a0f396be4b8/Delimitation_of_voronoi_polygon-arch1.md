# DATA HEADER INFORMATION for Delimitation_of_voronoi_polygon.csv

## Overview
- Describes the target tree environment used for delimitation of Voronoï polygons.
- Related to ESPA programme and the P4GES project.
- DOI provided for data reference.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Spatial and Data Structure
- ZOI (Zone of Interest) information included; ZOI is treated as a categorical variable with units of ZOI² (Examples: Andasibe, Anjahamana).
- Code field encodes the target tree as: site code + initial of local name + size class (L = large DBH ≥ 20 cm, M = medium 10 ≤ DBH < 20 cm, S = small 5 ≤ DBH < 10 cm).
- N°, Neighbour tree name, Distance_from_target_tree, and related fields describe spatial relationships between the target tree and its neighbours.
- Distance of the picket defines how far from the target tree the pickets are placed, impacting final delimitation.
- Height, DBH-related measurements, and directional/positional data are included for each neighbour and for pickets.

## Variables and Measurements
- Neighbour tree name: textual identifier of each neighbouring tree, read from north and along a directional reference.
- Distance_from_target_tree: numeric distance (meters) from the target tree to each neighbour.
- % (Percentage): calculated importance of target tree size relative to a neighbouring tree using (% = (DBH_T + DBH_N) / DBH_T) × 100.
- Distance of the picket: distance (meters) from the target tree to the picket position.
- Height neighbour tree: total height of each neighbouring tree (measured at 1.30 m DBH reference).
- N° Picket 1 / N° Picket 2: identifiers for two pickets used in delimitation.
- Distance between picket: distance between the two neighbouring pickets (meters).
- Height of each triangle: height of the triangle formed by the target tree and two pickets.
- Base of each triangle: base length for each triangle (meters).
- Area of each triangle: area of each triangle (square meters).

## Delimitation Method
- Delimitation is based on constructing triangles formed by the target tree and two pickets.
- The calculated triangle dimensions (height, base, area) contribute to defining the Voronoï delimitation around the target tree.

## Provenance and Access
- DOI provided for citation and data access reference.
- Programme: ESPA; Project: P4GES; related project websites listed.
- Data products derived from these data require acknowledgment of the contributing laboratory/institution.

## Considerations for Analysts
- The dataset emphasizes local-scale environmental data with detailed tree-neighbour relationships, suitable for spatial delimitation analyses and predictive modeling.
- Potential challenges align with analysts’ typical needs: precise localisation (local scale), standardisation across sites, and integration of multiple spatial measurements (distances, heights, DBH classifications).
- Clear metadata (field definitions, units, and calculation formulas) supports data cleaning, reproducibility, and sharing via portals with metadata.