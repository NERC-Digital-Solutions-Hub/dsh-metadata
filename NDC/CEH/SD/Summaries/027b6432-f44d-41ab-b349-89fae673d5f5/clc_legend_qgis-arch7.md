# QGIS Generated Color Map Export File

## Overview
- A QGIS color map export designed for discrete classification visualization.
- Defines a palette of 50 color-filled classes with associated codes and Descriptions, suitable for mapping land cover or CORINE-like categories.
- Each entry specifies an RGBA color, a class code, and a human-readable label.

## Content of the Color Map
- Interpolation mode: DISCRETE
- 50 color-class entries, plus special classes:
  - 1–50: Main discrete classes with specific RGB colors and codes (e.g., 111, 112, 121, 122, 123, etc.) and descriptions such as:
    - Continuous urban fabric
    - Discontinuous urban fabric
    - Industrial or commercial units
    - Road and rail networks and associated land
    - Port areas
    - Airports
    - Mineral extraction sites
    - Dump sites
    - Construction sites
    - Green urban areas
    - Sport and leisure facilities
    - Non-irrigated arable land
    - Permanently irrigated land
    - Rice fields
    - Vineyards
    - Fruit trees and berry plantations
    - Olive groves
    - Pastures
    - Annual crops associated with permanent crops
    - Complex cultivation patterns
    - Agriculture with significant natural vegetation
    - Agro-forestry areas
    - Broad-leaved forest
    - Coniferous forest
    - Mixed forest
    - Natural grasslands
    - Moors and heathland
    - Sclerophyllous vegetation
    - Transitional woodland-shrub
    - Beaches, dunes, sands
    - Bare rocks
    - Sparsely vegetated areas
    - Burnt areas
    - Glaciers and perpetual snow
    - Inland marshes
    - Peat bogs
    - Salt marshes
    - Salines
    - Intertidal flats
    - Water courses
    - Water bodies
    - Coastal lagoons
    - Estuaries
    - Sea and ocean
  - 48: NODATA
  - 49: UNCLASSIFIED LAND SURFACE
  - 50: UNCLASSIFIED WATER BODIES
- Final entry:
  - 255,255,255,255,255,990 - UNCLASSIFIED (terminator/placeholder)

## How to Use
- Purpose: Apply to raster data with corresponding class codes to produce a map with labeled land-cover categories.
- Steps:
  - Import or copy this color map into QGIS as a style for a raster layer.
  - Ensure the raster’s classification codes match the codes listed (e.g., 111, 112, 121, 122, …, 523, 411–523, etc.).
  - The entries are discrete; each class is mapped to a single color.
- Practical applications: Creating readable, produce-ready maps for policy, planning, environmental analysis, or public-facing GIS visualizations.

## Considerations
- The palette is tailored to CORINE-like land-cover classes with explicit codes and labels.
- Some codes (e.g., 999 for NODATA, 990 for UNCLASSIFIED) indicate special handling in the dataset.
- Colors are fixed per class; if the audience requires different color semantics, adjust the palette while preserving class mappings.

## Endnotes
- The file is a generated, discrete color map export intended to reproduce a predefined, class-based visualization in QGIS.