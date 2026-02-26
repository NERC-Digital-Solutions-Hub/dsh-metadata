# WP3.2 Food web sites riparian vegetation structure data

- A LiDAR-derived dataset describing the extent and complexity of riparian vegetation upstream of three chalkstream sampling sites in the Wessex area: River Till, River Wylye, and Nine Mile River.
- For each site, provides minimum, maximum, mean, and standard deviation of vegetation height along banks, within defined upstream buffer zones.

## Data collection context

- LiDAR data requested by Dr John Murphy (Queen Mary University of London) and received from the Environment Agency in April 2014; processed by Dr John Redhead (Centre for Ecology and Hydrology).
- Source: Environment Agency LiDAR archive (digital surface models) from surveys since 1998; data used span 25 cm to 2 m spatial resolution.
- Coverage: three rivers in the Wessex chalk area; riparian analysis focuses on 10 m wide buffers on both banks at defined upstream distances.

## Areas and metrics

- Upstream distances considered: 100 m, 200 m, and 1 km from the sampling location along the watercourse.
- Buffer: 10 m wide on each bank for each site/distance.
- Vegetation statistics computed for:
  - All vegetation
  - Trees (height > 2 m)
  - Low vegetation (height < 2 m)
  - Buildings masked out
- For each area, calculated:
  - Area (m2)
  - Volume (m3)
  - Min/Max/Mean/Standard deviation of vegetation heights (m)

## Data structure and key fields

- RIVER_ID: unique river identifier
- SITE_ID: unique sampling location identifier
- RIVER_NAME: river name
- SITE_NAME: site name
- NGR / EASTING / NORTHING: grid references
- Distance_upstream_m: distance upstream (km) of the buffer zone from the NGR
- Vegetation: height-based categorization (All, Trees >2 m, Low <2 m)
- AREA_m2: area covered by the buffer and defined upstream distance
- VOLUME_m3: vegetation volume within the area
- MIN_HEIGHT_m, MAX_HEIGHT_m, MEAN_HEIGHT_m, SD_HEIGHT_m: height statistics for vegetation within the area

## Data processing and quality checks

- Processing steps included separating vegetation by height class and masking buildings.
- Visual checks in ArcGIS confirmed buffer strips and data validity.
- Consistency check ensured that the sum of Tree and Low vegetation equals the All vegetation value.

## Completeness and provenance

- Data are complete for the defined three chalkstreams and upstream distances.
- Responsible collaboration: data requested by Dr John Murphy and processed by Dr John Redhead.
- Metadata and references:
  - LiDAR data source: Environment Agency LIDAR Composite DSM - 1 m, 2015.
  - Reference link: data.gov.uk dataset for LiDAR composites.