# Tree canopy data derived from LiDAR data for South West England 2013

## Overview
- Dataset derived from high-resolution LiDAR over Cornwall and Devon (July–August 2013) for the Tellus South West project.
- Produced by the British Antarctic Survey with data processed by the Environment Agency; content includes Digital Terrain Model (DTM) and Digital Surface Model (DSM).
- Aims to provide tree canopy outlines and treetop locations for forested and rural landscapes in South West England, with filtering to separate hedgerows and urban features.

## Licensing and access
- Data available at the provided DOI and licensed under the Open Government Licence.
- Users must acknowledge the dataset by citing: Scholefield, P; Trembath, P. (2022). Tree canopy data derived from LiDAR data for South West England 2013. NERC EDS Environmental Information Data Centre. Dataset. DOI: 10.5283/78dba959-989b-43d4-b4da-efd2506e0c8e.
- By downloading, accessing, or using the data, you agree to the licence terms.

## Provenance and collection details
- Acquisition: BAS collected high-resolution LiDAR (~1 point/meter) with vertical accuracy ~25 cm.
- Timeframe: July–August 2013.
- Area: 9,424 km² west of Exmouth (approximately west of 3°N 21' W).
- Source data: Raw LiDAR converted to DSM and DTM by Environment Agency (contract).
- Coordinate system: OSGB 1936 / British National Grid (EPSG:27700).
- Data outputs are provided as 2 cm height layers (terrain and surface) at 1 m grid resolution.

## Data contents and structure
- Primary outputs:
  - Tree crown polygon layer (crown outlines)
  - Tree top point layer
  - Saved as 25 km² geopackages
- Supporting data:
  - DTM (bare-earth terrain) and DSM (features on bare earth, e.g., vegetation, buildings)
  - Rural feature dataset filtered to emphasize hedgerows and trees; buildings/forests retained for user analysis
  - Non-hedgerow layer created to filter rural vs urban/offshore features using ancillary datasets (Greenspace, Urban Areas, Landcover)
- Data fields (sampled structure):
  - treeID: unique identifier at 1 km scale (not unique for the 25 km² tiles)
  - Height: height of the delineated tree crown (m)
  - crownAr: crown area (m²)
  - crwnDmt: mean crown diameter (m)
  - habitat: category (buildings/coastal, forest/woodland/urban greenspace, or rural/agricultural)
  - Geometry: geometry type (points for treetops, polygons for crowns)

## Methods for generating canopy outlines
- Software: Forest Tools R package; requires DSM and DTM inputs.
- Treetop detection: variable window function; dynamic window size based on canopy height to detect dominant treetops.
- Crown delineation: canopy height model segmentation using the mcws function (watershed-based) with marker-controlled segmentation to reduce oversegmentation.
- Outputs: tree crown polygons and treetop points; generation is computationally intensive and generates 25 km² geopackages.
- Parameter tuning: test-area based adjustment to achieve full crown models (minHeight = 1 m; non-crown classes excluded).

## Quality control and data quality notes
- LIDAR data quality: 2 cm height layers, 1 m grid cells, average height accuracy ~25 cm.
- Data provided “as is” after delineation; rural filtering applied while preserving buildings/forests for context.
- Potential issues: oversegmentation avoided via marker-controlled segmentation; crown outlines require substantial processing time and disk space; some features may still be affected by data density and crown adjacency.
- Metadata supports user-driven analyses with additional contextual layers.

## Use and governance considerations for data stewards
- Licensing and attribution: Open Government Licence; requires citation and acknowledgment in any reuse.
- Versioning and updates: outputs reflect 2013 LiDAR data; guidance needed for future updates or reprocessing with new data.
- Provenance and traceability: clearly documented sources (BAS, Tellus SW, Environment Agency) and references to foundational methods (Popescu & Wynne; Beucher & Meyer; Ferraccioli et al.) to support metadata completeness.
- Data storage and interoperability: data provided in ESRI grid tiles and geopackages; ensure consistent CRS (OSGB 27700) and harmonized file naming to facilitate discovery and reuse.
- Metadata considerations: include collection date, area coverage, data processing steps, data quality notes, and processing software details to support governance and discoverability.

## References
- Beucher, Beucher & Meyer (1993). Morphological approach to segmentation and watershed transformation.
- Popescu, S. C., & Wynne, R. H. (2004). Seeing the trees in the forest.
- Ferraccioli, F. et al. (2014). LiDAR-based DSM/DTM data for South West England. NERC EIDC.