# Landscapes

- The Landscapes are part of the Treescapes STAND project led by the RSPB, spanning:
  - North Pennines & Dales landscape, England
  - Elenydd landscape, mid Wales

## Aim and approach
- Identify tree cover and height across both landscapes using LiDAR-derived DTM and DSM to create canopy height models (CHMs).
- Compute dominant treetops, heights, and tree crowns from CHMs, with a height threshold of 1.5 m to include shrub/scrub while excluding built features.

## Data sources
- England:
  - Environment Agency National LiDAR Programme
  - Accessed via R package gblidar
- Wales (Elenydd):
  - Welsh Government LiDAR Cloud Optimized GeoTIFFs
  - Imported into QGIS and clipped to the Elenydd boundary
- Buildings:
  - OS Local buildings data used to remove buildings from treetop and crown data

## Processing workflow
- Create CHMs by CHM = DSM − DTM
- Generate dominant treetops, height values, and tree crowns from CHMs using ForestTools
  - Functions: vwf and mcws
- Exclude non-tree features by removing buildings
- Resample/aggregate outputs to 10 m resolution

## Outputs and metrics
- Total canopy cover percentage by landscape
- Mean tree height by landscape
- Outputs produced at 10 m resolution for both landscapes

## Output reference materials
- Figure 2 illustrates comparison between satellite imagery of woodlands/trees and LiDAR-derived canopy cover

## Data sources and references
- Environment Agency. National LiDAR Programme
- Graham, H. gblidar R package
- Ordnance Survey OS OpenMap Local
- Plowright, A. ForestTools R package
- Welsh Government LiDAR data
- Syder et al. (in prep) on future treescapes (values and land-use context)