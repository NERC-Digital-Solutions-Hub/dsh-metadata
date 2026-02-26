# Landscapes

- Part of the Treescapes STAND project led by the RSPB, focusing on two landscapes: North Pennines & Dales (England) and Elenydd (mid Wales).
- Objective is to identify tree cover and height across these landscapes using LiDAR-derived models to produce canopy metrics for mapping and analysis.

## Data sources and provenance

- England data: DTM and DSM from Environment Agency National LiDAR Programme, accessed via the R package gblidar.
- Wales data: DTM/DSM from Welsh Government LiDAR Cloud Optimized GeoTIFFs, imported into QGIS and clipped to the Elenydd boundary.
- Outputs are designed for reproducibility and subsequent analysis across landscapes.

## Methods and processing

- CHMs created by subtracting DTM from DSM (CHM = DSM − DTM).
- Dominant treetops, height values, and tree crowns computed from CHMs using ForestTools.
- Height threshold: 1.5 m to capture shrubs/scrub while excluding structures (e.g., buildings).
- Buildings removed using OS Local buildings data.
- Calculations performed at 10 m resolution to derive total canopy cover percentage and mean tree height for each landscape.

## Outputs and products

- Canopy cover percentage and mean tree height at 10 m resolution for each landscape.
- Visual comparison (Figure 2) between satellite imagery and LiDAR-derived canopy cover.

## Tools and reproducibility

- R packages: gblidar (data download/access) and ForestTools (tree metrics analysis).
- QGIS used for processing Welsh data clipping and integration with landscape boundaries.
- Clear provenance from data sources to final CHMs and canopy metrics, enabling reproducibility and audit.

## Data governance considerations for Data Stewards

- Provenance and metadata: document data sources, processing steps, thresholds (e.g., 1.5 m), and building removal method.
- Data quality: ensure accurate DTM/DSM alignment, successful exclusion of non-tree features, and validation of canopy metrics.
- Interoperability: use of standard formats (GeoTIFFs, CHMs, 10 m grids) and integration with OS building footprints.
- Access, reuse, and licensing: map data from government sources; clarify licensing and potential embargoes for underlying LiDAR data; provide clear metadata to enable discovery and reuse.
- Updates and versioning: maintain versioned workflows to incorporate updated LiDAR datasets; document any changes to processing parameters.
- Documentation of limitations: acknowledge threshold choice and potential omissions (e.g., very low vegetation, non-vegetated features) and how these affect interpretation.

## References

- EnvironmentAgency. (2023). National Lidar Programme.
- Graham, H. (2023). gblidar: A package to download tiled and point cloud LiDAR data for Great Britain.
- OrdnanceSurvey. (2023). OS OpenMap - Local.
- Plowright, A. (2023). ForestTools: Tools for Analyzing Remote Sensing Forest Data. R package version 1.0.0.
- Syder, A., Baker, S., Bowditch, E., Carlisle, S., Finch, T., Minter, M. & Constant, N. (in prep). Visioning future treescapes in upland landscapes: using deliberative processes to understand values and land-use preferences of local stakeholders.
- WelshGovernment. (2023). LiDAR Welsh Government.