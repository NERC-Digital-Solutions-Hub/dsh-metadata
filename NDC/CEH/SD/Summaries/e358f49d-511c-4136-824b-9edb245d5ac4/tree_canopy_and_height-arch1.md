# Landscapes

- Objective: Identify tree cover and height across two STAND landscapes (North Pennines & Dales in England; Elenydd in mid Wales) using LiDAR-derived models.

## Study areas
- North Pennines & Dales, England
- Elenydd, mid Wales

## Data and methods

- LiDAR data sources
  - England: Environment Agency National LIDAR Programme (DTM and DSM)
  - Wales: Welsh Government LiDAR Cloud Optimized GeoTIFFs (2020–22)
- Data access and workflows
  - England data retrieved via R package gblidar
  - Wales data imported into QGIS and clipped to the Elenydd boundary
- Canopy height model (CHM) creation
  - CHM = DSM − DTM
- Vegetation metrics extraction
  - Dominant treetops, height values, and tree crowns derived from CHM
  - ForestTools R package (functions vwf and mcws) with a height threshold of 1.5 m
  - Threshold 1.5 m captures shrub/scrub; excludes built structures (e.g., dry stone walls)
- Data cleaning
  - Buildings removed using Ordnance Survey local buildings data
- Output metrics
  - Total canopy cover percentage (Figure 2)
  - Mean tree height
  - Calculations performed at 10 m spatial resolution for each landscape

## Processing and tools

- Software and packages
  - R: gblidar, ForestTools
  - QGIS
- Boundary handling
  - CHMs clipped to landscape boundaries
- Visualization
  - Output includes comparison between satellite imagery and LiDAR-derived canopy cover (Figure 2)

## Outputs and references

- Outputs: Canopy cover (%) and mean tree height maps at 10 m resolution; figures illustrating CHM-based results
- Figure references
  - Figure 1: STAND focal landscapes and their location in the UK
  - Figure 2: Comparison of satellite imagery with LiDAR-derived canopy cover
- Key data sources and tools cited
  - Environment Agency National Lidar Programme
  - gblidar (R)
  - ForestTools (R)
  - OS OpenMap Local
  - Welsh Government LiDAR data