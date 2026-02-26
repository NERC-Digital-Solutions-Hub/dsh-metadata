# Woody habitat corridor data in South West England

## Overview
- Polylines depicting non-woodland linear tree and shrub features in Cornwall and much of Devon.
- Derived from lidar data collected by the Tellus South West project, combined with open-source GIS datasets to map woody vegetation corridors.

## Access and Citation
- Open Government Licence data availability.
- DOI: https://doi.org/10.5285/4b5680d9-fdbc-40c0-96a1-4c022185303f
- Citation: Broughton, R.K.; Gerard, F.; Haslam, R.; Howard, A.S. (2017). Woody habitat corridor data in South West England. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/4b5680d9-fdbc-40c0-96a1-4c022185303f

## Background
- Habitat corridors (hedgerows, tree lines) are important habitats and dispersal pathways in lowland Britain.
- Mapping location, extent, and height of woody features has been challenging; this dataset uses lidar plus existing open datasets to map non-woodland linear woody features.

## Method
- Processing steps to produce the dataset:
  - Create canopy height model (CHM) by subtracting the digital terrain model (DTM) from the digital surface model (DSM); discard features below 1 m.
  - Mask woodland parcels (Forest Commission data) and buildings (OS VectorMap District/OpenMap Local with a 5 m buffer).
  - Classify features above 1 m into height classes:
    - Class 1: 1 – 1.4999 m (low hedges, shrubs)
    - Class 2: 1.5 – 2.9999 m
    - Class 3: 3 – 5.9999 m
    - Class 6: 6 – 50 m (hedgerow and non-woodland trees)
    - NoData for other heights
  - Filter out small features (Class 1–3 areas < 20 m²; Class 6 areas < 10 m²) by assigning to surrounding dominant values.
  - Manual QA to remove anomalies (glassed houses, unmapped buildings, vehicles, caravan parks, solar farms).
  - Generate centre lines to produce polyline output of woody corridors.
  - Tile the dataset into 20 x 20 km shapefiles, coded by the bottom-left 10 km hectad name.
- Data sources and validation:
  - Lidar data from July/August 2013; ground truthing in Nov 2018 (1 km² SX7485).
  - 164 ground truth height values mapped to height classes; comparison with modelled classes; adjusted accuracy calculation.

## Quality control and limitations
- Not an exhaustive error check; extensive manual checks reduce obvious issues, but some errors remain (e.g., coastal misclassification within 50 m of high tide line).
- Tall crops may be misclassified as low scrub; irregular patches of trees/scrub can produce overly dense or sparse polylines.
- Ground truthing occurred five years after lidar data; hedges are typically long-term assets, so class stability is assumed.

## Data structure and description
- Output: shapefile polyline tiles (20 x 20 km).
- Fields:
  - SHAPE: Geometry (polyline)
  - GRIDCODE: Height class code for each polyline feature
  - LENGTH: Length of polyline feature in metres

## Usage notes for GIS visualization
- Height classes function as proxies for hedge/tree height, useful for visualization and corridor analysis.
- Be mindful of coastal and land-use misclassifications; consider QA in coastal regions.
- Tiled format supports performance when working with large extents.

## References
- OS Open Map Local; OS VectorMap District (Crown copyright, 2015).
- Forestry Commission National Forest Inventory Great Britain 2015 (Open Government Licence v3.0).
- Ferraccioli, F. et al. (2014). LiDAR-based DSM for South West England; Ferraccioli, F. et al. (2014). LiDAR-based DTM for South West England. NERC EIDC.