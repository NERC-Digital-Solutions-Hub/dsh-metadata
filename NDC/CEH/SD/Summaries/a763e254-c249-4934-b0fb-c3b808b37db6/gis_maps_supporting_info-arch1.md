# Chamoli District, Uttarakhand, India — GIS shapefiles describing the location and condition of bridges, buildings and roads following the 7 February 2021 avalanche and debris flow hazard cascade (the Chamoli event)

## Overview
- GIS shapefiles describing the location and condition of riparian infrastructure (bridges, buildings, roads) and geomorphological segments related to the Chamoli avalanche/debris flow event.
- Supports post-event reconnaissance and identification of infrastructure affected by the 2021 flood.

## What data are
- Shapefiles for Bridges, Buildings, Roads and geomorphological_segments.
- Bridges: current and former bridges with attributes on type and condition.
- Buildings: various residential, industrial, municipal categories with condition.
- Roads: major/minor, paved/unpaved, and track classifications with condition.
- Geomorphological segments: IDs (1–35) with area in m²; used for river valley analysis.
- Accompanying metadata and a key file (key.txt) to interpret attributes.

## Why collected
- To support the objectives of NERC Urgency Grant NE/W002930/1.
- Specifically for post-event reconnaissance and identifying riparian infrastructure affected by the 2021 flood.

## Where and when
- Collected in Chamoli District, Uttarakhand, India.
- Bounding box approximate coordinates (WGS 84 / UTM Zone 44N): Top left 353406 m E, 3385683 m N; Lower right 381352 m E, 3371602 m N.
- Data created between 29 June 2021 and 21 August 2021.
- Underlying satellite imagery for mapping buildings/infrastructure spans 28 April 2019 – 10 February 2021.

## How collected
- Manual digitisation of GIS shapefiles (polygons and polylines) in ArcGIS Pro v2.8.
- Reference imagery from Maxar WorldView-3; data licensed under NASA High-Mountain Asia grant terms (not public domain).
- New Pléiades DEMs used to support geomorphological segment creation.
- Data interpreted with guidance from Principal Investigator and Co-Investigator; building/infrastructure footprints created by a Research Assistant.

## Responsibility
- Building and infrastructure footprints: created by a Research Assistant with PI/Co-I guidance.
- Geomorphological segments: created by the Principal Investigator.
- Data interpretation and validation conducted by project investigators.

## Completeness
- Building and infrastructure mapping considered the most comprehensive possible with available resources; minor omissions possible.
- Geomorphological segment outlines exclude heavily shadowed areas and DEM artifacts.

## Experimental design and methods
- Primary shapefiles: Bridges, Buildings, Roads, plus geomorphological_segments.
- Attributes:
  - Roads: Type (1 major paved, 2 major unpaved, 3 minor paved, 4 minor unpaved, 5 track unpaved); Condition (1 intact, 2 obstructed/damaged).
  - Bridges: Type (0 for intact in some shapefiles), Condition (1 intact, 2 damaged, 3 destroyed).
  - Buildings: Type (1 residential permanent, 2 residential informal/temporary, 3 industrial/hydropower, 4 municipal); Condition (1 intact, 2 obstructed/damaged).
  - Geomorphological segments: ID (1–35) and area (m²); other fields ignored.
- A key.txt provides interpretation guidance for attribute tables.

## Nature and units of recorded values
- Coordinate system: WGS 84 / UTM Zone 44N (EPSG:32644).
- Attribute values are as described in the data schema (Types and Conditions above) and segment areas in square meters.

## Quality control
- Independent visual review by Co-Investigators Westoby and Dunning.
- Confirmed data accuracy and suitability for disaster response objectives.

## Dataset structure
- Total of 46 files, with accompanying .dbf, .prj, .shx, .sbx, .sbn, and .cpg as applicable.
- Folders and primary shapefiles:
  - Bridges: 10Feb2021_bridge.shp; former_bridges.shp
  - Buildings: 10Feb2021_build.shp
  - Roads: 10Feb2021_road.shp; former_roads.shp
  - geomorphological_segments: Chamoli_geomorph_segments.shp
- A separate key.txt provides attribute interpretation.