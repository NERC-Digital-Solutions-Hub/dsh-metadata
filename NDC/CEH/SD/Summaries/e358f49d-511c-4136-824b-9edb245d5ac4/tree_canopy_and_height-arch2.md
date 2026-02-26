# Landscapes

- Overview
  - Part of the Treescapes STAND project led by the RSPB.
  - Focal landscapes: North Pennines & Dales in England and Elenydd in mid Wales.

- Methods
  - Data sources: LiDAR-derived DTM and DSM to create canopy height models (CHM); English data from the National LiDAR Programme; Welsh data from Welsh Government LiDAR Cloud Optimized GeoTIFFs.
  - Processing: CHM = DSM − DTM; dominant treetops, height values, and tree crowns derived from CHM using ForestTools (vwf and mcws) with a 1.5 m height threshold to include shrubs but exclude built structures.
  - Data cleaning: Buildings removed using OS local buildings data.
  - Output calculations: Total canopy cover percentage and mean tree height computed for each landscape at 10 m resolution.
  - Software/tools: R (gblidar, ForestTools), QGIS for Wales data handling.

- Outputs
  - Figure 2: Comparison of satellite imagery of woodlands and other trees with LiDAR-derived canopy cover.
  - Generated maps/data products for canopy cover and mean height at landscape scale.

- Data sources and stewardship
  - Primary LiDAR sources: Environment Agency National LiDAR Programme; Welsh Government LiDAR.
  - Supporting data: OS OpenMap Local for building removal.
  - Analytical approach emphasizes standardised, repeatable processing to enable monitoring of environmental structure.

- Relevance to environmental monitoring
  - Provides standardized metrics (canopy cover %, mean height) to assess tree presence and structure across landscapes.
  - Outputs support environmental health reporting and policy performance evaluation.

- Challenges and data access considerations
  - Increasing value by integrating canopy metrics with other environmental datasets (e.g., habitat, land-use data) and ensuring underlying data are accessible to others.