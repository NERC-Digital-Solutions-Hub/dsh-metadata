# Chamoli District, Uttarakhand, India - Post-event GIS shapefiles for bridges, buildings, roads and geomorphological segments

## Overview
- GIS shapefiles describing geospatial location and condition of bridges, buildings, and roads, plus geomorphological segments for change analysis in Chamoli District after the 2021 avalanche and debris flow (Chamoli event).
- Created to support post-event reconnaissance and identification of riparian infrastructure affected by the 2021 flood (NERC Urgency Grant NE/W002930/1).

## Data content and scope
- Shapefiles describe:
  - Bridges: footprints with type and condition attributes
  - Buildings: footprints with type and condition attributes
  - Roads: footprints with type and condition attributes
  - Geomorphological segments: segment IDs and area (m2) for river valley change analysis
- Completeness: described as the most comprehensive dataset achievable with available resources; minor omissions possible. In geomorphological mapping, areas in heavy shadow were excluded to avoid DEM artifacts.

## Spatial extent and coordinate reference
- Location: Chamoli District, Uttarakhand, India
- Bounding box (approximate): defined by the supplied coordinates in the WGS 84 / UTM Zone 44N system
- Coordinate system: WGS 84 / UTM Zone 44N (EPSG:32644)

## Data collection and processing methods
- Data source: manual digitisation of GIS shapefiles in ArcGIS Pro (v2.8) using high-resolution satellite imagery
- Imagery sources: Maxar WorldView-3 (for buildings and riparian infrastructure) under NASA High-Mountain Asia Grant; Pléiades DEMs used for geomorphological segments
- Imagery time span: reference imagery from 28 Apr 2019 to 10 Feb 2021
- Mapping window: 29 Jun 2021 to 21 Aug 2021
- Personnel: Research Assistant (footprints), guided by Principal Investigator (PI) and Co-Investigator; geomorphological segments created by PI

## Attribute schema (key for interpretation)
- Roads
  - Type: 1 Major (paved), 2 Major (unpaved), 3 Minor (paved), 4 Minor (unpaved), 5 Track (unpaved)
  - Condition: 1 Intact, 2 Obstructed/damaged
- Bridges
  - Type: 0 Intact bridge (only where present; some shapefiles omit this attribute)
  - Condition: 1 Intact, 2 Damaged, 3 Destroyed
- Buildings
  - Type: 1 Residential (permanent), 2 Residential (informal/temporary), 3 Industrial (e.g., hydropower), 4 Municipal
  - Condition: 1 Intact, 2 Obstructed/damaged
- Geomorphological segments
  - ID: 1–35
  - Area: value in square meters
  - Other fields: disregarded

## Quality control
- Independent visual review by project Co-Investigators Westoby and Dunning
- Confirmed data suitable to support disaster-response objectives

## Dataset structure and contents
- Total files: 46
- Primary shapefiles (with accompanying files): 
  - Bridges: 10Feb2021_bridge.shp, former_bridges.shp
  - Buildings: 10Feb2021_build.shp
  - Roads: 10Feb2021_road.shp, former_roads.shp
  - Geomorphological segments: Chamoli_geomorph_segments.shp
- Associated ancillary files: .dbf, .cpg, .prj, .sbn, .sbx for each shapefile
- Attribute interpretation key: key.txt

## Licensing and access
- Imagery/licensing: Maxar WorldView-3 data licensed; terms prohibit sharing these data in the public domain
- Usage: Suitable for GIS mapping and analysis within permitted license constraints and for disaster-response purposes

## How to use
- Integrate map-based layers to visualize riparian infrastructure and geomorphological changes post-event
- Use attribute schemas to filter by type and condition for targeted analyses (e.g., prioritizing damaged bridges or obstructed roads)
- Reference key.txt for consistent interpretation of attributes across shapefiles