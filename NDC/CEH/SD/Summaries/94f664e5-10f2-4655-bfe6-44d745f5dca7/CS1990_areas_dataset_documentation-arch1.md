# Landscape area data 1990 [Countryside Survey], Great Britain

## Overview
- Two CSV datasets covering landscape area features from Countryside Survey in 1990 across 506 1km squares in Great Britain.
- Files:
  - LANDSCAPE_AREA_FEATURE_HAB_1990.csv: areas of Broad and Priority Habitats within each 1km square.
  - LANDSCAPE_AREA_FEATURE_ATT_1990.csv: additional attributes for those areas.
- Purpose: quantify habitat areas and associated attributes to support analysis of landscape structure, land use, and ecological characteristics at a 1km scale.

## Data files and key fields
- LANDSCAPE_AREA_FEATURE_HAB_1990.csv
  - SQUARE: 1km square sampling site code
  - YEAR: survey year (1990)
  - ID: polygon identifier (unique within a year)
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad/ Priority Habitat name
  - AREA: habitat area within the 1km square (square metres)
  - LC07: ITE Land Class 2007 code
  - LC07_NUM: ITE Land Class 2007 number
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY: county or council
  - EZ_DESC_07: environmental zone description
- LANDSCAPE_AREA_FEATURE_ATT_1990.csv
  - YEAR, SQUARE, ID: identifiers
  - THEME, THEME_NAME: theme and description (land use)
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME: primary attribute codes and descriptions
  - SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME: species and their cover values
  - PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME: qualifiers for attributes
  - STRUCTURE_USE, STRUCTURE_USE_NAME: structure/theme use descriptions
  - PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME: physiography-related cover descriptions
  - ROAD_VERGE_A, ROAD_VERGE_A_NAME; ROAD_VERGE_B, ROAD_VERGE_B_NAME: road verge attributes
  - MODAL_DBH, MODAL_DBH_NAME: modal DBH (diameter at breast height) descriptor
  - LC07, LC07_NUM: ITE Land Class 2007 codes and numbers
  - COUNTRY, COUNTY: location indicators
  - EZ_DESC_07: environmental zone description

## Coverage, scope, and classifications
- Coverage: 506 1km squares across Great Britain surveyed in 1990.
- Classifications included:
  - Broad Habitat (with Broad Habitat name)
  - ITE Land Classification (LC07) 2007 codes for cross-year comparability
  - Country and County metadata
  - Environmental Zone description (EZ_DESC_07)

## Data usage and attribution
- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement text:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey ©; all rights reserved
- Acknowledgement must appear on all copies, publications, reports, and presentations.

## Relevance for analysis and modeling
- Enables spatial analysis of habitat extent and distribution at 1km resolution.
- Facilitates correlations between habitat area (AREA) and land classification (LC07), environmental zones (EZ_DESC_07), and geographic location (COUNTRY, COUNTY).
- The ATT dataset provides rich attributes (themes, species, structure use, physiography, road verges, DBH) for deeper ecological analyses and modeling.

## References and additional resources
- Countryside Survey website and methodologies for project context.
- Key publications and datasets related to ITE Land Classification and Broad Habitat interpretations (e.g., Bunce et al., Jackson 2000).
- Data access and usage guidance are provided by the Countryside Survey portal and associated metadata.

## Practical notes for analysts
- Treat 1990 as a historical baseline; consider cross-year comparability when integrating with later periods.
- When combining HAB and ATT datasets, align on SQUARE and ID to link habitat areas with their attributes.
- Use LC07 and EZ_DESC_07 codes to standardize analyses across regions and land classes.
- Attribute data properly in all outputs and be mindful of dataset scope and year limitations.