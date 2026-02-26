# QGIS Generated Color Map Export File

## Overview
- A QGIS color map export defining a discrete (INTERPOLATION: DISCRETE) mapping from 50 land-cover classes to RGBA colors for visualization.

## Content and Structure
- Interpolation method: DISCRETE.
- 50 entries, each containing:
  - Entry index (1–50)
  - Red, Green, Blue, Alpha color values
  - Class code and description (e.g., 111 - Continuous urban fabric, 112 - Discontinuous urban fabric, etc.)
- Final entries include special categories:
  - 48 - NODATA
  - 49 - UNCLASSIFIED LAND SURFACE
  - 50 - UNCLASSIFIED

## Class List Highlights (representative examples)
- 111: Continuous urban fabric
- 112: Discontinuous urban fabric
- 121: Industrial or commercial units
- 122: Road and rail networks and associated land
- 123: Port areas
- 124: Airports
- 131–135: Various extractive and land-use sites (mineral extraction, dump sites, construction)
- 141–142: Green urban areas; sport and leisure facilities
- 211–213: Agricultural lands (non-irrigated/ar irrigated, rice fields)
- 221–223: Permanent crops (vineyards, fruit trees, olive groves)
- 231–243: Agricultural lands with natural vegetation, agro-forestry
- 311–313: Forest types (broad-leaved, coniferous, mixed)
- 321–324: Natural grasslands and related habitats
- 331–333: Beaches, bare rocks, sparsely vegetated areas
- 411–412: Inland marshes and peat bogs
- 421–423: Wetlands and coastal features (salt marshes, salines, intertidal flats)
- 511–522: Water-related features (water courses, water bodies, coastal lagoons, estuaries)
- 523: Sea and ocean
- 990/999: UNCLASSIFIED or NODATA categories

## How to Use for Analysis
- Load the color map into QGIS to apply a consistent RGBA scheme to each land-cover class.
- Use the 50 entries to interpret rasterized outputs by matching raster class codes to the corresponding descriptions (e.g., 111, 112, 121, etc.).
- Leverage the discrete classification to perform category-specific analyses (e.g., area by class, correlations with environmental or socio-economic variables).

## Notable Details
- The file uses discrete colors for clear category separation.
- Colors are defined per class with explicit RGBA values, enabling straightforward visualization.
- Includes explicit handling for non-classified and missing data (NODATA and UNCLASSIFIED entries).