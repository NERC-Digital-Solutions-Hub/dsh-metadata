# Tree canopy data derived from LiDAR data for South West England 2013

## Overview
- A high-resolution LiDAR-derived dataset describing tree canopies in South West England (2013), produced for the Tellus South West project.
- Outputs include Digital Terrain Model (DTM), Digital Surface Model (DSM), treetop detections, and crown outlines; intended for monitoring forest structure, hedgerows, and rural/urban green features.
- Provided as geospatial layers and accompanying attributes, suitable for informing environmental health monitoring and policy evaluation.

## Access and licensing
- Data available at: https://doi.org/10.5283/78dba959-989b-43d4-b4da-efd2506e0c8e
- Licensing: Open Government Licence (title referenced in dataset); usage requires acknowledgement/citation of: Scholefield, P; Trembath, P. (2022). Tree canopy data derived from LiDAR data for South West England 2013. NERC EDS Environmental Information Data Centre.
- Citation: Scholefield & Trembath (2022) dataset DOI: 10.5283/78dba959-989b-43d4-b4da-efd2506e0c8e

## Collection/generation methods
- Data source and creation:
  - British Antarctic Survey (BAS) collected a new high-resolution LiDAR survey over Cornwall and Devon in July–August 2013 for the Tellus South West project.
  - Raw LiDAR data converted to Digital Terrain Model (DTM) and Digital Surface Model (DSM) by Environment Agency (contract).
- Technical specifics:
  - 2 cm height layers for DSM and DTM at 1 m grid resolution; average height accuracy ~25 cm.
  - Coverage: 9,424 km2 west of Exmouth (approximately west of 3°21′W).
  - Files provided as segments corresponding to OS grid tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).
- Outputs and formats:
  - DTM (bare-earth height) and DSM (features on bare earth) generated and available as raster formats.
  - Outputs from delineation model include tree crown polygons and treetop points, stored as 25 km2 geopackages.
- Data processing steps:
  - Forest Tools R package used with DSM and DTM to detect dominant treetops via a variable window filter (dynamic window size based on canopy height).
  - Canopy segmentation using the mcws function (watershed algorithm from the imager package) to outline crowns; marker-controlled segmentation used to reduce oversegmentation.
  - Post-processing includes rural feature filtering using a nonhedgerow layer derived from multiple sources (National Forest Inventory, Greenspace/Urban Areas, Landcover Map 2007 Littoral layers).

## Spatial reference and coverage
- Coordinate system: OSGB 1936/British National Grid (EPSG:27700).
- Spatial extent: 9,424 km2 area west of Exmouth (roughly west of 3°21′W).

## Data products and generation workflow
- Outputs:
  - Tree crown polygon layer (crown outlines).
  - Tree top point layer.
  - Both saved as 25 km2 geopackages.
- Derived layers:
  - Nonhedgerow layer used to filter rural features from urban/shoreline features for more accurate canopy representation.
- Data structure and attributes:
  - Core fields include:
    - treeID: unique identifier at 1 km scale (not unique for 25 km2 tiles).
    - Height: crown height in metres.
    - crownAr: crown area in square metres (integer due to LiDAR resolution).
    - crwnDmt: mean crown diameter from tree top (metres).
    - habitat: categorisation (buildings/coastal, forest/woodland/urban greenspace, rural/agricultural).
    - Geometry: type (points for treetops, polygons for crown areas).

## Quality, limitations, and data governance
- Quality characteristics:
  - LiDAR data: 2 cm height layers, 1 m grid, ~25 cm vertical accuracy.
  - Outputs provided “as is” after delineation; rural feature filtering applied; buildings and forests retained to support downstream analyses.
- Processing considerations and limitations:
  - Crown outlines produced as polygons require substantial processing time and disk space.
  - Oversegmentation risk mitigated by marker-controlled segmentation, but potential for sub-crown segmentation remains a consideration.
  - Transformation/formatting steps may require additional metadata and careful data management for reuse.
- Data governance and usability notes:
  - Open data licensing enables reuse, but users must acknowledge dataset provenance and provide appropriate citations.
  - Metadata completeness and data provenance documentation are important for ensuring datasets meet monitoring and data governance standards.