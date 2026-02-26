# Landscapes

- The two landscapes are part of the Treescapes STAND project, led by the RSPB: North Pennines & Dales (England) and Elenydd (mid Wales).

## Overview
- STAND focal landscapes explored for tree cover and height using LiDAR-derived products to understand treescapes in upland areas.
- Outputs include comparisons with satellite imagery and spatial metrics at a 10 m resolution.

## Data sources
- England: Environment Agency National LiDAR Programme data; accessed via the R package gblidar.
- Wales: Welsh Government LiDAR Cloud Optimized GeoTIFFs (2020–22); imported into QGIS and clipped to the Elenydd boundary.

## Methods
- Compute canopy height models (CHMs) as DSM minus DTM.
- Derive dominant treetops, height values, and tree crowns from CHMs using ForestTools (functions vwf and mcws) with a 1.5 m height threshold.
  - Purpose of 1.5 m threshold: include shrubs/scrub, exclude buildings (verified against OS local buildings data).
- Remove buildings from analysis using Ordnance Survey Local data.
- Calculate total canopy cover percentage and mean tree height for each landscape at 10 m resolution.

## Outputs
- Figure 2: Visual comparison between satellite imagery of woodlands/trees and LiDAR-derived canopy cover.
- Key metrics produced: canopy cover percentage and mean height per landscape at 10 m resolution.

## Landscapes covered
- North Pennines & Dales (England)
- Elenydd (mid Wales)

## Tools and software
- R packages: gblidar, ForestTools
- QGIS for clipping Welsh LiDAR data
- OS OpenMap - Local data for building removal

## References (selected)
- Environment Agency. National LiDAR Programme
- Graham, H. gblidar package
- Ordnance Survey. OS OpenMap - Local
- Plowright, A. ForestTools
- Welsh Government LiDAR data