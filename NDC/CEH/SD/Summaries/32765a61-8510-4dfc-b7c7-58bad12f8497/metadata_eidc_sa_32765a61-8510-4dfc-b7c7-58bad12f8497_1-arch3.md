# itogon_inventory_v11_wgs84utm51

## Overview
- GIS-based inventory of landslide polygons generated from high- to very high-resolution satellite imagery.
- Mapping performed by a single mapper through visual evidence of change before and after a typhoon.
- Purpose aligned with environmental monitoring and disaster risk assessment.

## Data Collection and Methods
- Measurements and mapping done entirely within a Geographic Information System (GIS).
- Imagery resolution used: 0.5 m to 10 m; time window for the imagery: February 2018 to March 2019.
- Date of analysis of the data: January–May 2020.
- Output consists of polygon features representing landslide sites, created by visual interpretation of satellite imagery.

## Data Structure and Contents
- Dataset comprises 1,101 polygons (each with a unique identifier FID).
- Main data stored in a shapefile set:
  - itogon_inventory_v11_wgs84utm51.shp (geometry and primary attributes)
  - itogon_inventory_v11_wgs84utm51.dbf (attribute data)
  - itogon_inventory_v11_wgs84utm51.cpg (UTF-8 encoding)
  - itogon_inventory_v11_wgs84utm51.prj (WGS 1984 UTM Zone 51N projection)
  - itogon_inventory_v11_wgs84utm51.shx (spatial index)
  - itogon_inventory_v11_wgs84utm51.xml (version history of geodatabase updates)
- Polygon areas range from 25 to 120,000 m².
- Attributes are stored in the .dbf component; the identifier used is FID.

## Data Quality and Provenance
- Independent quality check conducted after inventory creation.
- SOPs for techniques are not available (N/A).
- Data provenance includes explicit versioning (version 1.0) and an XML log of changes.

## Temporal and Spatial Scope
- Geographic scope concentrated on mapped landslides within the Itogon inventory.
- Temporal scope of imagery: Feb 2018–Mar 2019; analysis conducted in 2020.
- Spatial reference: WGS 84 / UTM Zone 51N.

## Implications for Monitoring Frameworks
- Provides a structured, GIS-ready dataset for monitoring landslide risk and environmental health implications post-typhoon.
- Demonstrates the use of high-resolution imagery to identify hazard features for policy scrutiny and decision-making.

## Data Governance, Access, and Use Considerations
- Data is organized with clear file formats and version history, aiding traceability.
- Encoding standardized to UTF-8, facilitating data sharing.
- Absence of documented SOPs may hinder reproducibility and consistency across teams.
- Independent QC supports trust in data quality, though lack of broad metadata formalization could limit interoperability without additional metadata augmentation.