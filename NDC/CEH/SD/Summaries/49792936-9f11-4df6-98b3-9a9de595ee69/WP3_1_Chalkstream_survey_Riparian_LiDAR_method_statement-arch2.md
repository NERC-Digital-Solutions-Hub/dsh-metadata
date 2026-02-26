# Chalkstream survey riparian vegetation structure data

## Purpose and data overview
- Derived from LiDAR data to measure extent and complexity of riparian vegetation upstream of chalkstream sites sampled in WessexBESS WP 3.1.
- For each site, provides minimum, maximum, mean, and standard deviation of vegetation height along banks for multiple distances upstream.

## Data collection context
- 15 discrete chalkstreams along the white chalk geology from Dorset to Hampshire.
- LiDAR data requested by Dr John Murphy (Queen Mary University of London) and received from the Environment Agency in April 2014; processed by Dr John Redhead (Centre for Ecology and Hydrology).

## Data collection methods
- LiDAR: airborne laser scanning with up to 100,000 measurements per second; high-resolution surface/terrain models (25 cm to 2 m).
- Data split into: trees (>2 m) and low vegetation (<2 m); buildings masked out.
- Analysis areas: a 10 m wide riparian buffer strip on each bank, located upstream at 100 m, 200 m, or 1 km.
- For each area and vegetation category: compute minimum, maximum, mean, and standard deviation of heights, plus total vegetation area and volume.

## Data completeness and quality
- LiDAR data available for 15 of 20 stream sites; data missing for 5 sites.
- Quality checks include visual validation in ArcGIS of upstream buffer strips and verification that Tree + Low totals equal All.
- Metadata available: LiDAR Composite DSM - 1 m; data portal reference at data.gov.uk.

## Data structure and variables
- Key columns include:
  - RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME, NGR, EASTING, NORTHING
  - Distance_upstream_m (100 m, 200 m, 1 km)
  - Vegetation categories: Trees (>2 m) and Low vegetation (<2 m); buildings masked
  - AREA_m2, VOLUME_m3
  - MIN_HEIGHT_m, MAX_HEIGHT_m, MEAN_HEIGHT_m, SD_HEIGHT_m
- Distances and metrics are defined for each buffered upstream area and bank.

## Purpose and application
- Aims to understand relationships between in-stream biological communities and catchment/riparian land use.
- Sites span a gradient of catchment land cover intensification, from calcareous grassland/woodland to arable/improved grasslands.

## Access and references
- LiDAR metadata and related data available through data.gov.uk (Environment Agency LIDAR DSM - 1m, 2015).
- Source data linked to the chalkstream survey within WessexBESS WP 3.1.