# Supporting documentation for 'National-scale geodatabase of catchment characteristics in the Philippines'

- Purpose and scope
  - Creates a national-scale geodatabase of catchment characteristics to support river management applications in the Philippines.
  - Applies to medium- to large-sized catchments (area > 250 km²) across major island groups (Luzon, Catanduanes, Mindoro, Samar, Leyte, Panay, Palawan, Negros, Bohol, Mindanao).
  - Produces 91 morphometric and topographic attributes along the stream network for 128 catchments.

- Data sources and collection
  - Nationwide IfSAR DEM (5 m resolution; ~300,000 km²) used for consistent vertical accuracy (1 m RMSE).
  - DEM was bilinearly resampled to 10 m for processing.

- Methodology and processing workflow
  - Stream networks and catchments delineated with TopoToolbox V2 using D8 flow directions.
  - Alluvial channels identified with an upstream area threshold of 1 km² to separate debris-flow from alluvial channels.
  - DEM artefacts corrected via constrained regularized smoothing to ensure hydrologically consistent elevations (smoothing factor K = 2; quantile τ = 0.5).
  - Attributes computed at all points along the stream network; density of points is 0.01 km along DEM resolution.
  - Segments aggregated to lengths of 0.05, 0.1, 0.2, and 1 km to generalize local fluctuations.
  - Network is divided into homogeneous reaches bounded by confluences and outlets, ensuring consistent delineation across catchments.
  - 91 morphometric and topographic characteristics extracted, including linear, areal, and relief metrics, plus along-stream slope.

- Outputs and data products
  - GIS data and attribute tables for 128 catchments (catchments_n128) and corresponding stream networks (stream_network_n128).
  - Topographic characteristics dataset (n128) containing 91 attributes; accompanying description and README files detailing units and data types.
  - Example datasets and scripts provided to replicate analyses for a selected catchment (e.g., Tigum) including:
    - Example MATLAB code and topographic data
    - Tigum Catchment shapefile and several derived attribute layers at multiple scales
    - README_Philippines_topographic_processing_example.txt
  - Documentation folder with general overview and data descriptions (README.txt, README_Philippines_GIS_catchments_n128.txt, README_Philippines_topographic_characterstics_n128.csv, etc.).

- Reproducibility and accessibility
  - Interactive online version of the catchment geodatabase available at Glasgow’s ArcGIS web app viewer.
  - MATLAB-based workflow and example data provided to enable replication of the processing steps for a chosen catchment.

- Quality control and validation
  - DEM-derived stream networks visually validated against Google Earth imagery.
  - Consistency checks with the Philippines Hydrologic Dataset (PHD) mappings to ensure alignment with existing hydro-spatial data.

- Documentation and references
  - Detailed methodological references for DEM processing, stream-network delineation, and morphometric analysis (Topotoolbox, D8, smoothing approaches, and morphometric literature).
  - Key sources include demonstrations of DEM smoothing, channel-network representations, and Philippine hydrologic datasets development.

- Practical considerations for analysts
  - The approach emphasizes transparent, reproducible workflows suitable for informing river-management decisions at national to sub-catchment scales.
  - Limitations acknowledged include potential DEM artefacts, scale-dependent attribute calculations, and reliance on consistent access to GIS and MATLAB tooling.
  - The dataset supports exploring correlations between catchment morphometrics and hydrological behavior, enabling predictive assessments for river management actions.