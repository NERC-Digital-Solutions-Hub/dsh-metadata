# WP3.2 Food web sites riparian vegetation structure data

- Purpose and scope
  - Measure the extent and complexity of riparian vegetation upstream of three chalkstream sites (River Till, River Wylye, Nine Mile River) in the Wessex chalk area as part of Wessex BESS WP 3.2.
  - Use LiDAR-derived metrics to relate riparian vegetation to in-stream biological communities and catchment land use gradients.

- Data and form
  - Derived statistics include minimum, maximum, mean, and standard deviation of vegetation heights, plus total vegetation area and volume.
  - Data are organized for each defined upstream area relative to the sampling point: a 10 m wide riparian strip on each bank, at upstream distances of 100 m, 200 m, or 1 km.

- Vegetation categories
  - Vegetation height split: Trees (>2 m) and Low vegetation (<2 m); buildings masked out.
  - Statistics calculated for all vegetation together and separately for Trees and Low vegetation.

- Study locations and timing
  - Sites: River Till, River Wylye, Nine Mile River (three chalkstreams in the Wessex area).
  - Data collection period: LiDAR data requested in April 2014; processed to generate statistics subsequently.

- Data collection and processing method
  - Method: Airborne LiDAR to measure ground/vegetation elevations; up to 100,000 measurements per second; high-resolution surface models (25 cm to 2 m).
  - Data source: Environment Agency LiDAR archive (digital surface data from surveys since 1998); LiDAR metadata available via data.gov.uk.
  - Processing: Separation of vegetation by height thresholds; calculation of area and volume for each defined upstream area.

- Rationale and use
  - Aimed to improve understanding of how catchment land use and riparian vegetation structure influence in-stream biological communities along a gradient of land-use intensification.

- Provenance and responsibility
  - Data requested by Dr. John Murphy (Queen Mary University of London); statistics derived by Dr. John Redhead (Centre for Ecology and Hydrology).

- Completeness and quality assurance
  - Data are complete.
  - Quality checks: visual verification of upstream buffer strips in ArcGIS; sum checks to ensure Tree and Low values equal All values.

- Data structure and key fields (columns)
  - River and site identifiers: RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME
  - Location: NGR, EASTING, NORTHING
  - Upstream context: Distance_upstream_m (distance upstream of NGR for the buffer)
  - Vegetation data: Vegetation (Trees >2 m; Low vegetation <2 m; buildings masked)
  - Metrics: AREA_m2, VOLUME_m3
  - Height statistics: MIN_HEIGHT_m, MAX_HEIGHT_m, MEAN_HEIGHT_m, SD_HEIGHT_m

- Access and references
  - LiDAR data reference: Environment Agency LIDAR Composite DSM - 1m. 2015.
  - Data accessibility note: LiDAR metadata and datasets linked via data.gov.uk

- Implications for monitoring and policy
  - Demonstrates how standardized, high-resolution vegetation metrics can support long-term environmental health assessments and policy performance by enabling consistent comparisons across locations and time.