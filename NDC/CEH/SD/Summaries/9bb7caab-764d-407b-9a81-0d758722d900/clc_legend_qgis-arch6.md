# QGIS Generated Color Map Export File

## Overview
- A QGIS color map export using discrete interpolation that defines 50 land-cover classes with associated colors and labels.

## File structure
- Each entry defines:
  - Index (1–50)
  - RGBA color components (R, G, B, A)
  - Class code (e.g., 111–999, with special 990/995-range for unclassified)
  - Human-readable label describing the land-cover category

## Key class categories (representative examples)
- Urban and built environments:
  - 111 Continuous urban fabric
  - 112 Discontinuous urban fabric
  - 121 Industrial or commercial units
  - 122 Road and rail networks and associated land
  - 123 Port areas
  - 124 Airports
- Other built/infrastructure and land use:
  - 131 Mineral extraction sites
  - 132 Dump sites
  - 133 Construction sites
- Green spaces and recreation:
  - 141 Green urban areas
  - 142 Sport and leisure facilities
- Agriculture and crops:
  - 211 Non-irrigated arable land
  - 212 Permanently irrigated land
  - 213 Rice fields
  - 221 Vineyards
  - 222 Fruit trees and berry plantations
  - 223 Olive groves
  - 231 Pastures
  - 241 Annual crops with permanent crops
  - 242 Complex cultivation patterns
- Mixed/agro-forest and vegetation:
  - 243 Land principally occupied by agriculture with significant areas of natural vegetation
  - 244 Agro-forestry areas
- Forests and natural vegetation:
  - 311 Broad-leaved forest
  - 312 Coniferous forest
  - 313 Mixed forest
  - 321 Natural grasslands
  - 322 Moors and heathland
  - 323 Sclerophyllous vegetation
  - 324 Transitional woodland-shrub
- Land forms and bare areas:
  - 331 Beaches - dunes - sands
  - 332 Bare rocks
  - 333 Sparsely vegetated areas
  - 334 Burnt areas
  - 335 Glaciers and perpetual snow
- Wetlands and water-related:
  - 411 Inland marshes
  - 412 Peat bogs
  - 421 Salt marshes
  - 422 Salines
  - 423 Intertidal flats
  - 511 Water courses
  - 512 Water bodies
  - 521 Coastal lagoons
  - 522 Estuaries
  - 523 Sea and ocean
- Special classes:
  - 48 NODATA
  - 49 UNCLASSIFIED LAND SURFACE
  - 50 UNCLASSIFIED WATER BODIES
  - 255 UNCLASSIFIED

## Color details
- Each class line provides RGBA color values to be used when rendering the corresponding class in a map.
- The color mapping enables clear visual differentiation across all listed land-cover categories.

## Usage considerations for data support
- Facilitates quick styling of land-cover layers for end users to explore data through self-serve visualizations.
- Useful for policy and planning contexts where diverse topics require accessible, color-coded data representations.
- Be mindful of unclassified and nodata entries when merging with other datasets or performing analyses.