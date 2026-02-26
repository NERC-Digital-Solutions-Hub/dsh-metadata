# Chalkstream survey riparian vegetation structure data

## Overview
- LiDAR-derived statistics describing the extent and complexity of riparian vegetation upstream of chalkstream sites in the WessexBESS WP 3.1 project.
- For each site: minimum, maximum, mean, and standard deviation of vegetation height within defined upstream buffer areas.
- Statistics are computed for all vegetation and separately for trees (>2 m) and low vegetation (<2 m); buildings are masked out.
- Data are intended to inform relationships between in-stream biological communities and catchment/riparian land use.

## Data scope and geography
- Location: 15 chalkstreams along the white chalk geology from Dorset (southwest) through Wiltshire to Hampshire (northeast).
- Sampling context: 15 of 20 stream sites sampled in July 2012 as part of WessexBESS WP 3.1.
- Upstream buffers: 10 m wide riparian strips on each bank at distances of 100 m, 200 m, or 1 km upstream from the sampling point.
- Data completeness: LiDAR-derived data available for 15 sites; data for the remaining 5 sites are not available.

## Data collection and methods
- Source data: Airborne LiDAR (laser) measurements; high-resolution surface/terrain models.
- Resolution and capability: 25 cm to 2 m spatial resolution; up to 100,000 measurements per second; LiDAR archives include data since 1998.
- Data separation: Vegetation classified as Trees (>2 m) and Low vegetation (<2 m); buildings masked out.
- Processing approach: For each site and upstream buffer, calculated:
  - Minimum, maximum, mean, standard deviation of vegetation height
  - Area (m2) occupied by vegetation within the buffer
  - Volume (m3) of vegetation within the buffer
- Metadata and sources: LiDAR metadata available; data requested from Environment Agency; processing performed by CEH.

## Timeline and provenance
- Data request: April 2014, by Dr John Murphy (Queen Mary University of London) from the Environment Agency.
- Data processing: By Dr John Redhead (Centre for Ecology and Hydrology) to extract vegetation statistics.
- Complementary context: LiDAR data used to understand relationships between riparian vegetation and catchment land use across gradients of intensification.

## Data fields and definitions
- Key columns:
  - RIVER_ID: Unique river identifier in Britain
  - SITE_ID: Unique sampling location identifier
  - RIVER_NAME / SITE_NAME: Names (from OS mapping)
  - NGR / EASTING / NORTHING: Spatial references (grid/coordinates)
  - Distance_upstream_m: Upstream distance of the 10 m buffer strip (100 m, 200 m, or 1 km)
  - Vegetation: Height-based classification (Trees >2 m; Low <2 m)
  - AREA_m2: Area within the buffer strip
  - VOLUME_m3: Vegetation volume within the buffer
  - MIN_HEIGHT_m / MAX_HEIGHT_m / MEAN_HEIGHT_m / SD_HEIGHT_m: Descriptive height statistics for vegetation within the area

## Quality assurance
- Visual checks in ArcGIS confirmed correct upstream buffer delineation and data application.
- Consistency checks ensured that Tree + Low totals matched the All category where applicable (verification of aggregated values).

## Data completeness and limitations
- Completeness: 15/20 sites covered; 5 sites lack LiDAR data.
- Limitations: The document notes potential data gaps, and the completeness issue should be considered when cross-site comparisons or gradient analyses are performed.

## Access, usage, and potential data products
- Primary outputs: Quantitative vegetation structure statistics by site and upstream distance, suitable for building dashboards or reports to explore riparian-vegetation structure relationships.
- Data provenance and citation: Environment Agency LiDAR data (LIDAR Composite DSM - 1 m) referenced; metadata link provided.
- Potential use: Assessing links between riparian vegetation structure and in-stream biological communities or land-use gradients across chalkstream catchments.

## References
- Environment Agency LIDAR Composite DSM - 1m. 2015. https://data.gov.uk/dataset/lidar-composite-dsm-1m1