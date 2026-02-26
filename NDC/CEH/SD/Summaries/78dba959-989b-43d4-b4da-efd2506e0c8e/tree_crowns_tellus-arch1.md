# Data access and licensing information

- Data availability: https://doi.org/10.5283/78dba959-989b-43d4-b4da-efd2506e0c8e
- License and acknowledgement: By downloading, accessing or using the data you agree to the Open Government Licence; you must acknowledge use by citing Scholefield, P; Trembath, P. (2022). Tree canopy data derived from LiDAR data for South West England 2013. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5283/78dba959-989b-43d4-b4da-efd2506e0c8e

## Data collection and provenance
- Source: British Antarctic Survey (BAS) collected a high-resolution LiDAR dataset over Cornwall and Devon in July–August 2013 for the Tellus South West project.
- Resolution and accuracy: approximately 1 point per meter; vertical accuracy ~25 cm; 2 cm height layers for terrain and surface; 1 m grid cell resolution.
- Coverage: Digital Terrain Model (DTM) and Digital Surface Model (DSM) covering 9424 km² west of Exmouth (roughly west of 3°21' W).
- Data formats and tiles: provided as individual ESRI grid files representing OS tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).
- Coordinate system: OSGB 1936 / British National Grid (EPSG: 27700).

## Data generation and processing methods
- Inputs: DSM and DTM datasets used to derive canopy height models.
- Tree top detection: using Forest Tools R package with a variable window function; a moving window identifies local maxima as treetops; minimum height threshold set at 1 m.
- Canopy segmentation: watershed-based approach (mcws) to delineate crown outlines; employs marker-controlled segmentation to reduce over-segmentation.
- Output formats: tree crown polygons and tree top points; stored as 25 km² geopackages.
- Filtering: rural feature layer created by combining multiple layers (e.g., National Forest Inventory, Greenspace/Urban Areas, Landcover Map) to separate non-hedgerow features and improve spatial filtering.

## Spatial reference and coverage
- Coordinate system: OSGB 1936 / British National Grid (EPSG: 27700).
- Outputs relate to rural, urban, and coastal contexts within southwest England.

## Data outputs and structure
- Outputs: two primary layers per area — tree crown polygons and tree top points (25 km² geopackages).
- Data units: all heights and distances in metres; areas in square metres.
- Key attributes:
  - treeID: unique identifier (1 km scale; not unique within 25 km² tiles)
  - Height: height of delineated tree crown (m)
  - crownAr: crown area (m²)
  - crwnDmt: mean crown diameter (m)
  - habitat: category (buildings/coastal; forest/woodland/urban greenspace; rural/agricultural)
  - Geometry: point (treetop) or polygon (crown)

## Data quality, caveats, and usability
- Data presented as-is after delineation; rural dataset filtered to emphasize hedgerows and trees, with buildings and forests retained for supplementary analysis.
- Recognizes potential under- or over-segmentation and the need for careful parameter tuning when applying the method to different areas.
- The dataset provides rich secondary information for further analysis, including integration with other land cover and habitat layers.

## Licensing, attribution, and access conditions
- Open Government Licence terms apply; users must acknowledge the dataset with the provided citation.
- The dataset and related materials are documented and accessible via the provided DOI and dataset page.

## References
- Beucher, S., & Meyer, F. (1993). Morphological approach to segmentation via watershed transformation.
- Popescu, S. C., & Wynne, R. H. (2004). Seeing the trees in the forest.
- Ferraccioli, F., et al. (2014). LiDAR-based DSM and DTM data for South West England. NERC EIDC.