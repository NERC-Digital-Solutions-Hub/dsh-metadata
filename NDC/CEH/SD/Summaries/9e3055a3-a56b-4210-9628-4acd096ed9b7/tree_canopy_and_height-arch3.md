# Landscapes

- The Treescapes STAND project, led by the RSPB, covers two focal landscapes: North Pennines & Dales in England and Elenydd in mid Wales. The aim is to identify tree cover and height across these landscapes to inform monitoring, policy scrutiny, and future decision-making.

- Methods
  - Data sources:
    - England: Environment Agency National LIDAR Programme data accessed via the R package gblidar.
    - Wales: Welsh Government LiDAR Cloud Optimized GeoTIFFs imported into QGIS.
  - Processing steps:
    - Clip LiDAR data to the landscape boundaries.
    - Create canopy height models (CHMs) by subtracting DSM from DTM (CHM = DSM − DTM).
    - Derive dominant treetops, height values, and tree crowns from CHMs using ForestTools (functions vwf and mcws) with a 1.5 m threshold to include short vegetation but exclude structures like walls.
    - Remove buildings using OS local buildings data.
  - Outputs:
    - Total canopy cover percentage and mean tree height calculated for each landscape at a 10 m resolution.

- Outputs and visualization
  - Figure 2 presents a comparison between satellite imagery of woodlands/trees and the LiDAR-derived canopy cover.

- Data and tools
  - R: gblidar, ForestTools (ForestTools v1.0.0)
  - GIS: QGIS
  - Data sources: Environment Agency National LIDAR Programme, Welsh Government LiDAR data, OS OpenMap Local for buildings

- Relevance to monitoring frameworks
  - Provides measurable indicators (canopy cover and mean height) to monitor landscape-scale tree cover and structure.
  - Demonstrates integration of multiple open data sources and transparent processing workflows suitable for monitoring purposes.
  - Uses reproducible methods (CHM creation, vegetation threshold, building exclusion) and standard software to support ongoing governance and reporting of woodland extent.

- References and data sources (highlights)
  - Environment Agency (National LIDAR Programme); Graham (gblidar); Ordnance Survey (OS OpenMap Local); Plowright (ForestTools); Welsh Government LiDAR data.