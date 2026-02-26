# Parma2009_LandslideInventory_UTM_JJReviewed

## Overview
- Landslide polygons mapped by two people using visual evidence of change before/after Typhoon events.
- Mapping performed in a Geographic Information System (GIS) leveraging inventory layers and other GIS inputs.

## Data collection and methods
- Physical measurements/observations conducted within GIS using digital layers (e.g., Digital Elevation Model, Geology map).
- Satellite imagery at high/very high resolution used for polygon delineation (0.5 m to 10 m spatial resolution).
- Time window for imagery and inventory: October 2019 to March 2020.
- Polygon areas range from 6 to 40,000 m².
- Measurements and inventory rely on standard GIS workflows and multiple data layers.

## Data structure and contents
- One shapefile dataset comprising:
  - Parma2009_LandslideInventory_UTM_JJReviewed.shp: 2040 polygons with FID identifiers.
  - Parma2009_LandslideInventory_UTM_JJReviewed.dbf: attribute data for polygons (dBase format).
  - Parma2009_LandslideInventory_UTM_JJReviewed.cpg: encoding set to UTF-8.
  - Parma2009_LandslideInventory_UTM_JJReviewed.prj: projection WGS 1984 UTM Zone 51N.
  - Parma2009_LandslideInventory_UTM_JJReviewed.qpj: additional projection information.
  - Parma2009_LandslideInventory_UTM_JJReviewed.shx: polygon index file.
  - Parma2009_LandslideInventory_UTM_JJReviewed.xml: records changes/updates between geodatabases and external systems (version 1.0).

## Quality control and provenance
- Inventory checked by two people after creation.

## Analysis timeline
- Date of analysis: August–October 2020.

## Metadata, standards, and storage
- Data encoded in UTF-8 (cpg).
- Projection: WGS 1984 UTM Zone 51N (prj).
- Data version: 1.0; updates/changes tracked in accompanying XML.

## Use, sharing, and governance considerations
- Dataset designed for discoverability and reuse within GIS environments.
- Contains explicit versioning and change-tracking via XML.
- No explicit Standard Operating Procedures (SOPs) provided in this metadata; future stewardship may require documentation of methods to support interoperability and reproducibility.

## Limitations and considerations for Data Stewards
- Methods rely on visual interpretation and may be sensitive to subjectivity.
- No SOPs available for techniques; consider developing and publishing to improve reproducibility.
- Metadata notes cover data availability and update mechanics through the XML changelog; ensure ongoing synchronization with external systems and geodatabases.