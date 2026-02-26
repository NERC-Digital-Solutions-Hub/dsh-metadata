# QGIS Generated Color Map Export File

## Overview
- This is a discrete color map export used by QGIS to visualize land cover classifications.
- It uses the header "INTERPOLATION:DISCRETE" to indicate a non-gradual (categorical) color scheme.
- Each row defines a category with: index, RGB(A) color values, a numeric code, and a label.

## File Structure and Content
- Categories are listed from 1 to 50, each with a specific color and descriptive label.
- Examples of category mappings include:
  - 1:  Continuous urban fabric
  - 2:  Discontinuous urban fabric
  - 3:  Industrial or commercial units
  - 4:  Road and rail networks and associated land
  - 5:  Port areas
  - 6:  Airports
  - 7-9:  Mining, dump sites, construction sites
  - 10-11: Green urban areas; Sport and leisure facilities
  - 12-14: Agricultural lands (arable, irrigated, rice fields)
  - 15-17: Various crops and orchards (vineyards, fruit trees, olive groves)
  - 18-22: Agricultural land uses and agro-forestry
  - 23-25: Forest types (Broad-leaved, Coniferous, Mixed)
  - 26-29: Natural and semi-natural vegetation types (grasslands, moors, heathland, transitional woodland)
  - 30-33: Open/bare areas (beaches, rocks, sparsely vegetated)
  - 34-35: Natural features (burnt areas, glaciers/snow)
  - 35-37: Wetlands and related (inland marshes, peat bogs, salt marshes)
  - 38-43: Water-related features (salines, estuaries, sea/ocean)
  - 44-50: Water bodies and unclassified categories
- Special classes include:
  - 48: NODATA
  - 49: UNCLASSIFIED LAND SURFACE
  - 50: UNCLASSIFIED (and related entries 990/995 indicating UNCLASSIFIED WATER BODIES)

## Color and Code Details
- Each category line contains:
  - A category index (1–50)
  - RGBA color values (example: 230,0,77,255)
  - A numeric code (e.g., 111, 112, 121, … 523, 999)
  - A human-readable label describing the land cover or feature

## Relevance to Monitoring Frameworks
- Demonstrates a standardized data product for visualizing environmental health indicators across policies and dashboards.
- Supports clear communication of complex results by using distinct, predefined colors for each category, aiding stakeholder interpretation.
- Encapsulates a structured classification scheme that could be integrated into monitoring frameworks to ensure consistency across datasets, reports, and dashboards.

## Data Governance and Practical Considerations
- Importance for the monitoring authors to document metadata (category definitions, exact color values, and coding schemes) to enable provenance and reproducibility.
- The discrete color map must be maintained and updated in tandem with any changes to the classification scheme to avoid inconsistencies across systems.
- Potential data governance implications:
  - Ensuring open access to the color map and its mappings while controlling dataset provenance.
  - Handling UNCLASSIFIED/NODATA categories transparently in analyses and visualizations.
  - Addressing possible data silos by aligning this map with other datasets and metadata standards.