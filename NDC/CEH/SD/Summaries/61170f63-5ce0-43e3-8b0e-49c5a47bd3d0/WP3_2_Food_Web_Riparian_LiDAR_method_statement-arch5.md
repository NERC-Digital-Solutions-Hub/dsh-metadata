# WP3.2 Food web sites riparian vegetation structure data

- Purpose: Measure extent and complexity of riparian vegetation upstream of three chalkstream sites (River Till, River Wylye, Nine Mile River) using LiDAR data to relate in-stream biological communities to catchment and riparian land use.

- Study area and sites:
  - Three chalkstreams within the Wessex chalk area: River Till, River Wylye, Nine Mile River.

- Data collection timeline and provenance:
  - LiDAR data obtained from Environment Agency; requested by Dr John Murphy (Queen Mary University of London) and processed by Dr John Redhead (Centre for Ecology and Hydrology).
  - Data received in April 2014; LiDAR metadata available from data.gov.uk.

- Data collection methods:
  - LiDAR is airborne laser scanning capturing up to 100,000 measurements per second.
  - Spatial resolution: 25 cm to 2 m.
  - Data split into vegetation >2 m (Trees) and vegetation <2 m (Low); buildings masked out.
  - Buffer areas defined: 10 m wide on each bank, at distances upstream of sampling point of 100 m, 200 m, and 1 km.
  - For each area, computed statistics from LiDAR: minimum, maximum, mean, and standard deviation of vegetation heights; plus total vegetation area (AREA_m2) and volume (VOLUME_m3).

- Data variables and structure:
  - Tree and All vegetation statistics, plus Low vegetation statistics.
  - Core fields (example): 
    - RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME
    - NGR, EASTING, NORTHING (grid references)
    - Distance_upstream_m (100, 200, 1000)
    - Vegetation categories: All, Trees (>2 m), Low (<2 m)
    - AREA_m2, VOLUME_m3
    - MIN_HEIGHT_m, MAX_HEIGHT_m, MEAN_HEIGHT_m, SD_HEIGHT_m

- Why the data were collected:
  - To understand relationships between in-stream biological communities and catchment/riparian land use across a gradient of land-cover intensity (from calcareous grassland/woodland to arable/improved grasslands).

- Data completeness and quality assurance:
  - Status: Data are complete.
  - Quality checks: Visual verification of buffer strips in ArcGIS; verification that Tree + Low heights sum to All heights.
  - Metadata and definitions clearly documented (column definitions and units provided).

- Provenance and access:
  - LiDAR metadata: Environment Agency LIDAR Composite DSM - 1m (2015).
  - Data access notes: Metadata and dataset referenced via data.gov.uk; processing carried out by CEH.

- Use considerations and governance for Data Stewards:
  - Clear, tabulated definitions for each field, including units and height thresholds, enabling consistent reuse and integration with other datasets.
  - Temporal note: data reflect 2014 LiDAR and may not capture subsequent landscape changes without updates.
  - Ensure ongoing data governance: maintain buffer definitions, distance classes, and height categorization; preserve the linkage between site identifiers (RIVER_ID, SITE_ID) and geographic coordinates for discoverability and reuse.