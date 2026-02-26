# Chamoli District, Uttarakhand, India GIS shapefiles: bridges, buildings, roads and geomorphological segments after the 2021 avalanche and debris flow

- What are these data
  - GIS shapefiles mapping riparian infrastructure (bridges, buildings, roads) and geomorphological segments in Chamoli District, Uttarakhand, India.
  - Focus on the 7 February 2021 avalanche and debris flow hazard cascade (Chamoli event); includes polygon outlines for geomorphological change along river valleys between the avalanche source and Joshimath.

- Purpose
  - Support post-event reconnaissance and identify infrastructure affected by the 2021 flood under NERC Urgency Grant NE/W002930/1.

- Location and extent
  - Derived from manual interpretation of high-resolution satellite imagery over Chamoli District.
  - Geographic bounding area described in WGS84 / UTM Zone 44N coordinates (top left 353406 E, 3385683 N; bottom right 381352 E, 3371602 N).

- Timeframe
  - Data creation: 29 June 2021 – 21 August 2021.
  - Supporting imagery for mapping: 28 April 2019 – 10 February 2021.

- Methods
  - Manual digitisation of shapefiles (polygons and polylines) in ArcGIS Pro 2.8, using satellite imagery as reference.
  - Maxar WorldView-3 imagery used under NASA grant; licensing prohibits public sharing.
  - Pléiades DEMs used to support geomorphological segment creation.

- People and roles
  - Research Assistant digitised building and infrastructure footprints under guidance from Principal Investigator (PI) and Co-Investigator.
  - Geomorphological segments created by PI.

- Completeness and limitations
  - Building/infrastructure mapping is the most comprehensive feasible with available resources; minor omissions possible.
  - Geomorphological segments exclude heavily shadowed channel/valley floor areas and areas affected by DEM artifacts.

- Data structure and schema
  - Coordinate system: WGS 84 / UTM Zone 44N (EPSG:32644).
  - Attributes by feature type:
    - Roads: Type (1 Major paved, 2 Major unpaved, 3 Minor paved, 4 Minor unpaved, 5 Track unpaved); Condition (1 Intact, 2 Obstructed/damaged).
    - Bridges: Type (0 Intact only for ‘former bridges’ shapefile); Condition (1 Intact, 2 Damaged, 3 Destroyed).
    - Buildings: Type (1 Residential permanent, 2 Residential informal/temporary, 3 Industrial/hydropower, 4 Municipal); Condition (1 Intact, 2 Obstructed/damaged).
    - Geomorphological segments: ID (1–35) and area in m²; other fields ignored.

- Dataset structure
  - Total of 46 files; each shapefile (.shp) has accompanying .dbf, .cpg, .sbn, .sbx, .prj; a key.txt file explains attribute tables.
  - Primary shapefiles:
    - Bridges: 10Feb2021_bridge.shp, former_bridges.shp
    - Buildings: 10Feb2021_build.shp
    - Roads: 10Feb2021_road.shp, former_roads.shp
    - Geomorphological segments: Chamoli_geomorph_segments.shp

- Quality control
  - Independent visual review by project Co-Investigators Westoby and Dunning; data deemed sufficient for disaster response objectives.

- Licensing and access
  - Maxar imagery licensed; data cannot be shared in the public domain due to licensing terms.

- Relevance for data leaders
  - Illustrates end-to-end data lifecycle for post-disaster data products: collection, schema design, QA, and dissemination constraints.
  - Highlights practical challenges: access barriers, licensing, data gaps, and need for clear metadata and coverage.
  - Supports decision-making for recovery planning, risk assessment, and inter-organisational coordination through shared infrastructure data.