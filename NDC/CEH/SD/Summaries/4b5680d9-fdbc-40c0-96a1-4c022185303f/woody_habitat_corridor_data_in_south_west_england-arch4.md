# Woody habitat corridor data in South West England

- A dataset of polylines representing non-woodland linear woody features (hedgerows, tree lines) in Cornwall and much of Devon.
- Derived from lidar data collected by the Tellus South West project, combined with open-source GIS datasets to map woody corridors.

## Data access, rights and citation
- Licensed under the Open Government Licence.
- Access and DOI: https://doi.org/10.5285/4b5680d9-fdbc-40c0-96a1-4c022185303f
- Citation for reuse: Broughton, R.K.; Gerard, F.; Haslam, R.; Howard, A.S. (2017). Woody habitat corridor data in South West England. NERC Environmental Information Data Centre. https://doi.org/10.5285/4b5680d9-fdbc-40c0-96a1-4c022185303f

## Why this data matters for data leaders
- Habitat corridors are vital for woodland and hedgerow species in lowland Britain; large-scale mapping of these features has been limited by technical and logistical challenges.
- Combines remote sensing (lidar) with existing datasets to support planning, policy, and ecological connectivity assessments.
- Data outputs are structured for integration into broader data systems (tile-based shapefiles with height classification).

## How the data were produced (Method)
- Generate canopy height model (CHM) by subtracting a Digital Terrain Model from a Digital Surface Model derived from 1-m lidar.
- Exclude features below 1 m; mask woodland parcels and buildings.
- Classify remaining features greater than 1 m into height classes:
  - Class 1: 1–1.4999 m (low hedges, shrubs)
  - Class 2: 1.5–2.9999 m (most managed hedges)
  - Class 3: 3–5.9999 m (unmanaged hedges, shrubs, young trees)
  - Class 6: 6–50 m (hedgerows and non-woodland trees)
- Filter out very small features and generalize noise; manually remove anomalies (glasshouses, new buildings, vehicles, etc.).
- Create centre lines to form polyline outputs of woody corridors.
- Tile dataset into 20 x 20 km shapefiles, coded by bottom-left 10 km hectad name.

## Data quality, limitations and validation
- Not an exhaustive QA; extensive manual checks against aerial imagery reduced obvious errors.
- Notable issues: misclassification near the coast (coastal 50 m buffer removed), some tall crops misidentified as scrub, and very dense/sparse patches due to irregular patching.
- Ground truthing in Nov 2018 (1 km² blocks, 164 samples) showed an adjusted overall accuracy of 73.2% for height class matches, acknowledging some samples fell between height class thresholds.
- lidar data collected in 2013; ground truthing in 2018 mitigates concerns given hedges tend to be long-lived, but some change over time is possible.

## Data structure and description
- Output: shapefile polyline tiles (20 x 20 km) representing woody vegetation corridors.
- Fields:
  - SHAPE: geometry (polyline)
  - GRIDCODE: numeric height class code
  - LENGTH: length of polyline feature in metres

## Data sources and references
- OS Open Map Local and OS VectorMap District (Open Government Licence).
- Forestry Commission National Forest Inventory Great Britain (2015).
- Ferraccioli et al. LiDAR-based DSM/DTM data for South West England (various DOIs).
- Ground truth and methodology documentation linked to NERC Environmental Information Data Centre.

## Implications for data governance and reuse
- Licensed data with clear attribution and a reproducible workflow (lidar-based morphometrics, height-class classification).
- Dataset tiling and class coding support discoverability and integration into larger data ecosystems.
- Users should be aware of classification limitations and edge-case exclusions (coastal areas, certain urban/perimeter features).
- Encourages cross-agency collaboration by combining lidar with existing OS/FC datasets to support broader habitat connectivity analyses.