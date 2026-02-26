# QGIS Generated Color Map Export File

## Overview
- A QGIS-generated, discrete color map export for land cover classifications.
- Defines how each land cover class is visualized with a specific RGBA color and descriptive label.
- Intended to standardize map visuals for environmental monitoring and reporting.

## Data structure
- Each line encodes:
  - Class index (e.g., 1, 2, 3, …, 50, plus 48, 49, 50 for special codes)
  - Red, Green, Blue, Alpha color values (RGBA) in 0–255
  - A numeric CORINE-like code (e.g., 111, 112, 121, …, 523)
  - Text description of the class (e.g., “Continuous urban fabric,” “Road and rail networks and associated land”)

- Interpolation method: DISCRETE
- Example interpretation per line: 1, 230, 0, 77, 255, 111 - Continuous urban fabric

## Key classes included (high-level categories)
- Urban and built-up areas
  - Continuous urban fabric
  - Discontinuous urban fabric
  - Industrial or commercial units
  - Road and rail networks and associated land
  - Port areas
  - Airports
- Land use and agriculture
  - Non-irrigated arable land
  - Permanently irrigated land
  - Rice fields
  - Vineyards
  - Fruit trees and berry plantations
  - Olive groves
  - Pastures
  - Annual crops with permanent crops
  - Complex cultivation patterns
  - Agriculture with significant natural vegetation
  - Agro-forestry areas
- Forests and natural vegetation
  - Broad-leaved forest
  - Coniferous forest
  - Mixed forest
  - Natural grasslands
  - Moors and heathland
  - Sclerophyllous vegetation
  - Transitional woodland-shrub
- Other land surface types
  - Beaches, bare rocks, sparsely vegetated areas
  - Burnt areas
  - Glaciers and perpetual snow
- Wetlands and water bodies
  - Inland marshes, peat bogs
  - Salt marshes, salines
  - Intertidal flats
  - Watercourses, water bodies
  - Coastal lagoons, estuaries
  - Sea and ocean
- Special categories
  - NODATA
  - UNCLASSIFIED LAND SURFACE
  - UNCLASSIFIED WATER BODIES

## Practical use for monitoring and reporting
- Provides a consistent legend for visualizing land cover in environmental assessment maps.
- Facilitates comparison over time by maintaining standardized color encoding across datasets and reports.
- Supports data sharing and collaboration by offering a clear, reproducible color scheme for classification outputs.

## Data management and accessibility considerations
- Designed for standardised outputs; aligns with established classification schemes and portals.
- Encourages storage and upload of generated datasets to appropriate data portals for transparency and reuse.
- The discrete encoding supports straightforward layering with other environmental indicators for richer analyses.

## Relevance to monitoring challenges
- Enables value enhancement of monitoring datasets when combined with other data layers (e.g., climate, biodiversity, infrastructure).
- Supports broad accessibility of underlying class-color mappings, aiding cross-team analysis and policy scrutiny.