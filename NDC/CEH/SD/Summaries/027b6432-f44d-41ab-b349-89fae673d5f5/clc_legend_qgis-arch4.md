# QGIS Generated Color Map Export File

## Overview
- A QGIS color map export defining a discrete (INTERPOLATION:DISCRETE) color legend for a raster land-cover classification.
- Maps class IDs to specific RGBA colors and descriptive labels for visualization and interpretation.

## Data structure and contents
- Each line contains:
  - A class ID number
  - RGBA color values (Red, Green, Blue, Alpha)
  - A numeric code (sometimes shown after the color values)
  - A human-readable label describing the land-cover or data status
- Covers a wide range of land-cover types from urban fabric and infrastructure to agricultural, forest, grassland, water, coastal, and marine categories.
- Special classes included:
  - NODATA
  - UNCLASSIFIED LAND SURFACE
  - UNCLASSIFIED WATER BODIES
  - An additional UNCLASSIFIED category appears toward the end with a different numeric tag

## Key categories and examples
- Urban and infrastructure: Continuous urban fabric, Discontinuous urban fabric, Industrial/commercial units, Road and rail networks, Port areas, Airports
- Agriculture and grazing: Non-irrigated arable land, Permanently irrigated land, Rice fields, Vineyards, Fruit trees and berry plantations, Olive groves, Pastures, Annual crops, Complex cultivation patterns
- Natural and semi-natural: Broad-leaved forest, Coniferous forest, Mixed forest, Natural grasslands, Moors/heathland, Transitional woodland-shrub, Agro-forestry
- Open habitats and water: Beaches/dunes, Bare rocks, Sparsely vegetated areas, Water courses, Water bodies, Coastal lagoons, Estuaries, Sea/ocean
- Other: Burnt areas, Glaciers, Inland marshes, Peat bogs, Salt marshes, Salines, Intertidal flats
- High-level statuses: NODATA and UNCLASSIFIED categories for data quality and completeness

## Special considerations and metadata
- The export uses a discrete color scheme suitable for class-based raster visualization.
- Class IDs align with a structured hierarchy of land-cover types, facilitating cross-dataset consistency.
- Some codes for UNCLASSIFIED/NODATA appear with varying numeric tags, which may require harmonization if integrating with other datasets.

## Practical use for Data Leaders
- Supports consistent visualization and interpretation of land-cover datasets across teams and partner networks.
- Provides a clear legend that can be embedded in reports, dashboards, and map products, aiding user understanding and decision-making.
- Facilitates data governance by documenting exact color assignments and class labels alongside the raster product.
- Enables coordination with policy colleagues and other data users through shared color conventions and class definitions.

## Data quality, standards, and collaboration considerations
- Ensure alignment of class IDs and labels with any other datasets used in the organisation to avoid misinterpretation.
- Review for any inconsistencies in UNCLASSIFIED/NODATA codes when integrating with external sources.
- Maintain metadata about the data source, version, and any updates to the color map to support reproducibility.
- Consider establishing a community of practice around color legends and class definitions to reduce duplicated efforts and improve discoverability.