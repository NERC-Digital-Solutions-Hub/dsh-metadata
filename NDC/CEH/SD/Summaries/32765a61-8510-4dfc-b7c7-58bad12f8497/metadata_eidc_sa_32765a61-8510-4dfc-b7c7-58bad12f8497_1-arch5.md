# itogon_inventory_v11_wgs84utm51

## Overview
- Landslide inventory dataset for Itogon area, produced by mapping polygons from satellite imagery.
- Mapping method: visual observation of evidences of change before and after a typhoon, conducted in GIS.
- Timeframe: polygons prepared from imagery covering Feb 2018 to Mar 2019; date of analysis: Jan–May 2020.
- Data product: a shapefile-based inventory with 1101 polygons (FID) and accompanying attribute data.
- Data lifecycle: versioned (XML file documents changes/updates between geodatabases and external systems); version indicated as 1.0.

## Data Content and Structure
- Main dataset: 1101 polygons (FID) stored in a shapefile set.
- Shapefile components:
  - itogon_inventory_v11_wgs84utm51.shp (geometry)
  - itogon_inventory_v11_wgs84utm51.dbf (attributes)
  - itogon_inventory_v11_wgs84utm51.cpg (UTF-8 encoding)
  - itogon_inventory_v11_wgs84utm51.prj (WGS 1984 / UTM Zone 51N projection)
  - itogon_inventory_v11_wgs84utm51.shx (shape index)
  - itogon_inventory_v11_wgs84utm51.xml (versioning/updates log)
- Data encoding: UTF-8
- Spatial reference: WGS 1984, UTM Zone 51N
- Attribute data: stored in the .dbf file
- Data characteristics: polygon areas range from 25 to 120,000 m²
- Quality control: inventory independently checked after creation

## Methods and Data Provenance
- Measurement and mapping processes conducted entirely within GIS.
- Imagery used: high to very high resolution (0.5 m to 10 m) satellite data.
- SOPs for techniques: not available (N/A).

## Quality Assurance
- Independent reviewer checked the inventory after construction.
- Documentation of changes/updates maintained in the accompanying XML file (version 1.0).

## Metadata, Standards, and Versioning
- Data structure and metadata reflect standard shapefile components, including explicit encoding (UTF-8) and projection details.
- Version history is captured in itogon_inventory_v11_wgs84utm51.xml (describes changes/updates among geodatabases and external systems).

## Access, Sharing, and Distribution Considerations
- Primary format is a shapefile with a support XML log for updates.
- Cataloging and dissemination should reference the XML changelog to track updates and interoperability with external systems.
- SOPs are not provided; governance should consider creating or updating SOPs for data collection, processing, and sharing to improve interoperability.

## Limitations and Considerations for Data Stewards
- Mapping was performed by a single person, which may affect completeness and consistency.
- Dependence on satellite imagery and manual delineation introduces potential bias and uncertainty.
- Temporal coverage is restricted to Feb 2018–Mar 2019; ongoing updates are logged in XML but require ongoing governance for timely refreshes.