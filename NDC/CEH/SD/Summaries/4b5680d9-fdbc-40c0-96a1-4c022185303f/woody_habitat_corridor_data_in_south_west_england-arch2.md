# Woody habitat corridor data in South West England

## Overview
- Dataset of polylines depicting non-woodland linear woody features (hedgerows, tree lines) in Cornwall and much of Devon.
- Derived from lidar data collected by the Tellus South West project and combined with open GIS datasets.
- Aims to map woody corridors that provide habitat and dispersal pathways in lowland Britain.

## Data access and citation
- Available under Open Government Licence.
- Access: https://doi.org/10.5285/4b5680d9-fdbc-40c0-96a1-4c022185303f
- Citation: Broughton, R.K.; Gerard, F.; Haslam, R.; Howard, A.S. (2017). Woody habitat corridor data in South West England. NERC Environmental Information Data Centre. https://doi.org/10.5285/4b5680d9-fdbc-40c0-96a1-4c022185303f

## Background and purpose
- Woody linear features act as important habitats and dispersal corridors for woodland and hedgerow species in farmed and urban landscapes.
- Mapping the location, extent, and height of such features has been challenging; lidar-based methods were used to identify non-woodland woody vegetation.
- The dataset supports habitat monitoring and environmental health assessments by providing standardized corridor geometry.

## Method (how the data were produced)
- Input data and processing:
  - Use 1-m lidar-derived digital terrain model (DTM) and digital surface model (DSM) to create a canopy height model (CHM) by subtracting DTM from DSM.
  - Discard features with height < 1 m.
  - Mask woodland parcels (Forestry Commission) and buildings (OS VectorMap District/OpenMap Local with buffers).
  - Classify remaining features > 1 m into height classes:
    - Class 1: 1 – 1.4999 m (low hedges, shrubs)
    - Class 2: 1.5 – 2.9999 m (most managed farmland hedges)
    - Class 3: 3 – 5.9999 m (unmanaged hedges, shrubs, young trees)
    - Class 6: 6 – 50 m (hedgerow and non-woodland trees)
  - Filter out small areas (Class 1–3 < 20 m²; Class 6 < 10 m²) or assign to surrounding dominant values.
  - Manual review to remove anomalies (glasshouses, new buildings, vehicles, caravan parks, solar farms).
  - Generate centre lines to produce polyline outputs of woody corridors.
  - Tile the dataset into 20 x 20 km shapefiles, coded by bottom-left 10 km hectad name.
- Data sources involved:
  - OS Open Map Local, OS VectorMap District (Open Government Licence)
  - Forestry Commission National Forest Inventory (GB, 2015)
  - LiDAR-based DSM/DTM data (Tellus South West/NERC EIDC)

## Quality control and limitations
- Not an exhaustive error check; extensive manual checks against aerial imagery mitigated obvious issues, but some errors remain.
- Coastal areas: misclassification risk near high water mark (50 m coastal buffer removal applied).
- Tall in-field crops may appear as low scrub; irregular patches of trees/scrub can create very dense or sparse polyline areas.
- Ground truthing in 2018 ( SX7485 1 km square) with 164 point samples:
  - 120 matched between observed height class and lidar-derived class after adjustment.
  - Overall adjusted accuracy: 73.2%.
  - Some discrepancies due to height class threshold boundaries (e.g., 6 m threshold between Class 3 and Class 6).

## Data structure and description
- Output: shapefile polyline tiles (20 x 20 km) depicting likely woody vegetation features.
- Attributes:
  - SHAPE: geometry (polyline)
  - GRIDCODE: numeric height class code of the polyline feature
  - LENGTH: length of the polyline feature in metres

## Relevance for environmental monitoring analysts
- Provides a standardized, scalable dataset of woody habitat corridors suitable for integration with other environmental health indicators and policy performance datasets.
- Facilitates monitoring of habitat connectivity and changes over time when combined with time-series data and other Open GIS layers.
- Supports spatial analyses such as corridor density, overlap with land-use changes, and habitat suitability modeling, while explicitly noting the method-based height classifications and their limitations.