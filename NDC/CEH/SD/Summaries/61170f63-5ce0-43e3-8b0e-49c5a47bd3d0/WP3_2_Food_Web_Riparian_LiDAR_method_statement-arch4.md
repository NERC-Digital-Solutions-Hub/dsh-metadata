# WP3.2 Food web sites riparian vegetation structure data

## Overview
- LiDAR-derived statistics describing the extent and complexity of riparian vegetation upstream of three chalkstream sites in the Wessex BESS project: River Till, River Wylye, and Nine Mile River.
- Metrics include minimum, maximum, mean, and standard deviation of vegetation height, calculated for defined upstream buffer strips (10 m wide on each bank) at distances upstream of the sampling location (100 m, 200 m, and 1 km).
- Purpose: understand relationships between in-stream biological communities and catchment/riparian land use.

## Data collection and scope
- Data collected in the Wessex chalk area along three streams: River Till, River Wylye, and Nine Mile River.
- LiDAR data requested by Dr. John Murphy (Queen Mary University of London) and sourced from the Environment Agency; data received in April 2014.
- Completeness: the data are complete for the defined sampling framework.

## Data collection methods
- Technique: Airborne LiDAR (laser ranging) with up to ~100,000 measurements per second; high-resolution surface/terrain models (25 cm to 2 m).
- Processing: LiDAR data split into vegetation >2 m (Trees) and vegetation <2 m (Low vegetation); buildings masked out.
- Spatial scope: For each sampling point, defined riparian buffers (10 m wide on each bank) at upstream distances of 100 m, 200 m, and 1 km.
- Derived statistics per buffer: minimum, maximum, mean, and standard deviation of vegetation heights; also area (m2) and vegetation volume (m3).

## Data content and structure
- Vegetation statistics are provided for all vegetation and separately for Trees (>2 m) and Low vegetation (<2 m).
- Key variables include:
  - RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME
  - NGR (grid reference), EASTING, NORTHING
  - Distance_upstream_m (upstream distance in meters corresponding to each buffer)
  - AREA_m2, VOLUME_m3 (area and volume within the buffer)
  - MIN_HEIGHT_m, MAX_HEIGHT_m, MEAN_HEIGHT_m, SD_HEIGHT_m (height statistics)
- Data are organized around a 10 m buffer strip on both banks, with segments at 100 m, 200 m, and 1 km upstream.

## Provenance and responsibilities
- Data request and interpretation: Dr. John Murphy (Queen Mary University of London).
- Data processing and statistics extraction: Dr. John Redhead (Centre for Ecology and Hydrology).
- Purpose: to elucidate links between riparian/land-use characteristics and aquatic communities across catchment gradients.

## Data quality and checks
- Visual checks performed in ArcGIS to confirm buffer integrity upstream of sampling sites.
- Consistency check: sum of Tree and Low vegetation values equals the All (total) value.

## Metadata, standards, and access
- LiDAR metadata available from the Environment Agency and linked data.gov.uk dataset: LIDAR Composite DSM - 1m1 (data.gov.uk).
- The dataset is documented with a table of column headings and definitions (as listed above) to support discoverability and reuse.

## Context and references
- The data contribute to understanding ecological relationships along chalkstreams and their catchment contexts.
- Reference: Environment Agency LiDAR Composite DSM - 1m; data coverage and processing described in the project documentation.