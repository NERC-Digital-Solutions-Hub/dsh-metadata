# Landscapes

- The two landscapes are part of the Treescapes STAND project, led by the RSPB: North Pennines & Dales in England, and Elenydd in mid Wales.
- Aim in this work: identify tree cover and height across landscapes using LiDAR-derived data to create canopy height models (CHMs) and derive metrics of canopy structure.

## Data sources

- England (North Pennines & Dales): Environment Agency National LiDAR Programme data accessed via the R package gblidar.
- Wales (Elenydd): Welsh Government 2020–22 LiDAR Cloud Optimized GeoTIFFs imported into QGIS and clipped to the Elenydd boundary.
- Supporting reference data: OS local buildings data used to remove building features from tree-top analyses.

## Methods (data processing workflow)

- CHMs created by subtracting the DTM from the DSM (CHM = DSM − DTM).
- Dominant treetops, height values, and tree crowns extracted from CHMs using ForestTools in R (functions vwf and mcws) with a 1.5 m height threshold to include shrubs/scrub while excluding built structures.
- Building features removed to avoid confounding canopy measurements.
- Metrics computed per landscape:
  - Total canopy cover percentage
  - Mean tree height
- Outputs produced at 10 m resolution.

## Outputs and visuals

- Figure 2 illustrates the comparison between satellite imagery of woodlands/trees and the LiDAR-derived canopy cover.
- The study provides spatially explicit canopy cover and height data to inform landscape-scale assessments.

## References and data sources

- Environment Agency, National LiDAR Programme
- Graham, H. gblidar R package
- OrdnanceSurvey, OS OpenMap Local
- Plowright, A. ForestTools R package
- Welsh Government LiDAR data
- Syder et al. (in prep) on deliberative landscape visioning (contextual reference)