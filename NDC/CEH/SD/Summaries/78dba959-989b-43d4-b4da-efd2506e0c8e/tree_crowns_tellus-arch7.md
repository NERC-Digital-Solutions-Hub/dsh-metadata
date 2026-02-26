# Tree canopy data derived from LiDAR data for South West England 2013

## Overview
- High-resolution LiDAR-derived tree canopy dataset for Cornwall and Devon (Tellus South West, July–August 2013).
- Outputs include tree crown polygons and treetop points, suitable for map-based GIS analyses.

## Data Access and Licensing
- Data available at: https://doi.org/10.5283/78dba959-989b-43d4-b4da-efd2506e0c8e
- License: Open Government Licence. By download/usage, you agree to the OGL.
- Acknowledgement: Scholefield, P.; Trembath, P. (2022). Tree canopy data derived from LiDAR data for South West England 2013. NERC EDI Centre.
- Data source and project context: BAS LiDAR collection for Tellus South West; available as OSGB 27700 tiles.

## Data Coverage and Source
- Area: 9,424 km², west of Exmouth (approximately west of 3°21′W).
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
- Inputs: Digital Surface Model (DSM) and Digital Terrain Model (DTM) at ~1 m grid, each with ~25 cm vertical accuracy.
- Tile structure: data provided as individual files for OS grid tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).

## Data Content and Structure
- Outputs:
  - Tree crown polygon layer (crown outlines).
  - Tree top point layer (treetop locations).
  - Stored and delivered as 25 km² geopackages.
- Key attributes (per site):
  - treeID: unique identifier at 1 km scale (not unique across 25 km² tiles).
  - Height: crown height in metres.
  - crownAr: crown area in square metres (integer due to LiDAR resolution).
  - crwnDmt: mean crown diameter (metres).
  - habitat: category (buildings/coastal; forest/woodland/urban greenspace; rural/agricultural).
  - Geometry: points for treetops; polygons for crown outlines.
- Data quality context: includes both hedgerow-related rural features and retained buildings/forests to support broader analysis.

## Methods for Generating Tree Canopy Outlines
- Processing toolkit: Forest Tools R package; inputs required are DSM and DTM.
- Core algorithm:
  - Dynamic (variable) window filter to detect dominant treetops.
  - Window size scales with canopy height to accommodate varying crown sizes.
  - Minimum height threshold: minHeight = 1 m.
- Canopy segmentation:
  - Initially uses the mean canopy width (mcws) with a watershed approach (from imager package) to outline crowns.
  - Marker-controlled segmentation employed to mitigate oversegmentation (Beucher & Meyer, 1993).
  - Crown outlines as polygons require substantial processing time and disk space.
- Feature separation:
  - Rural vs. urban/offshore features filtered using a combined layer (National Forest Inventory, OS Greenspace/Urban Areas, Landcover Map 2007 Littoral).
  - Resulting dataset emphasizes rural features; retaining buildings/forests for analytic flexibility.

## Data Usage and Practical Considerations for GIS Specialists
- Outputs are designed for map-based visualization and spatial analysis in GIS workflows.
- Resolution and accuracy:
  - DSM/DTM at ~1 m, height accuracy ~25 cm.
  - Crown outlines reflect delineated crowns; treetop points provide precise localization for feature mapping.
- File and processing considerations:
  - Crown polygon generation is computationally intensive; plan for processing time and storage.
  - Data are delivered in tile-based geopackages aligned with OS grid tiling.

## Quality Control and Uncertainty
- LiDAR data quality: 2 cm height layers (terrain and surface) at 1 m resolution; average height accuracy ~25 cm.
- Outputs provided “as is” from the delineation model, with rural feature filtering applied.
- Retains buildings and forests to support user-driven analyses.

## References (Key Methods)
- Beucher, Beucher & Meyer (1993): Marker-controlled watershed segmentation.
- Popescu & Wynne (2004): Dynamic window-based treetop detection in canopy height models.
- Ferraccioli et al. (2014): LiDAR-based DSM/DTM for South West England.
- Ferraccioli et al. (2014): Additional DSM/DTM data context for the region.