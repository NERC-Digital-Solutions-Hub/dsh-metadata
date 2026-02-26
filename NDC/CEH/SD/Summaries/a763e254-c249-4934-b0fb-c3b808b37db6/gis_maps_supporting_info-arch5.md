# Chamoli District Geospatial Dataset Post-Chamoli Event (Feb 2021)

## What are these data?
- GIS shapefiles containing geospatial information describing the location and condition of bridges, buildings, and roads in Chamoli District, Uttarakhand, India, following the 7 February 2021 avalanche and debris flow hazard cascade (Chamoli event).
- An accompanying geomorphological_segments shapefile supports analysis of change in river valleys between the avalanche source and the town of Joshimath.

## Why were the data collected?
- To support the objectives of NERC Urgency Grant NE/W002930/1, specifically post-event reconnaissance and identification of riparian infrastructure affected by the 2021 flood.

## Where were the data collected?
- Derived from manual interpretation of high-resolution satellite imagery over Chamoli District, with a defined bounding area in WGS 84 / UTM Zone 44N.

## When were the data collected?
- Dataset created between 29 June 2021 and 21 August 2021.
- Supporting imagery for buildings/infrastructure gathered between 28 April 2019 and 10 February 2021.

## How were the data collected?
- Manual digitisation of GIS shapefiles (polygons and polylines) in ArcGIS Pro 2.8, using reference satellite imagery.
- Maxar WorldView-3 imagery under NASA High-Mountain Asia Grant for mapping buildings/infrastructure (licensing prohibits public sharing).
- Pléiades DEMs used to support geomorphological segment creation.
- Data collection conducted under guidance of Principal Investigator and Co-Investigators.

## Who was responsible for the collection and interpretation?
- A Research Assistant created building and infrastructure footprints with guidance from the Principal Investigator and Co-Investigator.
- Geomorphological segments were created by the Principal Investigator.

## Completeness of the dataset
- Building and infrastructure mapping is the most comprehensive dataset produced with the available resources; minor omissions may exist.
- Geomorphological segments excluded areas of the channel/valley floor with heavy shadow or DEM artifacts.

## 2. Experimental design and analytical methods
- Shapefiles describe locations and attributes for roads, bridges, and buildings, plus geomorphological segments.
- Attribute schemas:
  - Roads: Type (1 Major paved, 2 Major unpaved, 3 Minor paved, 4 Minor unpaved, 5 Track unpaved); Condition (1 Intact, 2 Obstructed/damaged)
  - Bridges: Type (0 Intact bridge; note: former_bridges shapefile lacks this attribute); Condition (1 Intact, 2 Damaged, 3 Destroyed)
  - Buildings: Type (1 Residential permanent, 2 Residential informal/temporary, 3 Industrial/hydropower, 4 Municipal); Condition (1 Intact, 2 Obstructed/damaged)
  - Geomorphological segments: ID (1–35) and area (m²); other fields disregarded.

## 4. Nature and units of recorded values
- Coordinate system: WGS 84 / UTM Zone 44N (EPSG:32644).
- Attribute values follow the schema described above.

## 5. Quality control
- Independent visual review by Co-Investigators Westoby and Dunning.
- Confirmed data accuracy and quality sufficient for disaster-response objectives.

## 6. Dataset structure
- Total of 46 files, with primary shapefiles in their respective folders:
  - Bridges
    - 10Feb2021_bridge.shp
    - former_bridges.shp
  - Buildings
    - 10Feb2021_build.shp
  - Roads
    - 10Feb2021_road.shp
    - former_roads.shp
  - geomorphological_segments
    - Chamoli_geomorph_segments.shp
- Each shapefile has accompanying .dbf, .cpg, .sbn, .sbx, and .prj files.
- A key.txt provides interpretation guidance for attribute tables.