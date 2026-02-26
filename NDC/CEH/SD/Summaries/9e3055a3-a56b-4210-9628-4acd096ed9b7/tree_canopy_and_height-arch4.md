# Landscapes

- The Land Scapes landscapes are part of the Treescapes STAND project led by the RSPB, focusing on the North Pennines & Dales in England and the Elenydd in mid Wales.

## Context and Objective
- Objective: identify tree cover and height across the two focal landscapes to support understanding of treescape structure and changes.
- Landscapes span cross-border regions (England and Wales) and are used to inform landscape-scale treescape assessments.

## Data Sources and Access
- LiDAR-derived data for England from Environment Agency National LiDAR Programme (DTM/DSM).
- LiDAR data for Wales from Welsh Government LiDAR Cloud Optimized GeoTIFFs (2020–2022).
- Building removal and feature filtering using OS OpenMap Local data (Ordnance Survey).
- All data are sourced from public datasets and compiled to support canopy analyses.

## Methods and Processing Pipeline
- CHM creation: canopy height models generated as DSM minus DTM.
- Software and packages:
  - R with gblidar to download and handle GB LiDAR data.
  - ForestTools in R to derive dominant treetops, height values, and tree crowns.
  - QGIS for processing Welsh LiDAR data and boundary clipping to the Elenydd landscape.
- Key parameters:
  - Height threshold of 1.5 m to capture shrubs/scrub while excluding buildings.
  - Buildings removed using OS data to avoid misclassifying structures as canopy.
- Outputs are computed at 10 m resolution for both landscapes (total canopy cover percentage and mean tree height).

## Outputs and Visualization
- Generated CHMs and derived metrics (dominant treetops, canopy cover %, mean height).
- Figure 2 provides a comparison between satellite imagery and LiDAR-derived canopy cover.

## Data Quality, Challenges, and Limitations
- Challenges include:
  - Capturing short vegetation due to threshold settings.
  - Data availability and heterogeneity between England and Wales LiDAR datasets.
  - Potential misclassification if buildings or non-vegetation features are not fully filtered.
- Limitations related to cross-border data compatibility and 10 m resolution granularity.

## Reproducibility, Tools, and Governance
- Reproducibility aided by explicit toolchain and package references (R: gblidar, ForestTools; QGIS).
- Data governance aspects include using public LiDAR sources and OS building data to ensure accurate filtering and canopy estimation.
- Clear documentation of processing steps supports future updates and cross-site comparisons.

## References
- Environment Agency. National LiDAR Programme.
- Graham, H. gblidar R package.
- Ordnance Survey. OS OpenMap - Local.
- Plowright, A. ForestTools R package.
- Syder et al. Visioning future treescapes in upland landscapes (in prep).
- Welsh Government LiDAR data and resources.