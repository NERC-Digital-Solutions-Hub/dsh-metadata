# Chalkstream survey riparian vegetation structure data

## Overview
- Derived from LiDAR data to quantify riparian vegetation upstream of chalkstream sampling sites as part of WessexBESS WP 3.1.
- For each site, provides minimum, maximum, mean, and standard deviation of vegetation height along the banks for specified downstream/upstream distances.

## Data collection and scope
- Location: 15 discrete chalkstreams along white chalk geology from Dorset (southwest) to Hampshire (northeast).
- Timeframe:
  - LiDAR data requested April 2014; processed subsequently.
  - Field sites surveyed July 2012 for WessexBESS WP 3.1; LiDAR-derived statistics reference these sites.
- Data availability: 15 of 20 stream sites have LiDAR-derived data; data for 5 sites are not available.
- Data source and processing: LiDAR is an airborne laser technique; up to 100,000 measurements per second; delivers high-resolution surface data (roughly 25 cm to 2 m resolution). Data split into Trees (>2 m from ground) and Low vegetation (<2 m) with buildings masked.

## Spatial and buffer definitions
- Buffer zones: 10 m wide riparian strips on each bank, evaluated at three upstream distances from the sampling point: 100 m, 200 m, and 1 km.
- For each defined area, statistics computed for all vegetation and separately for Trees and Low vegetation.

## Metrics and data products
- For each buffer area and vegetation category:
  - Height statistics: minimum, maximum, mean, standard deviation.
  - Vegetation extent: area (m²) and volume (m³) within the buffer.
- Data are provided as aggregated statistics for all vegetation and by category (Trees >2 m; Low vegetation <2 m; buildings masked).

## Data quality and validation
- Visual checks performed in ArcGIS to confirm buffer geometry and site alignment.
- Consistency checks: sum of Tree and Low vegetation values equals the All-category values.

## Data fields and definitions
- RIVER_ID: Unique river identifier in Britain.
- SITE_ID: Unique sampling location identifier along each river.
- RIVER_NAME: River name (from OS map).
- SITE_NAME: Site name.
- NGR: Ordnance Survey National Grid Reference.
- EASTING / NORTHING: OS coordinates.
- Distance_upstream_m: Upstream distance (km) of the buffer from the NGR along the watercourse (100 m, 200 m, or 1 km).
- Vegetation: Height-based categorization; data split into Trees (>2 m) and Low vegetation (<2 m); buildings masked out.
- AREA_m2: Area (m²) encompassed by the 10 m upstream buffer strips on both banks.
- VOLUME_m3: Vegetation volume (m³) within the defined buffer and distance.
- MIN_HEIGHT_m / MAX_HEIGHT_m / MEAN_HEIGHT_m / SD_HEIGHT_m: Vegetation height statistics (meters) within the sampled area.

## Purpose and context
- Aims to illuminate relationships between in-stream biological communities and catchment/riparian land use.
- Sampling covers a gradient of catchment land cover from calcareous grassland/woodland to arable/improved grassland.

## References and metadata
- Primary LiDAR source: Environment Agency LIDAR Composite DSM - 1m (2015). URL: data.gov.uk dataset lidar-composite-dsm-1m1
- Data availability note: five streams lacked LiDAR data; 15 streams included in the dataset.