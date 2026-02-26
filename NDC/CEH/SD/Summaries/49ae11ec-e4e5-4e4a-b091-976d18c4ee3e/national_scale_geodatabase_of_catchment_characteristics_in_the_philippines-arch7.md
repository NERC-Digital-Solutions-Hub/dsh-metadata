# National-scale geodatabase of catchment characteristics in the Philippines for river management applications

## Overview
- Documentation of a nationwide geodatabase describing catchment characteristics for river management in the Philippines.
- Generated from a 2013 5 m IfSAR DEM, resampled to 10 m for processing to balance accuracy with computational constraints.
- Workflow produces 128 catchments (>250 km2) spanning multiple islands; aims to support hydrological and geomorphological river management analyses.

## Data collection and processing workflow
- Elevation data and stream networks
  - DEM: IfSAR DEM with 5 m resolution; downstream hydrological consistency improved via constrained regularized smoothing (K = 2; tau = 0.5).
  - Flow routing: TopoToolbox V2 with D8 algorithm to derive flow direction and accumulation.
  - Alluvial channel delineation uses an upstream-area threshold of 1 km2.
- Stream network and catchment delineation
  - Stream network corrected for artefacts to ensure hydrologically plausible elevations downstream.
  - Stream network points are densely spaced (0.01 km) and aggregated along river segments to generalize local fluctuations.
  - Segmentation yields homogeneous reaches at 0.05, 0.1, 0.2, and 1 km lengths; segments distributed between confluences, between confluences and outlets, and between confluences and heads.
- Attributes and morphometrics
  - Extracted attributes at network points: elevation, drainage area, stream slope, stream order, distance from outlet.
  - Derived 91 morphometric and topographic characteristics (linear, areal, relief, and slope metrics along the stream network).
  - Emphasis on characteristics with broad applicability to hydrological and geomorphological applications.
- Study scope and reproducibility
  - Applied workflow to 128 catchments across major Philippine island groups (Luzon, Catanduanes, Mindoro, Samar, Leyte, Panay, Palawan, Negros, Bohol, Mindanao).
  - Example MATLAB code and topographic data provided to replicate processing for a selected catchment (Tigum).

## Data products and structure
- Core datasets (GIS)
  - Philippines_GIS_catchments_n128.shp with catchment characteristics.
  - Philippines_GIS_stream_network_n128.shp with stream network characteristics.
  - Philippines_topographic_characterstics_n128.csv containing 91 morphometric/topographic values.
- Documentation and descriptions
  - README.txt: general overview of all datasets.
  - README_Philippines_GIS_catchments_n128.txt
  - README_Philippines_GIS_stream_network_n128.txt
  - Philippines_topographic_characterstics_description.csv
  - README_Philippines_topographic_characterstics_n128.txt
- Reproducibility resources
  - Philippines_topographic_processing_example folder with example Tigum catchment processing files, including MATLAB scripts and several shapefiles (e.g., Tigum_10m_DEM.tif, Tigum_Catchment.shp, Tigum_Stream_Network_10m_D_A_G_SO_ELV_*.shp).
  - Example_Tigum_*.txt providing workflow steps and outputs.
- Additional context
  - An interactive online version of the catchment geodatabase is available via a provided ArcGIS Online link.

## Quality control and validation
- DEM-derived stream networks qualitatively align with Google Earth imagery and are consistent with the Philippine Hydrologic Dataset (PHD) stream networks, indicating reliable spatial positioning.

## Usage, scope, and applications
- Data products support river management by providing standardized catchment and stream-network characteristics suitable for hydrological and geomorphological analyses.
- The 128 catchments cover medium- to large-sized basins, enabling regional assessments and comparisons.
- Morphometric attributes are designed to be broadly applicable across similar river-management contexts.

## Reproducibility and access
- MATLAB and TopoToolbox V2 are used for processing, with explicit example datasets and code provided to enable replication for other catchments.
- Interactive online version of the geodatabase facilitates exploration by stakeholders and end-users.

## References and provenance
- Key methodological and software references include:
  - TopoToolbox 2 (MATLAB-based) for topographic analysis.
  - Established channel-network representation methods using digital elevation models.
  - Literature on smoothing and uncertainty in river profiles.
  - Philippine Hydrologic Dataset (PHD) development and RS-based water-resource inventories.
- These references underpin the data processing choices, attribute selection, and validation approaches.