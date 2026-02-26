# QGIS Generated Color Map Export File

- A QGIS color map export tuned for discrete classification.
- Defines a palette for 50 classes plus special categories used in a land-cover style scheme.
- Each entry lists: an index, RGBA color (red, green, blue, alpha), a numeric class code, and a descriptive label.

## Palette structure and contents

- Interpolation: DISCRETE, indicating a stepped color scheme rather than a gradient.
- Class entries (1 through 50) cover a wide range of land-cover categories, including:
  - Urban areas and related infrastructure: continuous urban fabric, discontinuous urban fabric, industrial/commercial units, road/rail networks, port areas, airports.
  - Natural and semi-natural environments: broad-leaved/Coniferous/Mixed forests, natural grasslands, moors/heathland, sclerophyllous vegetation, transitional woodland/shrub, agro-forestry areas.
  - Agricultural lands and crops: various arable lands, irrigated lands, rice fields, vineyards, fruit trees/berry plantations, olive groves, pastures, and other crop patterns.
  - Other land features: mineral extraction sites, dumps, construction sites, green urban areas, sport/leisure facilities, beaches/dunes, bare rocks, sparsely vegetated areas, burnt areas, glaciers/perpetual snow.
  - Water-related: inland marshes, peat bogs, salt marshes, salines, intertidal flats, water courses, water bodies, coastal lagoons, estuaries, sea/ocean.
- Each line provides the color (RGBA) aligned with its label, enabling clear visual differentiation when mapping.

## Notable special categories

- 48 NODATA: white color (255,255,255,255) indicating missing or undefined data.
- 49 UNCLASSIFIED LAND SURFACE: white color (255,255,255,255) representing unclassified land areas.
- 50 UNCLASSIFIED WATER BODIES: light color (230,242,255,255) representing unclassified water features.
- 255 UNCLASSIFIED: white color (255,255,255,255,255) used as an additional unclassified indicator.

## Practical use for GIS specialists

- Apply this color map to a land-cover dataset to visually distinguish the 50 defined classes on maps.
- Use the discrete palette to ensure consistent category colors across datasets and maps.
- Reference the class descriptions to align map visuals with land-cover terminology (e.g., urban fabric, forests, croplands, water bodies).
- Integrate with QGIS projects to style rasters or categorized layers, utilizing the provided RGBA values for precise rendering.
- Leverage the NODATA and UNCLASSIFIED entries to clearly indicate missing data and unclassified regions in visualizations.