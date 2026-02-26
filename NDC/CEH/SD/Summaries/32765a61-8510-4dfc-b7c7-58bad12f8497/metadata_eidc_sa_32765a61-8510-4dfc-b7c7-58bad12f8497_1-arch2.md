# itogon_inventory_v11_wgs84utm51

## Overview
- Landslide inventory dataset for Itogon area, created from satellite imagery and GIS analysis.
- Polygons represent landslide extents identified through visual evidence of change before and after a typhoon.
- Prepared to support environmental monitoring and policy performance assessment over time.

## Methods and Data Collection
- Mapping conducted by a single mapper using high- to very-high-resolution satellite imagery (0.5 m to 10 m).
- Visual observation of evidences of change to delineate landslide polygons corresponding to post-typhoon changes.
- Measurements and GIS-based analyses completed within a GIS environment.
- Temporal scope of imagery: Feb 2018 to Mar 2019; date of analysis: Jan–May 2020.
- Quality control: independent verification performed after initial mapping.

## Data Content and Structure
- Primary data format: shapefile set describing the inventory.
- Files included:
  - itogon_inventory_v11_wgs84utm51.shp — main polygon data (1101 polygons; FID IDs)
  - itogon_inventory_v11_wgs84utm51.dbf — attribute data (dBase format)
  - itogon_inventory_v11_wgs84utm51.cpg — UTF-8 encoding
  - itogon_inventory_v11_wgs84utm51.prj — projection: WGS 1984 UTM Zone 51N
  - itogon_inventory_v11_wgs84utm51.shx — shape index
  - itogon_inventory_v11_wgs84utm51.xml — changes/updates (version 1.0)
- Polygon characteristics: areas range from 25 to 120,000 m²; polygons derived from very high-resolution imagery within a 1-year window.

## Spatial and Temporal Scope
- Geographic: Itogon area (polygons mapped in GIS, using UTM Zone 51N coordinates, WGS 1984).
- Temporal: imagery from Feb 2018–Mar 2019; analysis conducted Jan–May 2020.
- Dataset version: 1.0.

## Quality Assurance
- Independent reviewer validated the inventory after initial mapping.
- No standard operating procedures (SOPs) documented in metadata.

## Use and Access Considerations
- Data stored as a shapefile bundle with accompanying metadata and a version log (XML).
- Designed for integration with other datasets to enhance usefulness beyond single-use applications and to support broader environmental monitoring initiatives.

## Limitations and Considerations for Analysts
- Mapping performed by a single individual, which may introduce subjectivity or consistency considerations.
- SOPs for methods are not provided in the metadata; users may need to assess reproducibility.
- Access to underlying data and interoperability with other datasets should consider the explicit data formats and projection used.