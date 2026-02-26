# Landscapes

- Context: Part of the Treescapes STAND project led by the RSPB, focusing on two landscapes — North Pennines & Dales (England) and Elenydd (mid Wales). Figure 1 shows focal landscapes and locations in the UK.

## Methods

- Objective: Identify tree cover and height across the two landscapes using LiDAR-derived data to create canopy height models (CHMs).
- Data sources:
  - England: Environment Agency National LiDAR Programme (DTM and DSM) accessed via the R package gblidar.
  - Wales: Welsh Government LiDAR Cloud Optimized GeoTIFFs imported into QGIS and clipped to the Elenydd boundary.
- Processing steps:
  - CHM creation by CHM = DSM − DTM.
  - Extraction of dominant treetops, height values, and tree crowns from CHMs using ForestTools in R.
  - Height threshold: 1.5 m to capture shrubs/scrub while excluding built structures like dry stone walls.
  - Buildings removed from tree-top and crown data using OS Local buildings data.
- Outputs: Total canopy cover percentage and mean tree height computed for each landscape at 10 m resolution.

## Outputs and Visualization

- Figure 2 presents a comparison between satellite imagery of woodlands/trees and the LiDAR-derived canopy cover.

## Data Handling and Standards

- Data are sourced from established LiDAR datasets and processed with standardised methods (R packages gblidar, ForestTools; QGIS workflows).
- Outputs are generated at landscape scale with resolution of 10 m, enabling comparisons over time and across landscapes.

## References and Data Sources

- Environment Agency (National LiDAR Programme)
- Graham (gblidar R package)
- Ordnance Survey (OS OpenMap Local)
- Plowright (ForestTools R package)
- Syder et al. (in prep, related to visioning treescapes)
- Welsh Government LiDAR data