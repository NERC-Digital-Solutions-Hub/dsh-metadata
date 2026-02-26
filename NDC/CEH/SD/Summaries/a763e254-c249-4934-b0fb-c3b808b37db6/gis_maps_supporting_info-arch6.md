# Chamoli District, Uttarakhand, India - GIS shapefiles describing bridges, buildings, roads, and geomorphological segments after the Chamoli avalanche and debris flow (7 February 2021)

## What are these data?
- GIS shapefiles describing geospatial locations and conditions of bridges, buildings, and roads in Chamoli District, Uttarakhand, India, following the 2021 Chamoli avalanche and debris flow event.
- Includes a geomorphological segments shapefile for change analysis in river valleys between the avalanche source and the town of Joshimath.
- Attribute data covering type and condition for roads, bridges, and buildings; segment IDs and areas for geomorphological features.

## Why were the data collected?
- Created to support NERC Urgency Grant NE/W002930/1 objectives: post-event reconnaissance and identification of riparian infrastructure affected by the 2021 flood.

## Where were the data collected?
- Derived from manual interpretation of high-resolution satellite imagery for a portion of Chamoli District, using a defined geographic bounding box (WGS 84 / UTM Zone 44).

## When were the data collected?
- Building and infrastructure mapping created between 29 June 2021 and 21 August 2021.
- Underpinning satellite imagery for mapping acquired between 28 April 2019 and 10 February 2021.

## How were the data collected?
- Manual digitisation of GIS shapefiles (polygons and polylines) in ArcGIS Pro (v2.8) using existing satellite imagery as reference.
- Maxar WorldView-3 imagery used under a NASA High-Mountain Asia grant; Pléiades DEMs used for geomorphological segments.
- Data licensing restricts public sharing of Maxar-derived data; geomorphological data included in this collection.

## Who was responsible for the collection and interpretation of the data?
- A Research Assistant created building and infrastructure footprints, guided by the Principal Investigator and Co-Investigator.
- Geomorphological segments created by the Principal Investigator.

## Completeness and limitations
- Building and infrastructure mapping is the most comprehensive available within resource constraints; minor omissions may exist.
- Geomorphological segment outlines exclude heavily shadowed channel/valley floor areas and areas affected by satellite DEM artifacts.

## Experimental design and analytical methods
- Separate shapefiles for: bridges, buildings, roads, and geomorphological segments.
- Attributes:
  - Roads: Type (1 Major paved, 2 Major unpaved, 3 Minor paved, 4 Minor unpaved, 5 Track unpaved); Condition (1 Intact, 2 Obstructed/damaged).
  - Bridges: Type (0 Intact for former bridges shapefile; other types not present), Condition (1 Intact, 2 Damaged, 3 Destroyed).
  - Buildings: Type (1 Residential permanent, 2 Residential informal/temporary, 3 Industrial/hydropower, 4 Municipal); Condition (1 Intact, 2 Obstructed/damaged).
  - Geomorphological segments: ID (1–35) and area in square meters.
- Rationale: describe location and status of critical infrastructure affected by the event.

## Nature and units of recorded values
- Coordinate system: WGS 84 / UTM Zone 44N (EPSG:32644).
- Attribute values correspond to the schemas described for roads, bridges, buildings, and geomorphological segments (IDs and areas).

## Quality control
- Independent visual review by project Co-Investigators Westoby and Dunning, confirming data accuracy and suitability for disaster response objectives.

## Dataset structure
- Total of 46 files, each .shp accompanied by related files (.dbf, .cpg, .sbn, .sbx, .prj) and a key for attribute interpretation (key.txt).
- Primary shapefiles:
  - Bridges: 10Feb2021_bridge.shp, former_bridges.shp
  - Buildings: 10Feb2021_build.shp
  - Roads: 10Feb2021_road.shp, former_roads.shp
  - Geomorphological segments: Chamoli_geomorph_segments.shp
- Supporting files are available in their respective folders:
  - Bridges, Buildings, Roads, and geomorphological_segments directories
- Data provenance and attribute interpretation guidance provided in key.txt

## Data formats and licensing
- Data provided as standard ESRI Shapefiles with accompanying metadata files.
- Maxar WorldView-3 imagery licensing prohibits public sharing; data included in this collection reflect project-supported mapping.
- Pléiades DEMs used for geomorphological analysis; licensing implications noted.