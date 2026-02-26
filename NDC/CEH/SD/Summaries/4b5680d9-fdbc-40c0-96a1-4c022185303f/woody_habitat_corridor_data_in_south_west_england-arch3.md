# Woody habitat corridor data in South West England

- Purpose: A dataset of polylines depicting non-woodland woody linear features (hedgerows, tree lines, and similar) in Cornwall and much of Devon, derived from Tellus South West lidar data, intended to map habitat corridors and inform environmental monitoring and policy decisions.

- Data access and citation:
  - Open Government Licence; DOI: 10.5285/4b5680d9-fdbc-40c0-96a1-4c022185303f
  - Citation: Broughton, R.K.; Gerard, F.; Haslam, R.; Howard, A.S. (2017). Woody habitat corridor data in South West England. NERC EIDC.

- Background and motivation:
  - Woody linear features (hedgerows and tree lines) are important habitats and dispersal corridors in lowland Britain.
  - Mapping the location, extent, and height of these features has been challenging; lidar-based methods were used to enable large-area mapping.

- Methodology (data processing workflow):
  - Start with 1-m lidar-derived DSM and DTMs to produce a canopy height model (CHM) by subtracting DTM from DSM.
  - Remove features below 1 m height; mask woodland parcels (Forestry Commission) and buildings (OS VectorMap District/OpenMap Local with 5 m buffer).
  - Classify features >1 m into height bins:
    - Class 1: 1–1.4999 m (low hedges, shrubs)
    - Class 2: 1.5–2.9999 m (most managed hedges)
    - Class 3: 3–5.9999 m (unmanaged outgrown hedges, shrubs, young trees)
    - Class 6: 6–50 m (hedgerows and non-woodland trees)
  - Filter out small features (Class 1–3 < 20 m²; Class 6 < 10 m²); generalize to surrounding values to reduce noise.
  - Manual checks to remove anomalies (greenhouses, new buildings, vehicles, caravan parks, solar farms).
  - Generate center lines to create polyline outputs; tile dataset into 20 x 20 km shapefiles (coded by bottom-left 10 km hectad name).

- Quality control and limitations:
  - Not all errors are exhaustively checked; extensive manual checking against aerial imagery removed obvious anomalies, but some remain.
  - Coastal misclassification: features within 50 m of high-water mark removed; some tall-field crops may appear as low scrub.
  - Tall or irregular patches of trees may be rendered as very dense or very sparse polylines.
  - Data originate from lidar collected in 2013; ground-truthing in 2018 (1 km² SX7485) with 164 sample points; overall adjusted accuracy 73.2% (120 correct out of 164 after adjusting for class-threshold ambiguities).
  - Changes over time are possible but considered unlikely for hedges due to long-term management; height classes are broad to accommodate change.

- Data structure and description:
  - Output: shapefile polyline tiles (20 x 20 km) indicating woody features likely to be trees/shrubs.
  - Attributes:
    - SHAPE: geometry (polyline)
    - GRIDCODE: numeric height class code
    - LENGTH: length of polyline in metres

- Data sources and references:
  - OS Open Map Local; OS VectorMap District (Crown copyright)
  - Forestry Commission National Forest Inventory GB (Open Government Licence)
  - Ferraccioli et al. (2014) lidar-based DSM/DTM data for South West England
  - Related lidar-derived datasets and acknowledgments to NERC EIDC

- Implications for monitoring frameworks:
  - Provides spatially explicit, tallied indicators of woody corridors useful for habitat connectivity and landscape-scale health monitoring.
  - Strengths: large-area coverage, standardized processing workflow, open data access, clear height classification scheme.
  - Considerations for policymakers and auditors: be aware of age of lidar data (2013), potential coastal misclassifications, and limitations in ground-truthing; ensure metadata completeness and consider data governance for ongoing updates and reproducibility.