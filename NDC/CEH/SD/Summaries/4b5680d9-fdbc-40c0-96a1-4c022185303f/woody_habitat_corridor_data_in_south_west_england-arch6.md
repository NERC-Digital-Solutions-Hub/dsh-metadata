# Woody habitat corridor data in South West England

## Overview
- Polylines depicting non-woodland linear tree and shrub features in Cornwall and much of Devon.
- Derived from LiDAR data collected by the Tellus South West project.
- Height-classified canopy features used to map woody corridors and potential habitats.
- Output delivered as 20 x 20 km shapefile tiles, with center lines representing woody corridors.

## Data access and citation
- Open Government Licence; data available at https://doi.org/10.5285/4b5680d9-fdbc-40c0-96a1-4c022185303f
- Citation: Broughton, R.K.; Gerard, F.; Haslam, R.; Howard, A.S. (2017). Woody habitat corridor data in South West England. NERC Environmental Information Data Centre. https://doi.org/10.5285/4b5680d9-fdbc-40c0-96a1-4c022185303f

## Background
- Woody linear features (hedgerows, tree lines) are important habitats and dispersal corridors in lowland Britain.
- Mapping location, extent, and height of hedges and non-woodland trees is challenging.
- LiDAR-based DSM/DTM data, combined with open GIS datasets, was used to map non-woodland linear woody features.

## Method
- Subtract 1 m resolution DTM from DSM to create a canopy height model (CHM).
- Discard features under 1 m in height.
- Mask woodland parcels (Forestry Commission) and buildings (OS VectorMap Local/OpenMap Local with 5 m buffer).
- Classify remaining features >1 m tall into height bins:
  - Class 1: 1.0–1.4999 m (low hedges, shrubs)
  - Class 2: 1.5–2.9999 m (most managed hedges)
  - Class 3: 3–5.9999 m (unmanaged hedges, shrubs, young trees)
  - Class 6: 6–50 m (hedgerow and non-woodland trees)
  - NoData: all else
- Filter out small areas (Class 1–3 < 20 m²; Class 6 < 10 m²) by generalizing to surrounding values.
- Manual checking to remove anomalies (glasshouses, unmapped buildings, vehicles, caravan parks, solar farms).
- Generate centre lines to produce polyline output of woody corridors.
- Tile dataset into 20 x 20 km shapefiles, coded by bottom-left 10 km hectad name.

## Quality control
- Not exhaustively checked; extensive manual review against aerial imagery removed obvious anomalies.
- Coastal misclassification: features within 50 m of high-water mark removed.
- Tall field crops may appear as low scrub; irregular patches of trees can yield very dense or simplistic polylines.
- Ground truthing in Nov 2018 (1 km grid SX7485) with 164 height samples; 134 matched to the model, but many were near class thresholds.
- Adjusted accuracy: 120 correct samples out of 164 → 73.2% overall class-match accuracy.
- Note: 2013 LiDAR data with 2018 ground truth; changes unlikely in long-term hedgerow management, and broad class ranges mitigate some change.

## Data structure and description
- Shapefile polyline tiles (20 x 20 km) representing features likely to be woody vegetation.
- Fields:
  - SHAPE: Geometry (polyline)
  - GRIDCODE: Height class code (numeric)
  - LENGTH: Polyline length in metres

## References
- OS Open Map Local, OS VectorMap District. Open Government Licence.
- Forestry Commission National Forest Inventory Great Britain 2015. Open Government Licence v3.0.
- Ferraccioli, F. et al. (2014). LiDAR DSM data for South West England. NERC EIDC. https://doi.org/10.5285/b81071f2-85b3-4e31-8506-cabe899f989a
- Ferraccioli, F. et al. (2014). LiDAR DTM data for South West England. NERC EIDC. https://doi.org/10.5285/e2a742df-3772-481a-97d6-0de5133f4812