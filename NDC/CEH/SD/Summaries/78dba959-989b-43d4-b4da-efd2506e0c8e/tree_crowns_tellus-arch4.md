# Tree canopy data derived from LiDAR data for South West England 2013

## Overview
- Data license: Open Government Licence; attribution required via the citation provided.
- Dataset DOI: https://doi.org/10.5283/78dba959-989b-43d4-b4da-efd2506e0c8e
- Citation: Scholefield, P; Trembath, P. (2022). Tree canopy data derived from LiDAR data for South West England 2013. NERC EDS Environmental Information Data Centre (Dataset). https://doi.org/10.5283/78dba959-989b-43d4-b4da-efd2506e0c8e
- Purpose: Deliver LiDAR-derived tree canopy information for South West England (2013) to support spatial analysis and decision-making.

## Data collection and provenance
- Source: British Antarctic Survey (BAS) acquired high-resolution LiDAR data over Cornwall and Devon in July–August 2013 for the Tellus South West project.
- Resolution and accuracy: ~1 point per square meter with ~25 cm vertical accuracy.
- Processing: Raw LiDAR converted to Digital Terrain Model (DTM) and Digital Surface Model (DSM) by the Environment Agency contractor.
- Coverage: 9,424 km² area west of Exmouth (approximately west of 3°21′W), represented as ESRI grid tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).
- coordinate system: OSGB 1936 / British National Grid (EPSG:27700).
- Data types: DTM (bare-earth height) and DSM (surface height) layers.

## Data products and processing methods
- Primary tools: Forest Tools R package for DSM/DTM-based analysis.
- Tree top detection: Dynamic window function to identify local maxima in canopy height; window size scales with local canopy height; minimum height threshold of 1 m.
- Crown delineation: Canopy height models segmented into crown outlines using a watershed-based approach (mcws function) with marker-controlled segmentation to reduce oversegmentation.
- Outputs: 
  - Tree crown polygon layer
  - Tree top point layer
  - Both saved as 25 km² geopackages
- Feature filtering: Non-hedgerow areas (rural features) separated from urban/shoreline features using LiDAR-derived data plus Greenspace and Urban Areas, and Landcover Map 2007 layers to create a rural-only mask.
- Processing considerations: Crown delineation can be computationally intensive in terms of time and disk space.

## Nature and units of recorded values
- Units: metres for heights and distances; square metres for areas.
- Data outputs include height of delineated crowns, crown area, mean crown diameter, and geometric representation (points for treetops; polygons for crowns).

## Data structure and contents
- Key fields:
  - treeID: unique identifier at 1 km scale (not unique for 25 km² tiles)
  - Height: height of the delineated crown (m)
  - crownAr: crown area (m²)
  - crwnDmt: mean crown diameter (m)
  - habitat: category (buildings/coastal; forest/woodland/urban greenspace; rural/agricultural)
  - Geometry: geometry type (points for treetops; polygons for crown areas)

## Quality control and data characteristics
- LiDAR data specifics: 2 cm height layers, 1 m grid cell resolution, ~25 cm height accuracy.
- Dataset scope: filtered to provide rural feature extents; buildings and forests retained to support user analyses.
- Output characteristics: as-generated data with accompanying rural/hedgerow context for interpretation.

## Notes on data access and attribution
- Access: data available via the provided DOI and license terms.
- Usage note: users must acknowledge the dataset and cite the provided reference to ensure proper attribution and traceability.

## References (methods and context)
- Beucher, D. & Meyer, 1993. Morphological approach to segmentation and watershed transformation.
- Popescu, S. C., & Wynne, R. H., 2004. Seeing the trees in the forest (watershed-based crown delineation).
- Ferraccioli, F. et al., 2014. LiDAR-based DSM and DTM data for South West England. NERC EIDC.