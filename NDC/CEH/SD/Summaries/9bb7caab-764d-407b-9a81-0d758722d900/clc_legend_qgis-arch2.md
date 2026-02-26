# QGIS Generated Color Map Export File

## Summary
- A QGIS color map export that defines discrete classes for land cover/land use with corresponding RGBA colors.
- Interpolation method is set to DISCRETE, meaning each class is shown with a single color.
- Contains 50 standard classes (codes 1–50) plus special entries for data handling and unclassified categories.
- Each entry lists: code, color (R,G,B,A), and a descriptive label.

## Color Map Structure
- Codes 1–50 cover a wide range of land cover types, including:
  - Urban areas (continuous and discontinuous)
  - Industrial/commercial units
  - Road/rail networks, ports, airports
  - Various agricultural lands and patterns
  - Forests (broad-leaved, coniferous, mixed) and other vegetation
  - Grasslands, moors, transitional vegetation
  - Coastal, water-related features (water bodies, estuaries, seas)
  - Wetlands and related land/water features
  - Bare/rocky and burnt areas
  - Glaciers, snow, and ice
- Each class is assigned a specific RGBA color with full opacity (A = 255).

## Special Entries
- 48 - NODATA
- 49 - UNCLASSIFIED LAND SURFACE
- 50 - UNCLASSIFIED WATER BODIES
- 990 - UNCLASSIFIED (white color)

## Example Class Scope (representative highlights)
- 1 - Continuous urban fabric
- 2 - Discontinuous urban fabric
- 11 - Sport and leisure facilities
- 22 - Agro-forestry areas
- 41 - Water courses
- 42 - Water bodies
- 43 - Coastal lagoons
- 44 - Sea and ocean
- 48-50 - Special handling categories (NODATA, UNCLASSIFIED)

## How this supports environmental monitoring
- Provides a standardized, repeatable visual schema for maps and dashboards.
- Facilitates consistent interpretation of environmental health and policy performance over time.
- Enables easy storage and portal upload of standardized color-encoded datasets.
- Aligns with analysts’ goals of verifiable, comparable outputs across monitoring programs.