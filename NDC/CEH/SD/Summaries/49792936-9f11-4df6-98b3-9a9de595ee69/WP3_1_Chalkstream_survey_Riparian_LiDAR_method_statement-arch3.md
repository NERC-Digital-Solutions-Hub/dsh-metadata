# Chalkstream survey riparian vegetation structure data

## Overview
- LiDAR-derived measures of riparian vegetation extent and complexity upstream of chalkstream sampling sites (15 of 20 sites sampled in July 2012 for WessexBESS WP 3.1).
- Statistics calculated: minimum, maximum, mean, and standard deviation of vegetation heights; total vegetation area and volume. Data are separated for trees (>2 m) and low vegetation (<2 m), with buildings masked out.

## Data collection context
- Location: 15 chalkstreams along white chalk geology from Dorset to Hampshire (southwest to northeast).
- Project: Wessex BESS WP 3.1.
- Data requested by: Dr. John Murphy (Queen Mary University of London); processed by Dr. John Redhead (Centre for Ecology and Hydrology).
- LiDAR collection date: 2014 (data originally from EA archives dating back to 1998).

## Methods
- Technique: airborne LiDAR mapping; up to 100,000 ground measurements per second; spatial resolution 25 cm to 2 m.
- Data split: vegetation >2 m vs. <2 m; buildings masked.
- Buffer zones: for each site, 10 m wide riparian strips on both banks at upstream distances of 100 m, 200 m, and 1 km.
- Calculations per buffer: min, max, mean, SD of vegetation heights; area (m2); volume (m3).

## Purpose and use
- Aims to understand relationships between in-stream biological communities and catchment/riparian land use.
- Sites chosen to span gradients from calcareous grassland/woodland to arable/improved grassland.

## Data provenance and access
- Data collected by Environment Agency; processed for this study by Centre for Ecology and Hydrology.
- LiDAR metadata available via data.gov.uk (LIDAR Composite DSM - 1m; 2015).

## Completeness and limitations
- Completeness: LiDAR data available for 15 of 20 stream sites; 5 sites missing.
- Validation: visual checks in ArcGIS to confirm buffer alignment; sums of tree and low vegetation equalled totals.

## Data structure and key fields
- Site identifiers and geography: RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME, NGR_EASTING, NGR_NORTHING.
- Upstream context: Distance_upstream_m (distance up the watercourse for the buffer).
- Vegetation metrics: Vegetation (Trees >2m; Low <2m); AREA_m2; VOLUME_m3; MIN_HEIGHT_m; MAX_HEIGHT_m; MEAN_HEIGHT_m; SD_HEIGHT_m.
- Buffering: 10 m buffer strips on both banks at 100 m, 200 m, and 1 km upstream.

## Data quality and governance
- Quality controls: internal visual checks; consistency checks ensuring components sum to totals.
- Governance: data sharing of underlying LiDAR data; metadata availability noted.

## Relevance for monitoring frameworks
- Provides concrete, GIS-/LiDAR-derived indicators of riparian structure that can be linked to ecological monitoring and policy evaluation.
- Highlights practical data challenges relevant to monitoring frameworks: data gaps, access, metadata adequacy, data transformation needs, and governance requirements.