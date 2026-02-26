# Supporting documentation for 'National-scale geodatabase of catchment characteristics in the Philippines'

## Overview
- Develops a national-scale geodatabase of catchment characteristics for river management in the Philippines.
- Based on a nationwide IfSAR DEM (2013) at 5 m resolution, resampled to 10 m for processing.
- Applied a reproducible workflow to 128 catchments (>250 km2) across multiple island groups (Luzon, Catanduanes, Mindoro, Samar, Leyte, Panay, Palawan, Negros, Bohol, Mindanao).
- Delineated stream networks and catchments using TopoToolbox v2 with D8 flow routing; identified alluvial channels using an upstream area threshold of 1 km2.
- Addressed DEM artefacts with constrained regularized smoothing to ensure hydrologically consistent DEMs.

## Data and methods
- Stream network and catchment delineation:
  - Flow routing via D8; stream network points spaced at 0.01 km (DEM resolution).
  - Aggregated attributes along streams at 0.05, 0.1, 0.2, and 1 km segment lengths to generalize local fluctuations.
  - Segmentation creates homogeneous reaches distributed between confluences, outlets, and channel heads.
- Morphometric and topographic characteristics:
  - 91 attributes extracted per catchment, including linear, areal, and relief metrics, plus along-network slope metrics.
  - Attributes chosen for broad applicability to river management in the Philippines; methodology aligned with established hydrological/geomorphological practices.
- Quality control and data integrity:
  - DEM-derived streams visually validated against Google Earth imagery and Philippine Hydrologic Dataset (PHD) networks.
  - Smoothing parameters (K = 2; τ = 0.5) used to mitigate DEM artefacts and ensure plausible stream profiles.

## Outputs and data structure
- Data products produced for 128 catchments:
  - Philippines_GIS_catchments_n128.shp with catchment boundaries.
  - Philippines_GIS_stream_network_n128.shp with stream network attributes.
  - Philippines_topographic_characterstics_n128.csv containing 91 morphometric/topographic metrics per catchment.
  - Descriptive readmes and a description CSV (Philippines_topographic_characterstics_description.csv).
  - A topographic processing example set (Example_Tigum_Catchment_Processing.txt, etc.) with supporting TIGUM catchment data and scripts.
- Interactive access:
  - An online interactive version of the catchment geodatabase is available at Glasgow University’s ArcGIS web app viewer.

## Reproducibility, usage, and accessibility
- Example MATLAB code and topographic data provided to replicate the workflow for a selected catchment (e.g., Tigum).
- Documentation and data designed to enable end users to self-serve analyses, reuse outputs, and adapt workflows for other regions or datasets.
- Data structure supports integration with other GIS and analysis tools and can inform river management decisions, planning, and policy discussions.

## Applications and implications
- Purpose-built to support river management applications and policy work in the Philippines by offering a standardized, scalable set of catchment characteristics.
- Facilitates cross-catchment comparisons and data-driven decision making for water resources, flood risk assessment, erosion control, and other hydrological analyses.
- Encourages broader data creation and sharing practices to improve data-driven governance.

## Notes and references
- Technical choices and workflow steps are grounded in established literature on: TopoToolbox usage, channel network extraction from DEMs, morphometric analysis, and prior Philippine hydrological data efforts (PHD, LiDAR-based datasets).
- Key references provided for data provenance and methodological context, supporting reuse and methodological transparency.