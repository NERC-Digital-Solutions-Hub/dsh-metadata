# Chamoli District, Uttarakhand, India – Post-event Reconnaissance Shapefiles for Bridges, Buildings, Roads, and Geomorphological Segments Following the 2021 Avalanche and Debris Flow Hazard Cascade

- What the data are
  - GIS shapefiles describing the location and condition of bridges, buildings, and roads in Chamoli District, Uttarakhand, India, after the 2021 Chamoli avalanche and debris flow hazard cascade.
  - Additional geomorphological segment shapefile outlining changes in river valleys between the avalanche source and Joshimath.

- Why the data were collected
  - To support the objectives of the NERC Urgency Grant NE/W002930/1, specifically post-event reconnaissance and identification of riparian infrastructure affected by the 2021 flood.

- Where the data were collected
  - Chamoli District, Uttarakhand, India.
  - Derived from manual interpretation of high-resolution satellite imagery.

- When the data were collected
  - Created between 29 June 2021 and 21 August 2021.
  - Supporting imagery for buildings and infrastructure mapped from 28 April 2019 to 10 February 2021.

- How the data were collected
  - Manual digitisation of GIS shapefiles (polygons and polylines) in ArcGIS Pro (v2.8).
  - Reference data from commercial satellite imagery (Maxar WorldView-3) under NASA grant terms; imagery data licensed for project use and not publicly shareable.
  - New Pléiades DEMs used to support geomorphological segment creation.
  - Data appear within this collection.

- Who was responsible
  - A Research Assistant created building and infrastructure footprints with guidance from the Principal Investigator (PI) and a Co-Investigator.
  - The geomorphological segments were created by the PI.

- Completeness of the dataset
  - Building and infrastructure mapping is the most comprehensive possible with available resources; minor omissions may exist.
  - Geomorphological outlines exclude areas of heavy shadow and corresponding DEM artifacts.

- Data structure and content (schema and attributes)
  - Shapefiles describe locations and attributes for:
    - Roads: Type (Major/Minor, paved/unpaved, Track) and Condition (Intact/Obstructed).
    - Bridges: Type (e.g., Intact for former bridges absence of type) and Condition (Intact/Damaged/Destroyed).
    - Buildings: Type (Residential permanent, Residential informal/temporary, Industrial/hydropower, Municipal) and Condition (Intact/Obstructed/damaged).
  - Geomorphological segments: ID (1–35) and Area (m²); other fields disregarded.
  - Coordinate system: WGS 84 / UTM Zone 44N (EPSG:32644).

- Quality control
  - Independent visual review by project Co-Investigators Westoby and Dunning.
  - Confirmed data accuracy and quality sufficient for disaster-response objectives.

- Dataset structure and files
  - 46 files in total, with primary shapefiles located in:
    - Bridges: 10Feb2021_bridge.shp; former_bridges.shp
    - Buildings: 10Feb2021_build.shp
    - Roads: 10Feb2021_road.shp; former_roads.shp
    - Geomorphological segments: Chamoli_geomorph_segments.shp
  - Each .shp file accompanied by corresponding .dbf, .prj, .shx, .sbn/.sbx/.cpg files as applicable.
  - A key.txt file provided to interpret attribute tables.

- Access and sharing considerations
  - Satellite imagery licensed terms prohibit public sharing of the underlying data.
  - Underlying datasets may require restricted access or project-specific sharing arrangements.

- Relevance to monitoring and policy decisions
  - Provides a structured, standards-based dataset for assessing post-disaster infrastructure exposure and damage, enabling monitoring of recovery and resilience planning.
  - Clear attribute schemas for asset type and condition support consistent reporting and trend analysis.
  - Metadata, dataset provenance, and governance considerations highlighted (data licensing, quality checks, and responsibility for data interpretation).
  - Identifies potential barriers to data sharing (licensing, metadata availability, and data transformations) that can inform future data governance and data stewardship within monitoring frameworks.