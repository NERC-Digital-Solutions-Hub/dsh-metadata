# Landscapes

## Overview
- Part of the Treescapes STAND project led by the RSPB.
- Focus areas: North Pennines & Dales (England) and Elenydd (mid Wales).

## Data Sources and Formats
- English LiDAR data from Environment Agency National LIDAR Programme.
- Wales LiDAR data from Welsh Government LiDAR Cloud Optimized GeoTIFFs.
- Data types involved: DTM (digital terrain model), DSM (digital surface model); derived CHM (canopy height model).

## Processing Workflow
- CHMs created by subtracting DTM from DSM (CHM = DSM − DTM).
- Dominant treetops, height values, and tree crowns derived from CHM using ForestTools in R (functions vwf and mcws) with a 1.5 m height threshold to include shrubs but exclude buildings.
- Building footprints removed using OS OpenMap Local data.
- Datasets analyzed to compute:
  - Total canopy cover percentage
  - Mean tree height
- Resolution for outputs set at 10 m.

## Outputs and Visualization
- Outputs include canopy cover percentage and mean height per landscape at 10 m resolution.
- Figure contrasts satellite imagery with the LiDAR-derived canopy cover.

## Tools, Reproducibility, and Documentation
- Software and packages used:
  - R: gblidar (to access LiDAR tiles), ForestTools (tree metrics extraction)
  - QGIS (for clipping data to the landscape boundary)
- Clear documentation of methods and parameters (e.g., height threshold 1.5 m) supports reproducibility and reuse.

## Scope and Boundaries
- Landscapes covered in this study:
  - North Pennines & Dales (England)
  - Elenydd (mid Wales)

## References
- Environment Agency. National Lidar Programme.
- Graham (2023). gblidar: R package for LiDAR data.
- Ordnance Survey. OS OpenMap - Local.
- Plowright (2023). ForestTools: analyzing remote sensing forest data.
- Syder et al. (in prep). Visioning future treescapes in upland landscapes.
- Welsh Government. LiDAR data resources.