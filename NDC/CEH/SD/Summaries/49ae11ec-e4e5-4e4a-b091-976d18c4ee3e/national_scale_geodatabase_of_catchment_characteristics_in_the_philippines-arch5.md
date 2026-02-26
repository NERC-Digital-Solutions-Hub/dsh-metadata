# National-scale geodatabase of catchment characteristics in the Philippines for river management applications

- Purpose: Provide a national-scale geodatabase of catchment characteristics to support river management applications in the Philippines, with standardized, reusable datasets and documented workflows.

## Data sources and collection

- Primary data: nationwide IfSAR digital elevation model (DEM) from 2013 with 5 m spatial resolution and ~300,000 km2 coverage; vertical accuracy ~1 m RMSE.
- Downsampling: DEM bilinearly resampled to 10 m resolution due to computational constraints.
- Stream and catchment delineation: TopoToolbox v2 with D8 flow routing to derive flow direction, flow accumulation, and drainage basins.
- Channel definition: upstream area threshold of 1 km2 to delineate alluvial channels; artefact/pattern damping to ensure hydrologically consistent DEM.

## Processing workflow and standards

- Homogeneous reaches: stream network segmented into reaches (0.05, 0.1, 0.2, and 1 km) to smooth local fluctuations and generalize attributes.
- Attributes derived: 91 morphometric and topographic characteristics (linear, areal, relief, and along-network slope) along the stream network.
- Output granularity: consistent delineation method across all catchments; attributes calculated at densely spaced stream points, then aggregated to defined reach lengths.
- Catchment scope: 128 catchments with area > 250 km2, covering Luzon, Catanduanes, Mindoro, Samar, Leyte, Panay, Palawan, Negros, Bohol, and Mindanao.

## Data products and structure

- Data products:
  - Philippines_GIS_catchments_n128.shp with catchment characteristics
  - Philippines_GIS_stream_network_n128.shp with stream network characteristics
  - Philippines_topographic_characterstics_n128.csv with 91 morphometric/topographic metrics
  - Philippines_topographic_characterstics_description.csv detailing metrics
  - Example_Tigum_Catchment_Processing.txt, Example_Tigum_Stream_Network_Processing.txt, Tigum_*.shp and related files for a replication example
- Documentation: README_Philippines_GIS_catchments_n128.txt, README_Philippines_GIS_stream_network_n128.txt, README_Philippines_topographic_characterstics_n128, and other descriptive READMEs outlining data structure, units, and usage.
- Replication resources: Example MATLAB code and topographic data provided in the Philippines_topographic_processing_example folder to reproduce the workflow for a selected catchment.

## Quality control and validation

- Visual validation: DEM-derived stream networks aligned with Google Earth imagery and consistent with the Philippine Hydrologic Dataset (PHD) stream mapping.
- Artefact mitigation: constrained regularized smoothing (parameters: K = 2; quantile τ = 0.5) to reduce DEM artefacts and ensure downstream elevation consistency.
- Data integrity: 91 attributes and 128 catchments prepared with systematic, reproducible methods; documentation included for nature and units of recorded values.

## Replication, access, and documentation

- Reproducibility: complete workflow described; MATLAB-based tools and example files enable replication of analyses for any selected catchment.
- Access: datasets, GIS shapefiles, CSVs, and processing examples are provided with extensive READMEs and metadata to facilitate discovery and reuse.
- Online mapping: interactive version of the catchment geodatabase available at an ArcGIS web app viewer.

## Geographic scope and coverage

- National-scale coverage across major Philippine islands, focusing on medium- to large-sized catchments (areas > 250 km2).
- Spatial focus supports river management applications at scales relevant to watershed planning and hydrologic/resource management.

## Governance considerations and data stewardship implications

- Standardization: uniform methodology across all catchments supports consistent data governance, interoperability, and metadata quality.
- Metadata and documentation: thorough READMEs and data descriptions enable clear data lineage, usage constraints, and attribute interpretation.
- Data availability and reuse: openly documented workflows and reproducible code enhance discoverability and reuse by data creators, managers, and users.
- Limitations and caveats: DEM-derived results depend on initial data quality (5 m IfSAR DEM) and processing choices (downsampling, smoothing, and threshold values); users should consider these when applying the dataset to new contexts.
- Update and maintenance: framework supports future updates or expansion to additional catchments with the same standardized processing approach.

## Relevance for Data Stewards

- Provides a governance-ready, well-documented, and reproducible workflow for building national-scale hydromorphometric databases.
- Demonstrates robust data quality practices, explicit metadata, and tooling that facilitate sharing, interoperability, and ongoing maintenance across large dataset inventories.