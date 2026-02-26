# Landscapes

- The Landscapes component of the Treescapes STAND project, led by the RSPB, covers two focal landscapes: North Pennines & Dales in England and Elenydd in mid Wales.
- Goal: identify tree cover and height across both landscapes using LiDAR-derived data to produce comparable canopy metrics.

## Methods

- Use LiDAR-derived digital elevation models (DTM) and digital surface models (DSM) to create canopy height models (CHM) by CHM = DSM − DTM.
- England data: downloaded from the Environment Agency National LIDAR Programme and processed with the R package gblidar.
- Wales data: Welsh Government LiDAR Cloud Optimized GeoTIFFs imported into QGIS and clipped to the Elenydd boundary.
- Feature extraction: dominant treetops, height values, and tree crowns derived from CHM with ForestTools (R) using vwf and mcws; height threshold set at 1.5 m to capture shrubs/scrub while excluding built structures.
- Data cleaning: remove buildings using OS Local building data.
- Outputs: compute total canopy cover percentage and mean tree height for each landscape at a 10 m resolution.

## Data Products and Outputs

- CHM-based metrics (dominant treetops, height values, tree crowns) across both landscapes.
- Canopy cover maps and mean height maps at 10 m resolution.
- Figure 2 illustrates the comparison between satellite imagery and LiDAR-derived canopy cover, supporting interpretation and validation of the maps.

## Tools and Data Sources

- England: Environment Agency National LiDAR Programme; processed with gblidar (R).
- Wales: Welsh Government LiDAR Cloud Optimized GeoTIFFs; processed in QGIS.
- ForestTools (R) for tree metrics extraction; OS OpenData for building removal.

## Relevance for Data Support

- Demonstrates end-to-end data workflow: data acquisition from multiple sources, harmonization and cleaning, CHM creation, feature extraction, and production of user-ready canopy and height products.
- Produces spatially explicit, reusable data products suitable for landscape-scale woodlands assessment and decision support.