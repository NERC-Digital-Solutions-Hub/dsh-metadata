# QGIS Generated Color Map Export File

## Overview
- A QGIS color map export that assigns discrete RGB colors to a land cover classification.
- Intended to drive consistent visualization of raster data by mapping each category to a specific color.

## Structure and Contents
- Interpolation: DISCRETE.
- Each line defines a class with:
  - Category ID
  - Red, Green, Blue, Alpha (RGBA)
  - Code number and textual description (e.g., 111 - Continuous urban fabric)
- Example entries:
  - 1,230,000,077,255, 111 - Continuous urban fabric
  - 2,255,000,000,255, 112 - Discontinuous urban fabric
  - 3,204,077,242,255, 121 - Industrial or commercial units
  - 4,204,000,000,255, 122 - Road and rail networks and associated land
  - 50,230,242,255,255, 995 - UNCLASSIFIED WATER BODIES
  - 255,255,255,255,255, 990 - UNCLASSIFIED
- The file covers a broad suite of land cover classes, from urban areas and infrastructure to various agricultural, forest, vegetation, and water/sea classes.

## Classes Included (representative scope)
- Urban and built environments: continuous and discontinuous urban fabric, industrial/commercial units, road/rail networks, port areas, airports.
- Natural/man-made land uses: mineral extraction sites, dump sites, construction sites, green urban areas, sport facilities.
- Agriculture and vegetation: various arable lands, irrigated lands, rice fields, vineyards, orchards, pastures, different crop patterns, agro-forestry.
- Forests and vegetation types: broad-leaved, coniferous, mixed forests; natural grasslands; moors/heathlands; various vegetation types.
- Transitional and landscape features: transitional woodland-shrub, complex cultivation patterns, areas with agriculture and natural vegetation.
- Water and coastal features: water courses, water bodies, coastal lagoons, estuaries, sea/ocean.
- Special categories: inland marshes, peat bogs, salt marshes, salines, intertidal flats.
- Other: beaches/dunes, bare rocks, sparsely vegetated areas, burnt areas, glaciers/snow.
- Data hygiene categories: NODATA, UNCLASSIFIED LAND SURFACE, UNCLASSIFIED WATER BODIES, UNCLASSIFIED.

## Practical Value for Data Leaders
- Enables consistent, shareable visualization standards across projects and partners.
- Supports clear interpretation and communication of land cover data to policy colleagues and stakeholders.
- Facilitates metadata and discoverability by pairing color semantics with each class.
- Provides a ready-to-use legend for map production, aiding dissemination and reporting.

## Governance and Integration Considerations
- Treat as part of the data asset’s visualization metadata; ensure versioning and documentation of class definitions.
- Align with existing data standards and metadata schemas to support interoperability across networks.
- Consider data quality and completeness, especially for classes with granular or sparse representation.
- Use the UNCLASSIFIED/NODATA classes to handle missing or unspecified areas consistently.