# WP3.2 Food web sites riparian vegetation structure data

- Purpose: Derive measures of the extent and complexity of riparian vegetation upstream of three chalkstream sites to understand relationships between in-stream biological communities and catchment/riparian land use.
- Study area: Wessex chalk streams; River Till, River Wylye, and Nine Mile River.

## What was recorded and data format
- For each site, statistics describing vegetation height along banks were computed:
  - Minimum, maximum, mean, and standard deviation of vegetation height.
  - Calculated for multiple upstream distances: 100 m, 200 m, and 1 km.
  - Within a 10 m wide riparian buffer strip on each bank (two banks).
- Vegetation categories analyzed:
  - All vegetation
  - Trees (>2 m)
  - Low vegetation (<2 m)
  - Buildings masked out
- Outputs included:
  - Area (m2) and volume (m3) of vegetation within the defined buffers and distances.
- Data fields include: river and site identifiers, geographic coordinates, distance upstream, vegetation category, area, volume, and height statistics.

## Data collection and provenance
- Data source: LiDAR data held by Environment Agency; processed to extract vegetation statistics.
- Processing: Conducted by Dr John Redhead (Centre for Ecology and Hydrology) from LiDAR data requested by Dr John Murphy (Queen Mary University of London).
- Timing: LiDAR data requested/received in April 2014; processing followed to generate statistics.
- LiDAR details: Airborne laser scanning with up to 100,000 measurements per second; high-resolution surface/terrain models (25 cm to 2 m); data include digital surface models and vegetation height information.

## Sampling design and study context
- Location: Chalkstream sites within the Wessex area; chosen to represent a gradient of catchment land cover (from calcareous grassland/woodland to arable/improved grasslands).
- Buffer and distance definitions: 10 m riparian buffers on each bank; analyses conducted for 100 m, 200 m, and 1 km upstream.

## Data quality and completeness
- Completeness: Data are complete.
- Validation checks:
  - Visual checks in ArcGIS to confirm buffer alignment upstream of each site.
  - Consistency check ensuring Tree + Low heights equal All vegetation heights.

## Data structure and metadata
- Key fields:
  - RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME
  - NGR, EASTING, NORTHING
  - Distance_upstream_m (buffer distance: 100 m, 200 m, 1 km)
  - Vegetation category (All, Trees >2 m, Low <2 m)
  - AREA_m2, VOLUME_m3
  - MIN_HEIGHT_m, MAX_HEIGHT_m, MEAN_HEIGHT_m, SD_HEIGHT_m
- Additional notes:
  - Buildings masked out in the vegetation analyses.
  - LiDAR metadata: Environment Agency LIDAR Composite DSM - 1m; referenced as 2015; data.gov.uk dataset link provided.

## Purpose for analysts and potential uses
- Enables examination of how riparian vegetation structure relates to in-stream biological communities and catchment land-use gradients.
- Provides standardized, region-specific vegetation metrics across multiple upstream distances for robust comparative analyses.

## References
- Environment Agency LiDAR Composite DSM - 1m (2015). https://data.gov.uk/dataset/lidar-composite-dsm-1m1