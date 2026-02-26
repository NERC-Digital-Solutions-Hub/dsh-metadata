# itogon_inventory_v11_wgs84utm51.shp

## Overview
- Landslide polygons mapped from satellite imagery to identify evidences of change before and after a Typhoon.
- Measurements and analysis conducted in a Geographic Information System (GIS).
- Date of analysis: January–May 2020.

## Data Collection and Sampling Locations
- Mapping performed by a single person using high- to very high-resolution satellite imagery (0.5 m to 10 m).
- Time window for imagery: February 2018 to March 2019.
- Polygons represent landslide inventory across the study area.

## Measurements and Data Collection
- All measurements: GIS-based; no physical samples collected (N/A for sample storage/treatment).
- Quality control: inventory independently checked after initial mapping.

## Data Structure and Contents
- Data format: shapefile collection with main files:
  - itogon_inventory_v11_wgs84utm51.shp (main polygon data; 1101 polygons; FID)
  - itogon_inventory_v11_wgs84utm51.dbf (attribute data)
  - itogon_inventory_v11_wgs84utm51.cpg (UTF-8 encoding)
  - itogon_inventory_v11_wgs84utm51.prj (WGS 1984 / UTM Zone 51N projection)
  - itogon_inventory_v11_wgs84utm51.shx (spatial indexes)
  - itogon_inventory_v11_wgs84utm51.xml (change/update history; version 1.0)
- Polygon areas range from 25 to 120,000 m².

## Quality Control
- Independent verification of the inventory conducted after initial mapping.

## Temporal and Spatial Scope
- Spatial: landslide polygons mapped within a defined study area (UTM Zone 51N; WGS84).
- Temporal: imagery from Feb 2018–Mar 2019; analysis performed Jan–May 2020.

## Versioning and Access
- Version: 1.0.
- Data stored as a shapefile set with standard GIS formats and UTF-8 encoding to support broad accessibility and reproducibility.

## Potential Uses and Considerations for Analysts
- Suitable as a baseline for landslide risk assessment, change-detection studies, and correlation analyses with typhoon events.
- Single-mapper methodology introduces potential subjective bias; independent QC mitigates but does not eliminate it.
- Data attributes beyond geometry are not detailed here; users may need to inspect the attribute table for additional fields.
- Be mindful of the time window mismatch between imagery (2018–2019) and analysis (2020) when aligning with other datasets.