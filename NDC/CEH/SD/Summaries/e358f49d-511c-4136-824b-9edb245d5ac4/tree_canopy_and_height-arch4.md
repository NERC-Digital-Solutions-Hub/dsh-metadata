# Landscapes

- Overview
  - Part of the Treescapes STAND project led by the RSPB.
  - Focused on two focal landscapes: North Pennines & Dales (England) and Elenydd (mid Wales).
  - Objective: identify tree cover and height across these landscapes using LiDAR-derived data.

- Data sources
  - England: Environment Agency National LiDAR Programme for DTMs and DSMs, accessed via the R package gblidar.
  - Wales: Welsh Government LiDAR Cloud Optimized GeoTIFFs (2020–22), imported into QGIS and clipped to the Elenydd boundary.
  - Buildings: OS local buildings data used to remove buildings from tree top/crown data.

- Methods and processing
  - CHM creation: canopy height model obtained by CHM = DSM - DTM.
  - Feature extraction: dominant treetops, height values, and tree crowns derived from CHM using ForestTools (functions vwf and mcws) with a 1.5 m height threshold to include shrubs/scrub but exclude structures.
  - Data standardization: data clipped to landscape boundaries and analyzed at 10 m resolution.
  - Quality considerations: threshold chosen to balance capturing vegetation while ignoring built features.

- Outputs
  - Metrics computed: total canopy cover percentage and mean tree height for each landscape.
  - Visualization: Figure 2 showing comparison between satellite imagery of woodlands/trees and LiDAR-derived canopy cover.

- Tools and reproducibility
  - Software and packages: R (gblidar, ForestTools), QGIS, OS building data.
  - Data sources are cited with references to underlying datasets and tools.

- Implications for data leadership and strategy
  - Demonstrates an end-to-end data workflow combining multi-source LiDAR data with GIS processing to produce standardized landscape-scale vegetation metrics.
  - Highlights the importance of data integration across sources, clear boundary definitions, and consistent spatial resolution for repeatable reporting.
  - Shows how data products ( canopy cover, mean height ) can support landscape management decisions and monitoring, with potential for inclusion in broader data communities and collaborations.