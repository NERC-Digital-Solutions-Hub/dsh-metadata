# Chalkstream survey riparian vegetation structure data

## Overview
- LiDAR-derived statistics describing the extent and complexity of riparian vegetation upstream of chalkstream sites in the WessexBESS WP 3.1 study.
- Aimed at understanding relationships between in-stream biological communities and catchment/riparian land use.

## What is recorded and data form
- For each site, statistics describing vegetation height within a 10 m wide buffer strip on each bank, upstream of the sampling location, at distances of 100 m, 200 m, and 1 km.
- Calculated metrics include minimum, maximum, mean, and standard deviation of vegetation height, plus area (m2) and volume (m3) of vegetation within the defined buffers.
- Data are split by vegetation type: Trees (>2 m) and Low vegetation (<2 m); buildings are masked out.
- Data are derived from LiDAR DSM data (1 m resolution; up to 100,000 measurements per second) and complemented by QA checks.

## Study area and timing
- 15 chalkstreams located along the white chalk geology corridor from Dorset (southwest) through Wiltshire to Hampshire (northeast).
- LiDAR data requested in 2014; processed for this study by CEH; originally from Environment Agency LiDAR archive (surveys since 1998).

## How the data were collected
- LiDAR airborne laser scanning generates detailed surface models; a 10 m riparian buffer on both banks was used, with three upstream distances (100 m, 200 m, 1 km).
- Vegetation statistics calculated separately for all vegetation, trees, and low vegetation; buildings masked.
- Metadata: LiDAR data and related documentation available (LiDAR Composite DSM - 1 m).

## Why the data were collected
- To inform understanding of how riparian vegetation structure relates to in-stream biological communities and catchment land use across a gradient of land-cover intensification.

## Responsibility and provenance
- Data requests by Dr. John Murphy (Queen Mary University of London); processing and extraction of vegetation statistics by Dr. John Redhead (Centre for Ecology and Hydrology).
- Completeness: LiDAR data obtained for 15 of 20 sites; data for 5 sites unavailable.

## Data quality and checks
- Visual verification in ArcGIS confirmed buffer strip alignment upstream of sites.
- Consistency check: sum of Tree and Low vegetation values matched the All-vegetation values.

## Data fields (column definitions)
- RIVER_ID: Unique river identifier (Britain)
- SITE_ID: Unique sampling location identifier along each river
- RIVER_NAME: River name
- SITE_NAME: Site name
- NGR: Ordnance Survey National Grid Reference
- EASTING: OS Easting
- NORTHING: OS Northing
- Distance_upstream_m: Distance upstream (km) of the 10 m buffer strip; values include 100 m, 200 m, or 1 km
- Vegetation: LiDAR-derived vegetation data split by height (>2 m as Trees; <2 m as Low vegetation; buildings masked)
- AREA_m2: Area covered by the defined buffers
- VOLUME_m3: Vegetation volume within the defined buffers
- MIN_HEIGHT_m: Minimum vegetation height within the sampled area
- MAX_HEIGHT_m: Maximum vegetation height within the sampled area
- MEAN_HEIGHT_m: Mean vegetation height within the sampled area
- SD_HEIGHT_m: Standard deviation of vegetation height within the sampled area

## Access and references
- References: Environment Agency LIDAR Composite DSM - 1 m (2015)
- Data source link: data.gov.uk dataset /lidar-composite-dsm-1m1

## Potential uses for data leaders
- Data discovery, governance, and reuse: track provenance, assess data gaps, and plan data collection or integration with other datasets.
- Support for decision-making: relate riparian structure to aquatic ecosystem indicators and land-use policy analyses.
- Metadata and discoverability enhancements: leverage clear column definitions, buffer geometry, and upstream distance documentation to improve data discovery and interoperability across networks of partners.