# Parma2009_LandslideInventory_UTM_JJReviewed

## Overview
- Datasets map landslide polygons from a post-typhoon context.
- Polygons mapped by two people using visual evidence of change before and after the typhoon.
- Analysis timeframe: August–October 2020.
- Mapping relied on high- and very high-resolution satellite imagery (0.5 m to 10 m) covering Oct 2019–Mar 2020.
- Polygon areas range from 6 to 40,000 m².
- Inventory also integrated with GIS layers such as Digital Elevation Model and geology maps.

## Methods
- Identification method: visual observation of evidence of change to detect landslides.
- GIS-based execution: inventory polygons created and stored within GIS, leveraging DEM and geology layers.
- Quality control: inventory checked by two people after creation.
- Data sources for mapping: high/very high-resolution satellite imagery within a one-year window.

## Data Structure
- Primary dataset: Parma2009_LandslideInventory_UTM_JJReviewed.shp (main information: 2040 polygons with FID).
- Attribute data: Parma2009_LandslideInventory_UTM_JJReviewed.dbf (dBase format corresponding to the shapefile).
- Encoding: Parma2009_LandslideInventory_UTM_JJReviewed.cpg (UTF-8).
- Projection: Parma2009_LandslideInventory_UTM_JJReviewed.prj (WGS84 UTM Zone 51N).
- Additional metadata: Parma2009_LandslideInventory_UTM_JJReviewed.qpj (projection info) and Parma2009_LandslideInventory_UTM_JJReviewed.shx (polygon indexes).
- Versioning/changes: Parma2009_LandslideInventory_UTM_JJReviewed.xml contains updates or changes between geodatabases or external systems (version 1.0).

## Spatial and Temporal Coverage
- Spatial: landslide polygons mapped within the specified study area (UTM Zone 51N, WGS84).
- Temporal: imagery and inventory reflect Oct 2019–Mar 2020, with analysis conducted Aug–Oct 2020.
- Polygon characteristics: 2040 polygons with varying areas (6–40,000 m²).

## Data Quality and provenance
- Quality assurance: two-person verification of the inventory post-creation.
- Data lineage: integrated with GIS layers (DEM, geology) and external geodatabases; XML file tracks changes/updates.
- SOPs: no explicit Standard Operating Procedures provided in the metadata.

## Potential Analytical Uses
- Suitable for analyzing spatial distribution of landslides and correlations with terrain and geological factors when combined with other GIS layers.
- Supports development of predictive models or risk assessments using the inventory as a foundational dataset.
- Data can be converted or linked to standard GIS workflows given the shapefile format and UTF-8 encoding.

## Notes and Limitations
- Mapping relies on visual detection, which may introduce subjectivity.
- No explicit SOPs documented for the methods used.
- Data stored as shapefiles with accompanying metadata files; accessibility depends on GIS capabilities and proper handling of multiple associated files.