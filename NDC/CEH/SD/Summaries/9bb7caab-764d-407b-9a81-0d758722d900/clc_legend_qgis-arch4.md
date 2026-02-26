# QGIS Generated Color Map Export File

## Overview
- A QGIS-generated color map export using discrete interpolation.
- Defines a color-coded scheme for multiple land-cover/land-use classes, mapped to numeric class IDs and descriptive labels.
- Includes 50 main classes plus special categories for unclassified data and other non-surface types.

## File Structure
- Each entry specifies:
  - A color in RGBA (Red, Green, Blue, Alpha)
  - A numeric class ID
  - A textual label describing the class
- The header indicates INTERPOLATION:DISCRETE, signaling distinct color steps for each class.

## Representative Classes Included
- 111 - Continuous urban fabric
- 112 - Discontinuous urban fabric
- 121 - Industrial or commercial units
- 122 - Road and rail networks and associated land
- 123 - Port areas
- 124 - Airports
- 131-132 - Mineral extraction and dump sites
- 133 - Construction sites
- 141-142 - Green urban areas; Sport and leisure facilities
- 211-213 - Various agricultural lands (non-irrigated arable, irrigated, rice fields)
- 221-223 - Permanent crops and related plantations (vineyards, fruit trees, olive groves)
- 231-243 - Agricultural areas with natural vegetation, agro-forestry, etc.
- 311-313 - Forest types (broad-leaved, coniferous, mixed)
- 321-324 - Natural grasslands, moors/heathland, transitional woodland-shrub
- 331-335 - Coastal/beach and barren/rocks/globally sparse areas
- 411-413 - Wetlands (inland marshes, peat bogs)
- 421-423 - Salt marshes, salines, intertidal flats
- 511-523 - Water-related features (water courses, water bodies, lagoons, estuaries, sea)
- 990-995 - UNCLASSIFIED categories (LAND SURFACE, WATER BODIES)

## Practical Uses for Data Leaders
- Provides a standardized visual encoding for geospatial datasets, aiding cross-team consistency.
- Supports effective data product development by aligning color semantics with class definitions.
- Facilitates quick visual interpretation of land-use/land-cover patterns in dashboards, reports, and maps.

## Governance and Data Quality Considerations
- Ensure the color map aligns with the dataset’s class definitions and any external standards used across the organization.
- Maintain metadata linking class IDs to their descriptions to support discoverability and reuse.
- Monitor for updates to class definitions or new categories, and version the color map accordingly.
- Verify compatibility with downstream visualizations and ensure that updates do not disrupt established visual mappings.