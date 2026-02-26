# National-scale geodatabase of catchment characteristics in the Philippines for river management applications

- Purpose: Create a nationwide geodatabase of catchment characteristics to support river management applications, enabling standardized analysis and cross-catchment comparisons at scale.
- Scope: Applied workflow to 128 medium-to-large catchments (catchment area > 250 km²) across major Philippine island groups (Luzon, Catanduanes, Mindoro, Samar, Leyte, Panay, Palawan, Negros, Bohol, Mindanao).

## Data sources and processing infrastructure

- Primary data: nationwide IfSAR digital elevation model (DEM) from 2013, at 5 m spatial resolution, covering ~300,000 km² with ~1 m RMSE vertical accuracy.
- Resolution adjustment: 5 m DEM bilinearly resampled to 10 m for computational efficiency.
- software: TopoToolbox V2 for stream network delineation and morphometric calculations; D8 flow-direction algorithm used for routing.

## Methods and workflow

- Stream and catchment delineation:
  - Hydrologically consistent stream network created; downstream-decreasing elevations enforced via constrained regularized smoothing (K = 2; τ = 0.5) to minimise DEM artefacts.
  - Upstream area threshold set to 1 km² to distinguish alluvial channels within the network.
- Attribute extraction:
  - Calculated 91 morphometric and topographic characteristics along the stream network, including linear, areal, relief, and slope metrics.
  - Attributes gathered at densely spaced stream points (0.01 km); aggregated along river segments to generalize local variations using segment lengths of 0.05, 0.1, 0.2, and 1 km.
  - River segments categorized between confluences, confluences/outlets, and confluences/headwaters to create homogeneous reaches.
- Outputs:
  - Comprehensive set of 91 characteristics for each catchment.
  - Documentation and replication resources provided (example MATLAB code and topographic data in a dedicated folder).

## Data products and access

- Geographic data:
  - Philippines_GIS_catchments_n128.shp with catchment characteristics.
  - Philippines_GIS_stream_network_n128.shp with stream network characteristics.
- Topographic data:
  - Philippines_topographic_characterstics_n128.csv and accompanying description CSV.
- Documentation and replication:
  - README and detailed files describing data structures and units.
  - Philippines_topographic_processing_example folder containing example scripts, Tigum catchment data, and DEM/SHPs to replicate analyses.
- Interactive access:
  - Online interactive geodatabase viewer: https://glasgowuni.maps.arcgis.com/apps/webappviewer/index.html?id=a88b9ca0919f4400881eab4a26370cee.

## Data structure and guidance

- Provided files and descriptions:
  - General overview: README.txt
  - Catchments: Philippines_GIS_catchments_n128.shp; README_Philippines_GIS_catchments_n128.txt
  - Stream network: Philippines_GIS_stream_network_n128.shp; README_Philippines_GIS_stream_network_n128.txt
  - Topographic characteristics: Philippines_topographic_characterstics_n128.csv; Philippines_topographic_characterstics_description.csv; README_Philippines_topographic_characterstics_n128.txt
  - Processing example: Example_Tigum_Catchment_Processing.txt; Example_Tigum_Stream_Network_Processing.txt; Tigum_10m_DEM.tif; Tigum_Catchment.shp; multiple Tigum network files; README_Philippines_topographic_processing_example.txt

## Quality assurance and validation

- Visual validation: DEM-derived stream networks align well with Google Earth imagery and closely match networks mapped by the Philippine Hydrologic Dataset programs.
- Consistency checks: Methods and outputs designed to be reproducible across all 128 catchments with standardized processing steps.

## Reproducibility and use considerations

- Reproducibility: MATLAB-based workflow and example datasets provided to replicate the analyses for a selected catchment.
- Intended use: Enable consistent, repeatable monitoring of catchment morphometry and hydrological characteristics at a national scale to inform river management decisions and policy evaluations.
- Data accessibility: Datasets and interactive viewer facilitate access for researchers, policymakers, and managers; emphasis on broader data reuse beyond the original study.

## Context and references

- Key methodological and data sources cited, including:
  - TopoToolbox 2 and stream network delineation references
  - Morphometric analysis literature
  - Philippine Hydrologic Dataset (PHD) and related RS-based water resources inventories
- References provide foundational context for the processing choices and validation approaches used in building the geodatabase.