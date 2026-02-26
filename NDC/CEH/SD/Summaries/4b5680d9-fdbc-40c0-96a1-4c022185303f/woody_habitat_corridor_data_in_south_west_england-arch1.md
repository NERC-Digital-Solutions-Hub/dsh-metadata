# Woody habitat corridor data in South West England

- What it is: A dataset of polylines representing non-woodland woody linear features (hedgerows, tree lines, and related habitat corridors) in Cornwall and much of Devon, derived from lidar data collected by the Tellus South West project and integrated with open GIS datasets.

- Purpose and usefulness: Maps woody habitat corridors essential for woodland and hedgerow species dispersal in farmed and urban landscapes; supports large-scale habitat mapping and ecological planning.

- Data access and citation:
  - Available under the Open Government Licence.
  - Source: Broughton et al. (2017) Woody habitat corridor data in South West England, NERC Environmental Information Data Centre.
  - DOI: 10.5285/4b5680d9-fdbc-40c0-96a1-4c022185303f

- Content and scope:
  - Output: 20 x 20 km shapefile tiles containing polyline features likely to be woody vegetation.
  - Each feature has a height class code and length; tile code corresponds to bottom-left 10 km hectad name.
  - Height classes (based on canopy height model):
    - Class 1: 1 – 1.4999 m (low hedges, shrubs)
    - Class 2: 1.5 – 2.9999 m (most managed hedges)
    - Class 3: 3 – 5.9999 m (unmanaged hedges, shrubs, young trees)
    - Class 6: 6 – 50 m (hedgerows and non-woodland trees)
    - NoData for other values

- Method (how it was created):
  - Derived from lidar-derived DSM and DTM to create a canopy height model (CHM = DSM − DTM).
  - Features < 1 m removed; woodland parcels and buildings masked using FC Forest Inventory and OS VectorMap Local/OpenMap Local (with 5 m buffer).
  - Remaining features > 1 m classified into height classes; small features (<20 m² for classes 1–3; <10 m² for class 6) generalized to surrounding values to reduce noise.
  - Manual checks to remove anomalies (e.g., glasshouses, new buildings, vehicles, solar farms).
  - Centre lines generated to form polylines representing woody corridors.
  - Dataset tiled into 20 x 20 km squares, with 10 km hectad naming convention.

- Quality control and limitations:
  - Not exhaustively checked; extensive manual checks against aerial imagery performed.
  - Coastal misclassifications: features within 50 m of high water mark removed; tall in-field crops may be misclassified as low scrub.
  - Irregular patches may yield very dense or very simplistic polylines due to classification/rendering challenges.
  - Lidar data from July/August 2013; ground truthing in Nov 2018 (SX7485).
  - Ground truth: 164 points; 134 matched to corresponding height class; after adjustment for class boundary thresholds, overall adjusted accuracy is 73.2%.

- Data structure:
  - Shapefile polyline tiles (20 x 20 km).
  - Attributes:
    - SHAPE: geometry
    - GRIDCODE: numeric height class code
    - LENGTH: length in metres

- References and data sources:
  - OS Open Map Local and OS VectorMap District (Open Government Licence)
  - Forestry Commission National Forest Inventory Great Britain 2015
  - Ferraccioli et al. 2014 (Lidar-based DSM/DTM for South West England)

- Practical considerations for analysts:
  - Useful for landscape-scale habitat connectivity and planning but consider coastal misclassification, potential misclassification of dense crops, and the dated lidar (2013) with limited ground-truthing.
  - When integrating with other datasets, be mindful of the height-class discretization and area-generalization steps that may affect precision at local scales.