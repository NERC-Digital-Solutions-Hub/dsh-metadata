# Tree canopy data derived from LiDAR data for South West England 2013

## Overview
- High-resolution LiDAR-derived tree canopy dataset for Cornwall and Devon, July–August 2013, as part of the Tellus South West project.
- Covers 9,424 km² west of Exmouth (OSGB 1936 / British National Grid area).
- Outputs include dendritic canopy outlines and treetop locations derived from DSM and DTM data.
- Data available under the Open Government Licence; citation required: Scholefield & Trembath (2022).

## Data collection and scope
- Source: British Antarctic Survey (BAS) collected ~1 point/meter LiDAR with ~25 cm vertical accuracy.
- Conversion to DSM/DTM performed by the Environment Agency.
- Spatial data provided as OS grid tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw) with 1 m grid cells.
- DSM represents surface features; DTM represents bare earth height.
- CRS: OSGB 1936 / EPSG: 27700.

## Methods for generating tree canopy outlines
- Inputs: DSM and DTM; processed with Forest Tools R package.
- Treetop detection: dominant treetops identified using a dynamic window function (variable window filter; based on Popescu & Wynne 2004); minimum canopy height threshold set at 1 m.
- Canopy segmentation: uses a watershed-based approach (mcws) to outline discrete crown shapes; marker-controlled segmentation reduces oversegmentation.
- Outputs: 
  - Tree crown polygons
  - Tree top points
  - Saved as 25 km² geopackages
- Feature filtering: rural vs urban/shoreline features separated using a non-hedgerow layer derived from multiple sources (Forest Research NFI, OS Greenspace and Urban Areas, Landcover Map 2007).
  
## Data structure and content
- Units: metres for heights/distances; square metres for areas.
- Key fields:
  - treeID: unique identifier at 1 km scale (not unique within 25 km² tiles)
  - Height: crown height (m)
  - crownAr: crown area (m²)
  - crwnDmt: mean crown diameter (m)
  - habitat: category (buildings/coastal, forest/woodland/urban greenspace, rural/agricultural)
  - Geometry: point for treetops, polygon for crown outlines

## Data quality and processing notes
- LiDAR data: 2 cm height layers, 1 m resolution, average height accuracy ~25 cm.
- Outputs provided “as is” after delineation; additional context from retained building/forest layers supports secondary analyses.
- Crown outlines may require significant processing time and disk space; marker-controlled segmentation helps mitigate sub-crown segmentation.

## Licensing, access, and citation
- Data accessible via https://doi.org/10.5283/78dba959-989b-43d4-b4da-efd2506e0c8e
- License: Open Government Licence (agreement to terms upon download/access)
- Acknowledge using and citing: Scholefield, P.; Trembath, P. (2022) Tree canopy data derived from LiDAR data for South West England 2013. NERC EIDC.

## Relevance for monitoring environmental health
- Provides standardized, high-resolution canopy metrics enabling temporal/environmental health assessments.
- Facilitates integration with other environmental datasets (e.g., hedgerows, urban greenspace) to enhance cross-cutting monitoring efforts.
- Outputs are readily usable in GIS for mapping canopy extent, crown metrics, and habitat classification across the southwest England region.