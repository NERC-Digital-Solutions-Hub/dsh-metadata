# Landscapes

- The two landscapes are part of the Treescapes STAND project, led by the RSPB: North Pennines & Dales (England) and the Elenydd (mid Wales).

## Methods

- Goal: identify tree cover and height across the landscapes using LiDAR-derived data to create canopy height models (CHMs).
- CHM creation: CHM = DSM − DTM (DSM minus DTM).
- Data sources:
  - England: Environment Agency National LiDAR Programme, accessed via the R package gblidar.
  - Wales: Welsh Government LiDAR Cloud Optimized GeoTIFFs, imported into QGIS and clipped to the Elenydd boundary.
- Analysis of CHMs:
  - Determine dominant treetops, height values, and tree crowns with ForestTools (functions vwf and mcws) using a 1.5 m height threshold (captures shrubs/scrub but excludes most built structures).
  - Buildings removed from tree tops and crowns data using OS Local buildings data.
- Outputs: total canopy cover percentage and mean tree height calculated for each landscape at 10 m resolution.

## Outputs

- Figure 2: Comparison of satellite imagery of woodlands and other trees with the LiDAR-derived tree canopy cover.

## Data sources and tools

- R packages: gblidar, ForestTools.
- GIS software: QGIS.
- Data sources referenced: Environment Agency National LiDAR Programme, Welsh Government LiDAR, OS OpenMap Local.

## References

- EnvironmentAgency. (2023). National Lidar Programme.
- Graham, H. (2023). gblidar: A package to download tiled and point cloud LiDAR data for Great Britain.
- OrdnanceSurvey. (2023). OS OpenMap - Local.
- Plowright, A. (2023). ForestTools: Tools for Analyzing Remote Sensing Forest Data.
- Syder, A. et al. (in prep). Visioning future treescapes in upland landscapes: using deliberative processes to understand values and land-use preferences of local stakeholders, Ecosystems and People.
- WelshGovernment. (2023). LiDAR Welsh Government.