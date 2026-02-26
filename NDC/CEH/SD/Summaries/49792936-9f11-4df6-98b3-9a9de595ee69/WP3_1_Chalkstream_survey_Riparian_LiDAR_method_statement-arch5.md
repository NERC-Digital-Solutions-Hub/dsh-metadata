# Chalkstream survey riparian vegetation structure data

## Overview
- Derived from LiDAR data to measure extent and complexity of riparian vegetation upstream of chalkstream sites sampled in WessexBESS WP 3.1.
- For each site, provides minimum, maximum, mean, and standard deviation of vegetation height along the banks for specified upstream distances.

## Data collection and scope
- Location: 15 discrete chalkstreams along the white chalk geology from Dorset (southwest) to Hampshire (northeast).
- Temporal scope: LiDAR data requested by Dr John Murphy (QMUL) and received from the Environment Agency in April 2014; processed subsequently by Dr John Redhead (CEH).
- Completeness: LiDAR data available for 15 of 20 stream sites studied in July 2012 (WP 3.1); data for 5 sites not available.

## Data collection method
- LiDAR: airborne laser scanning, up to ~100,000 measurements per second; spatial resolution between 25 cm and 2 m.
- Data handling: split into vegetation taller than 2 m (Trees) and vegetation up to 2 m (Low vegetation); buildings masked out.
- Buffer zones: defined as a 10 m wide strip along each bank, at upstream distances of 100 m, 200 m, or 1 km.
- Calculations: for each buffer, compute min, max, mean, and SD of vegetation height; also compute total vegetation area (AREA_m2) and volume (VOLUME_m3). Statistics computed for All vegetation as well as separately for Trees and Low vegetation.

## Data content and structure
- Data fields (examples):
  - RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME
  - NGR, EASTING, NORTHING
  - Distance_upstream_m (100 m, 200 m, 1 km)
  - AREA_m2, VOLUME_m3
  - MIN_HEIGHT_m, MAX_HEIGHT_m, MEAN_HEIGHT_m, SD_HEIGHT_m
  - Vegetation category: Trees (>2 m) and Low vegetation (<2 m) with buildings masked out
- Metadata accessibility: LiDAR metadata available at data.gov.uk (LIDAR Composite DSM - 1m).

## Provenance and processing
- Data origin: Environment Agency LiDAR data.
- Processing: statistics derived by Dr John Redhead (CEH) for the study initiated by Dr John Murphy (QMUL).

## Quality assurance
- Visual verification in ArcGIS to confirm the validity of upstream buffer strips.
- Internal consistency check ensuring Tree + Low equals All where applicable.

## Usage notes and limitations
- Purpose: to understand relationships between in-stream biological communities and catchment/riparian land use across different land cover gradients.
- Limitations: incomplete site coverage (only 15/20 sites available); results limited to the defined buffers and vegetation height thresholds; buildings masked, which may affect some metrics.

## Metadata and references
- References: Environment Agency LiDAR data; Environment Agency LIDAR Composite DSM - 1m (2015).
- Data access: LiDAR metadata available via data.gov.uk (https://data.gov.uk/dataset/lidar-composite-dsm-1m1).