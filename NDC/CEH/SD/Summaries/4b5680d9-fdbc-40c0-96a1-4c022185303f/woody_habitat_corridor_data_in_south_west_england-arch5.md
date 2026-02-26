# Woody habitat corridor data in South West England

## Overview
- Polylines depicting non-woodland linear tree and shrub features in Cornwall and much of Devon.
- Derived from lidar data collected by the Tellus South West project.
- Aimed at mapping woody corridors (hedgerows, tree lines) that serve as habitats and dispersal pathways.

## Data access and citation
- Open Government Licence; data available at https://doi.org/10.5285/4b5680d9-fdbc-40c0-96a1-4c022185303f
- If reused, cite: Broughton, R.K.; Gerard, F.; Haslam, R.; Howard, A.S. (2017). Woody habitat corridor data in South West England. NERC Environmental Information Data Centre. https://doi.org/10.5285/4b5680d9-fdbc-40c0-96a1-4c022185303f

## Background
- Habitat corridors of woody linear features provide essential habitats and dispersal routes for woodland and hedgerow species in lowland Britain.
- Mapping the location, extent, and height of hedgerows and non-woodland trees is challenging; lidar-based approaches were used with open GIS datasets to map woody linear features.

## Method
- Output: centre-line polylines of woody corridors; dataset tiled into 20 x 20 km shapefile tiles.
- Processing steps:
  - Generate canopy height model (CHM) by subtracting DTM from DSM; discard features under 1 m.
  - Mask woodland parcels (FC Forest Inventory) and buildings (OS VectorMap District/OpenMap Local with 5 m buffer).
  - Classify >1 m features by height:
    - Class 1: 1 – 1.4999 m (low hedges, shrubs)
    - Class 2: 1.5 – 2.9999 m (most farmland hedges)
    - Class 3: 3 – 5.9999 m (unmanaged hedges, shrubs, young trees)
    - Class 6: 6 – 50 m (hedgerow and non-woodland trees)
  - NoData for other values.
  - Filter out small features: class 1-3 areas < 20 m²; class 6 areas < 10 m²; reassign to surrounding dominant value.
  - Manual review to remove anomalies (glasshouses, unmapped buildings, vehicles, caravan parks, solar farms).
  - Generate centre lines to create the polyline output.
- Data sources and baselines:
  - lidar data collected July/August 2013.
  - ground truthing in Nov 2018 (1 km² SX7485) with 164 height values; comparison to height classes.

## Quality control
- Not an exhaustive error check; extensive manual checks against aerial imagery addressed obvious issues, but residual errors may remain (e.g., coastal misclassification within 50 m of high-water mark; tall crops misclassified as low scrub; irregular patches difficult to render).
- Ground truthing indicates an adjusted overall accuracy of 73.2% for height class matches (134 raw matched samples, adjusted to 120 correct after accounting for threshold boundaries).
- Change over time is considered unlikely for hedges given long-term management; dataset reflects broad class distinctions.

## Data structure and description
- Format: series of shapefile polyline tiles (20 x 20 km).
- Fields:
  - SHAPE: Geometry of the polyline feature.
  - GRIDCODE: Numeric height class code.
  - LENGTH: Numeric length of the polyline in metres.
- Metadata notes:
  - Height classes correspond to defined bins (as above).
  - Centre-line polylines represent likely woody vegetation corridors.
  - Tiles coded by the bottom-left 10 km hectad name.

## Data governance and stewardship considerations
- Licensing and attribution: Open Government Licence with required citation to the dataset and authors.
- Provenance and lineage: lidar-based methodology with explicit processing steps and mask layers; includes references to OS and FC data sources.
- Data quality and limitations: non-exhaustive QC; known misclassifications near coast and in certain crop areas; ground truthing performed several years after data capture; broad height classes limit fine-grained discrimination.
- Update and maintenance: dataset built from 2013 lidar and 2018 ground-truth checks; future updates would require new lidar campaigns and reprocessing to reflect changes in hedgerow structure.
- Interoperability: delivered as shapefile tiles; compatible with common GIS workflows but dependent on ancillary datasets (OS, FC inventories) for masking and interpretation.

## References
- OS Open Map Local, OS VectorMap District. Accessed through Open Government Licence. © Crown copyright and database rights 2015.
- Forestry Commission National Forest Inventory Great Britain 2015. Open Government Licence v3.0.
- Ferraccioli, F. et al. (2014). LiDAR-based DSM data for South West England. NERC EIDC. https://doi.org/10.5285/b81071f2-85b3-4e31-8506-cabe899f989a
- Ferraccioli, F. et al. (2014). LiDAR-based DTM data for South West England. NERC EIDC. https://doi.org/10.5285/e2a742df-3772-481a-97d6-0de5133f4812