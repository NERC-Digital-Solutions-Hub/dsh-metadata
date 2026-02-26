# WP3.2 Food web sites riparian vegetation structure data

## Overview
- Describes LiDAR-derived measures of riparian vegetation extent and complexity upstream of three chalkstream sites in the Wessex chalk area (River Till, River Wylye, Nine Mile River).
- Aims to relate in-stream biological communities to catchment and riparian land use.

## Data scope and content
- For each site, statistics summarize vegetation along banks within defined upstream buffers.
- Buffers: 10 m wide on each bank, evaluated at distances upstream of the sampling point of 100 m, 200 m, and 1 km.
- Vegetation statistics computed for all vegetation and separately for:
  - Trees (>2 m)
  - Low vegetation (<2 m)
  - Buildings masked out
- Statistics include:
  - Height metrics: minimum, maximum, mean, standard deviation
  - Area (m2) and Volume (m3) of vegetation within the buffers

## Data collected and processing
- Source: LiDAR data from Environment Agency, processed to extract vegetation statistics.
- Data request and processing:
  - Requested by Dr John Murphy (Queen Mary University of London) in April 2014
  - Processed to retrieve vegetation statistics by Dr John Redhead (Centre for Ecology and Hydrology)
- LiDAR details:
  - Airborne laser scanning with up to 100,000 measurements per second
  - Spatial resolution between 25 cm and 2 m
  - LiDAR archive includes DSM data from surveys since 1998
  - Data separated into vegetation >2 m (trees) and <2 m (low vegetation), with non-vegetation (buildings) masked

## Data structure and metadata
- Key identifiers: River_ID, Site_ID, River_Name, Site_Name
- Spatial references: NGR (grid reference), Easting, Northing
- Distance metric: Distance_upstream_m (upstream distance in meters; 100 m, 200 m, 1 km)
- Vegetation metrics: AREA_m2, VOLUME_m3, MIN_HEIGHT_m, MAX_HEIGHT_m, MEAN_HEIGHT_m, SD_HEIGHT_m
- Vegetation classification: Trees (>2 m) vs Low vegetation (<2 m); All values and category-specific sums provided

## Data quality and completeness
- Completeness: Data are reported as complete
- Quality checks:
  - Visual verification in ArcGIS of buffer strips upstream of each site
  - Consistency check: sum of Tree and Low values equals All values for height statistics

## Rationale and use cases
- Purpose: to understand relationships between in-stream biological communities and catchment/riparian land use across a gradient of catchment land cover intensification.
- Enables researchers to link LiDAR-derived riparian structure with ecological outcomes in chalkstreams.
- Data can support analyses on spatial patterns of vegetation structure and potential impacts on aquatic ecosystems.

## Access and references
- Data metadata and LiDAR context available via data.gov.uk (LIDAR Composite DSM - 1m, 2015)
- Site context: WessexBESS WP 3.2
- Key contributors: Dr John Murphy (QMUL) and Dr John Redhead (CEH)