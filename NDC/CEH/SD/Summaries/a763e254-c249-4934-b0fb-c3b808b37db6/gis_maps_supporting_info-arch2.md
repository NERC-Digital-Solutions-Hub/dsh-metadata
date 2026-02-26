# Chamoli District, Uttarakhand, India post-event reconnaissance GIS data following the Chamoli event

- GIS shapefiles describing location and condition of riparian infrastructure (bridges, buildings, roads) and geomorphological segments to support post-event analysis after the 7 February 2021 Chamoli avalanche and debris flow event.
- Includes polygon outlines for geomorphological analysis of river valley change between the avalanche source and Joshimath.

## What are these data?
- Shapefiles for:
  - Bridges (footprints and status)
  - Buildings (footprints and status)
  - Roads (current and former)
  - Geomorphological segments (ID and area)
- Attribute schemas:
  - Roads: Type (1–5) and Condition (1–2)
  - Bridges: Type (0 for intact; otherwise not all bridges have this attribute) and Condition (1–3)
  - Buildings: Type (1–4) and Condition (1–2)
  - Geomorphological segments: ID (1–35) and area (m²)

## Why were the data collected?
- To support the objectives of NERC Urgency Grant NE/W002930/1 via post-event reconnaissance.
- Aimed at identifying riparian infrastructure directly or indirectly affected by the 2021 flood.

## Where were the data collected?
- Derived from manual interpretation of high-resolution satellite imagery of Chamoli District, Uttarakhand, India.
- Spatial extent approximated by bounding box in WGS 84 / UTM Zone 44N (EPSG:32644).

## When were the data collected?
- Data collection: 29 June 2021 – 21 August 2021.
- Supporting imagery for mapping: 28 April 2019 – 10 February 2021.

## How were the data collected?
- Manual digitisation of GIS shapefiles (polygons and polylines) in ArcGIS Pro 2.8.
- Reference imagery from Maxar WorldView-3 under NASA High-Mountain Asia Grant; licensing prohibits public sharing.
- Pléiades DEMs used to support geomorphological segment creation.
- Data collection and interpretation led by a Research Assistant with guidance from the Principal Investigator and Co-Investigator; geomorphological segments created by the Principal Investigator.

## Who was responsible for the collection and interpretation of the data?
- Data collection: Research Assistant (with oversight from PI and Co-I).
- Data interpretation: Principal Investigator and Co-Investigator.
- Geomorphological segments: Principal Investigator.

## Completeness of the dataset
- Building and infrastructure mapping is the most comprehensive dataset of riparian infrastructure produced with available resources.
- May contain minor omissions.
- Geomorphological segments exclude areas of heavy shadow and DEM artifacts.

## Experimental design and analytical methods
- Focused on creating separate shapefiles for:
  - Bridges
  - Buildings
  - Roads
  - Geomorphological segments
- Attribute schemas defined as above for each feature class.
- Geomorphological segments include an ID (1–35) and an area in m²; additional fields are not used.

## Collection / generation / transformation methods
- Data generation methods described above (manual digitisation using satellite imagery as reference).

## Nature and units of recorded values
- Coordinate system: WGS 84 / UTM Zone 44N (EPSG:32644).
- Attribute values described in the respective schemas (section 2).

## Quality control
- Independent visual review by project Co-Investigators Westoby and Dunning.
- Confirmed data accuracy and quality sufficient for disaster-response objectives.

## Dataset structure
- Total files: 46
- Primary shapefiles (with accompanying files):
  - Bridges folder:
    - 10Feb2021_bridge.shp
    - former_bridges.shp
  - Buildings folder:
    - 10Feb2021_build.shp
  - Roads folder:
    - 10Feb2021_road.shp
    - former_roads.shp
  - Geomorphological segments:
    - Chamoli_geomorph_segments.shp
- Each shapefile pair includes: .shp, .dbf, .cpg, .sbn, .sbx, .prj
- A key for interpreting attribute tables is provided as key.txt.