# QGIS Generated Color Map Export File

## Overview
- A QGIS-generated color map export for a discrete land-cover classification.
- Uses the header INTERPOLATION:DISCRETE, indicating a discrete legend for class coloring.
- Contains 50 class entries, each with an RGBA color and an associated class code and label.
- Includes special classes for NODATA and UNCLASSIFIED categories at the end.

## File structure and content
- Each line after the header follows the pattern:
  - index, R, G, B, A, code - description
  - Example: 1,230,000,077,255, 111 - Continuous urban fabric
- RGBA color values are provided as integers (Red, Green, Blue, Alpha) for visualization.
- Class codes cover a broad set of land-cover types (urban areas, transportation networks, agricultural lands, forests, wetlands, water bodies, etc.).
- Special entries:
  - NODATA (code 999)
  - UNCLASSIFIED LAND SURFACE (code 990)
  - UNCLASSIFIED WATER BODIES (code 995)
  - An additional UNCLASSIFIED placeholder appears at the end

## Class roster (highlights)
- 111 - Continuous urban fabric
- 112 - Discontinuous urban fabric
- 121-124 - Industrial/commercial, roads/rail, port areas, airports
- 131-132 - Mineral extraction, dump sites
- 133-141-142 - Construction sites, Green urban areas, Sport/leisure
- 211-243 - Various agricultural classes and related vegetation
  - Examples: Non-irrigated arable land (211), Permanently irrigated land (212), Rice fields (213), Vineyards (221), Complex cultivation patterns (242)
- 311-324 - Forests, grasslands, heathlands, and related vegetation
- 331-335 - Beaches/sand areas, bare rocks, sparsely vegetated areas, burnt areas
- 411-423 - Wetlands and aquatic/coastal landscapes (marshes, estuaries, intertidal)
- 511-523 - Water bodies and coastal features (water courses, lagoons, sea)
- 999 - NODATA
- 990/995 - UNCLASSIFIED categories (land surface, water bodies)

## Governance and data stewardship implications
- Ensures a consistent visual legend for dataset sharing and cross-dataset interoperability.
- Critical to document in metadata:
  - The exact class-to-color mapping (RGBA values)
  - The class codes and their descriptive labels
  - The data source and version of the color map
  - Any embargoed or restricted classes (if applicable)
- Use the color map to accompany the dataset in catalogs and repositories to enable reproducible visualization.
- Ensure alignment between the color map and data attributes (class codes) across updates; track changes to avoid mislabeling.
- Include notes on NODATA and UNCLASSIFIED classes to prevent misinterpretation during analysis and visualization.

## Practical guidance for use
- Validate that imported datasets display the intended colors for each class when applying the map.
- Store the color map alongside the dataset and reference it in dataset documentation or catalogue records.
- When updating datasets, refresh the color map to maintain consistency with any schema changes in class definitions.