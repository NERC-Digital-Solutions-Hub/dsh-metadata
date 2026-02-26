# National-scale geodatabase of catchment characteristics in the Philippines for river management applications

## Overview
- Nationwide geodatabase developed for river management applications, focusing on catchment characteristics.
- Applied to 128 catchments with areas greater than 250 km², spanning major Philippine island groups (Luzon, Catanduanes, Mindoro, Samar, Leyte, Panay, Palawan, Negros, Bohol, Mindanao).

## Data sources and processing workflow
- Data source: IfSAR digital elevation model (DEM) from 2013, 5 m resolution, covering ~300,000 km²; vertical accuracy ~1 m RMSE.
- Processing: DEM resampled to 10 m due to computational constraints.
- Stream and catchment delineation: TopoToolbox V2 with D8 flow routing; upstream-area threshold of 1 km² to delineate alluvial channels.
- DEM artefacts addressed: downstream elevation monotonicity ensured and hydrologically corrected via constrained regularized smoothing (K = 2; quantile τ = 0.5).
- Attribute extraction: 91 morphometric and topographic characteristics calculated along the stream network (linear, areal, relief, and slope metrics).
- Stream network segmentation: homogeneous reaches created by aggregating points over river segment lengths of 0.05, 0.1, 0.2, and 1 km.
- Spatial sampling: network points spaced at 0.01 km (10 m) along the network.
- Reproducibility: Example MATLAB code and topographic data provided to replicate workflow for a selected catchment.

## Data products and structure
- Philippines_GIS_catchments_n128.shp with catchment characteristics.
- Philippines_GIS_stream_network_n128.shp with stream network characteristics.
- Philippines_topographic_characterstics_n128.csv and corresponding description CSV (detailed 91 characteristics).
- Philippines_topographic_processing_example folder containing: Example_Tigum_Catchment_Processing.txt, Example_Tigum_Stream_Network_Processing.txt, TIGUM_10m_DEM.tif, TIGUM_Catchment.shp, and related shapefiles.
- README files describing datasets and data structure.
- Interactive version available online: Glasgow-based map viewer link.

## Data quality and validation
- Visual validation shows DEM-derived streams align with Google Earth imagery.
- Streams are in close agreement with the Philippine Hydrologic Dataset (PHD) mappings.

## Reproducibility and access
- Workflow implemented in MATLAB using TopoToolbox; detailed example provided to replicate analyses.
- Comprehensive metadata and file descriptions accompany the datasets to support reuse and integration.

## Geographic coverage and scope
- Focused on medium- to large-sized catchments across multiple islands, ensuring nationally consistent hydromorphometric data for river management applications.

## Implications for Data Leaders
- Demonstrates a scalable, reproducible approach to building national-scale hydromorphometric data assets.
- Highlights the importance of data quality controls (artefact correction, validation against external datasets) and clear metadata.
- Supports co-ownership and collaboration by providing accessible data products and an interactive online version.
- Can inform data-gap prioritization by cataloguing 91 attributes and identifying coverage limitations (e.g., emphasis on larger catchments; need for ongoing updates and potential expansion to smaller catchments).