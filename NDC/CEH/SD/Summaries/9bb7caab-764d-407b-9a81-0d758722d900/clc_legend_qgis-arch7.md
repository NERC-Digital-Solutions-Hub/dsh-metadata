# QGIS Generated Color Map Export File

## Overview
- A discrete color map exported from QGIS for classifying land cover categories.
- Interpolation is set to DISCRETE, meaning each class has a fixed color without gradient transitions.
- Defines 50 primary classes (1 through 50) with specific RGB colors and descriptive labels.
- Includes additional special entries for nodata and unclassified categories.
- Each line maps a class index to an RGB color, an alpha value, a dataset code, and a label.

## Structure of the color map
- Format per entry (as seen in the file): index, R, G, B, A, code - Description
  - Example pattern: 1,230,000,077,255, 111 - Continuous urban fabric
  - The first value is the class index; the next three are the red, green, and blue color components; the following value is the alpha (transparency); the subsequent number is a dataset-specific code; the text after the dash is the human-readable label.

## Key class mappings (highlights)
- 1 - Continuous urban fabric
- 2 - Discontinuous urban fabric
- 3 - Industrial or commercial units
- 4 - Road and rail networks and associated land
- 5 - Port areas
- 6 - Airports
- 7 - Mineral extraction sites
- 8 - Dump sites
- 9 - Construction sites
- 10 - Green urban areas
- 11 - Sport and leisure facilities
- 12 - Non-irrigated arable land
- 13 - Permanently irrigated land
- 14 - Rice fields
- 15 - Vineyards
- 16 - Fruit trees and berry plantations
- 17 - Olive groves
- 18 - Pastures
- 19 - Annual crops associated with permanent crops
- 20 - Complex cultivation patterns
- 21 - Land principally occupied by agriculture with significant areas of natural vegetation
- 22 - Agro-forestry areas
- 23 - Broad-leaved forest
- 24 - Coniferous forest
- 25 - Mixed forest
- 26 - Natural grasslands
- 27 - Moors and heathland
- 28 - Sclerophyllous vegetation
- 29 - Transitional woodland-shrub
- 30 - Beaches, dunes, sands
- 31 - Bare rocks
- 32 - Sparsely vegetated areas
- 33 - Burnt areas
- 34 - Glaciers and perpetual snow
- 35 - Inland marshes
- 36 - Peat bogs
- 37 - Salt marshes
- 38 - Salines
- 39 - Intertidal flats
- 40 - Water courses
- 41 - Water bodies
- 42 - Coastal lagoons
- 43 - Estuaries
- 44 - Sea and ocean
- 48 - NODATA
- 49 - UNCLASSIFIED LAND SURFACE
- 50 - UNCLASSIFIED WATER BODIES
- 255 - UNCLASSIFIED

## Special entries
- NODATA: Represented with its own color and code for areas with no data.
- UNCLASSIFIED categories:
  - UNCLASSIFIED LAND SURFACE
  - UNCLASSIFIED WATER BODIES
  - General UNCLASSIFIED entry (catch-all)

## Usage notes for GIS workflows
- This color map is intended for raster classifications where each cell is assigned one of the 50 defined classes (or a special NODATA/UNCLASSIFIED category).
- Because interpolation is discrete, visualizations should avoid gradient blending between classes.
- The explicit RGB values can be applied directly in QGIS or other GIS software to reproduce the exact color scheme for map-based data products.
- Useful for policy briefs, client reports, and public-facing maps where clear, color-differentiated land cover categories are required.