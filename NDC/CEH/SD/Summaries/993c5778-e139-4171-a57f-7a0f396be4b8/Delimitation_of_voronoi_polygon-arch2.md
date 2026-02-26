# DATA HEADER INFORMATION for Delimitation_of_voronoi_polygon.csv

## Overview
- Describes the target tree environment and the data structure used to delimit Voronoi polygons around each target tree.
- Associated with ESPA (Project P4GES); DOI provided; acknowledgement required for products derived from these data.
- Zone of Interest (ZOI) and a set of fields capture spatial relationships between a target tree and its neighbours, enabling standardized environmental monitoring and spatial analysis.
- Data are organized to support storage and upload to appropriate data portals, with standardized units and field definitions.

## Key fields and definitions
- ZOI, Information: Zone of Interest; Type: Categorical; Examples: ZOI2 (Andasibe), ZOI3 (Anjahamana).
- Code, Information: Unique code for the target tree composed of site code + initial of local name + size category (L = large DBH ≥ 20 cm, M = medium 10–<20 cm, S = small 5–<10 cm). Type: Text String.
- N°, Information: Number of neighbouring trees according to the direction of a hand of a watch.
- Neighbour tree name, Information: Name of the neighbouring tree, positioned northward and in the indicated direction.
- Distance_from target_tree, Information: Distance from the target tree to each neighbour tree. Type: Numeric; Unit: Meter.
- %, Information: Relative size importance of the target tree with respect to a neighbour, calculated as % = (DBH_T + DBH_N) / DBH_T × 100. Type: Numeric; Unit: Percentage.
- Distance of the picket, Information: Distance between the target tree and the picket location used for delimitation. Type: Numeric; Unit: Meter.
- Height neighbour tree, Information: Total height of each neighbour tree (1.30 m DBH reference). Type: Numeric; Unit: Meter.
- N° Picket 1, Information: Number/identifier of the first picket. Type: Numeric.
- N° Picket 2, Information: Number/identifier of the second picket. Type: Numeric.
- Distance between picket, Information: Distance between the two neighbouring pickets. Type: Numeric; Unit: Meter.
- Height of each triangle, Information: Height of the triangle formed by the target tree and two neighbour pickets. Type: Numeric; Unit: Meter.
- Base of each triangle, Information: Base length of each triangle. Type: Numeric; Unit: Meter.
- Area of each triangle, Information: Area of each triangle. Type: Numeric; Unit: m².

## How it supports environmental monitoring
- Standardizes spatial delimitation using Voronoi-based polygons around target trees.
- Captures relationships to neighbouring trees and measurement points (pickets) to enable consistent, repeatable delimitation.
- Produces data suitable for maps, charts, and other outputs used to assess environmental structure and competition around trees.

## Data provenance and usage constraints
- Source programme/project: ESPA; Project: P4GES.
- DOI provided for dataset access and traceability.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).
- Data intended to be stored and uploaded to designated data portals with standardized field definitions and units.

## Relevance to monitoring goals and analysis
- Fits the Analysts Monitoring the Environment archetype by providing a consistent, quality-assured dataset to evaluate spatial relationships around target trees over time.
- Enables broad analytical outputs (e.g., comparisons across ZOIs, time-series of neighbourhood structure) using a standard format.
- Supports data integration by clearly defined fields and units, facilitating reuse and cross-site analysis.

## Challenges and opportunities for analysts
- Increase the value of the dataset by integrating with additional environmental layers (e.g., habitat, soil, microclimate) to enable broader insights.
- Improve data accessibility by ensuring underlying data are available to users beyond final outputs, enhancing transparency and reuse.