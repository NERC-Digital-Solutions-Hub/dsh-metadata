# Landscape area data 1998 [Countryside Survey], Great Britain

## Overview
- Provides areas of Broad and Priority Habitats from 569 1km squares across Great Britain, sampled in 1998 as part of the Countryside Survey.
- Data owned by NERC - Centre for Ecology & Hydrology; two CSV files accompany the dataset:
  - LANDSCAPE_AREA_FEATURE_HAB_1998.csv (habitat area per 1km square)
  - LANDSCAPE_AREA_FEATURE_ATT_1998.csv (additional attributes for areas within the same squares)

## Data files and key fields

- LANDSCAPE_AREA_FEATURE_HAB_1998.csv
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey
  - ID: Landscape area polygon identifier (unique within a year)
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad/Priority Habitat name (Jackson, 2000)
  - AREA: Area of habitat within the 1km square (square metres)
  - LC07 / LC07_NUM: ITE Land Class 2007 code and number
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY: County (England & Wales) or Council (Scotland)
  - EZ_DESC_07: Countryside Survey Environmental Zone description

- LANDSCAPE_AREA_FEATURE_ATT_1998.csv
  - YEAR, SQUARE, ID: as above
  - THEME, THEME_NAME: Theme code and description (land use)
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME: Primary attribute code and description
  - SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME: Species-related data and cover values
  - PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME: Primary qualifier description
  - STRUCTURE_USE, STRUCTURE_USE_NAME: Structure use code and description
  - PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME: Inland physiography cover description
  - ROAD_VERGE_A, ROAD_VERGE_A_NAME; ROAD_VERGE_B, ROAD_VERGE_B_NAME: Road verge attributes
  - MOSAIC_PRECENT_AREA: Proportion of area assigned to Broad Habitat in a mosaic habitat
  - LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07: as above
  - Note: All use of Countryside Survey data must be acknowledged

## Classifications and standards
- Habitat classifications align with Broad Habitat (Jackson, 2000) and ITE Land Classification of Great Britain (ITE LC07, 2007).
- EZ_DESC_07 provides environmental zone context.

## Data provenance and usage
- Data collected as part of the Countryside Survey; intended for monitoring environmental health and policy performance over time.
- Outputs suitable for maps, charts, and standardized reports to illustrate habitat distribution and changes across GB.
- Data can be linked to other environmental attributes (land use, physiography, road verges, mosaic habitats) for integrated analyses.

## Data rights, acknowledgement, and references
- All Countryside Survey data must be acknowledged in usage.
- Required acknowledgement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
- Copyright notice: Countryside Survey © NERC- Centre for Ecology & Hydrology. All rights reserved.
- Relevant references and links included (publications describing methodologies and classifications):
  - Countryside Survey website (general overview and methodologies)
  - Bunce et al. (1996, 2007): ITE Land Classification of Great Britain
  - Jackson (2000): Guidance on Biodiversity Broad Habitat Classification
  - Additional documentation and DOIs/links provided for datasets and classifications

## Relevance for monitoring and policy analysis
- Provides standardized, geo-referenced habitat area data across GB for a single year (1998), enabling trend analysis when combined with future cycles.
- Supports environmental health assessments by quantifying habitat extent within defined 1km squares and linking to land classification and environmental zone descriptors.
- Facilitates broader data integration by including rich attribute fields (land use themes, species, physiography, road verges, mosaic areas) to contextualize habitat data.

## Potential uses and considerations
- Ideal for creating maps and charts of habitat extent by square, year-over-year comparisons, and cross-tabulations with LC07 classifications.
- Useful for policy performance monitoring, landscape-scale analyses, and environmental envelope assessments.
- Considerations: dataset represents 1998 sampling; ensure appropriate acknowledgment and integrate with subsequent Countryside Survey cycles for temporal analyses.