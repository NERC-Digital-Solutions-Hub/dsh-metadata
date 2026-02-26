# Supporting documentation for 'National-scale geodatabase of catchment characteristics in the Philippines'

## Overview
- Nationwide geodatabase of catchment characteristics for river management applications.
- Systematic workflow applied to 128 catchments (catchment area > 250 km2) across major Philippine island groups (Luzon, Catanduanes, Mindoro, Samar, Leyte, Panay, Palawan, Negros, Bohol, Mindanao).
- An interactive version of the catchment geodatabase is available online.
- Example MATLAB code and topographic data provided to replicate the workflow for a selected catchment.

## Data sources and collection
- Uses a nationwide IfSAR Digital Elevation Model (DEM) at 5 m spatial resolution (2013 data) with ~1 m RMSE vertical accuracy.
- DEM was bilinearly resampled to 10 m for analysis due to computational constraints.
- Data quality checked against Google Earth imagery and existing Philippine Hydrologic Dataset (PHD) mappings.

## Stream networks and catchment delineation
- TopoToolbox V2 used to delineate stream networks and catchments with D8 flow direction.
- Upstream area threshold of 1 km2 employed to delineate alluvial channels within the stream network.
- Hydrologically consistent DEM achieved via constrained regularized smoothing (K = 2; quantile τ = 0.5) to reduce artefacts.
- Stream network points (0.01 km spacing) were aggregated along river segments to generalize local fluctuations.

## Morphometric and topographic characteristics
- Extracted 91 attributes per point along the stream network, forming linear, areal, and relief characteristics, including slope, drainage area, stream order, elevation, and distance to outlet.
- Points aggregated into homogeneous reaches with segment lengths of 0.05, 0.1, 0.2, and 1 km to produce consistent representations across catchments.

## Outputs and data structure
- Data products include:
  - Philippines_GIS_catchments_n128.shp
  - Philippines_GIS_stream_network_n128.shp
  - Philippines_topographic_characterstics_n128.csv
  - Philippines_topographic_characterstics_description.csv
  - README files and a topographic processing example folder (Example_Tigum_Catchment_Processing.txt, etc.)
- Documentation and metadata provided via README_Philippines_GIS_catchments_n128.txt and related files.
- An interactive web app viewer is provided at glasgowuni.maps.arcgis.com with a dedicated project ID.

## Reproducibility and methodology
- Workflow applied consistently across all 128 catchments to enable comparable analyses.
- Example workflow and data to replicate are contained in the Philippines_topographic_processing_example folder, including MATLAB code and sample outputs for the Tigum catchment.

## Quality assurance and validation
- Stream-network positions visually aligned with Google Earth imagery and closely matched PHD-mapped networks, supporting reliability of delineations and characteristics.

## Relevance for monitoring frameworks
- Provides a standardized, transparent dataset of catchment morphometrics and topographic characteristics suitable for environmental health monitoring and river-management decision-making.
- Emphasizes reproducibility, metadata availability, and data accessibility (including sharing of underlying data and reproducible processing steps), addressing common monitoring framework challenges such as data gaps, metadata inadequacies, and the need for transparent data governance.

## References
- Key methodological and data-source references underpinning the workflow and data products (e.g., IfSAR DEM acquisition, TopoToolbox usage, channel-network representation from DEMs, smoothing techniques, morphometric analyses, and the Philippine Hydrologic Dataset development).