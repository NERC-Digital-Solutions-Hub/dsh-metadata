# Landscape area data 1990 [Countryside Survey], Great Britain

- 506 1km squares across Great Britain sampled in 1990
- Data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey ©

## Overview
- Provides areas of Broad and Priority Habitats within 1km sampling squares (GB, 1990)
- Two CSV files containing habitat areas and associated attributes
- Designed for GIS-based map visualisations and analysis of landscape habitats and related attributes

## File contents

- LANDSCAPE_AREA_FEATURE_HAB_1990.csv
  - Purpose: Areas of Broad and Priority Habitats within 1km squares
  - Key columns:
    - SQUARE: 1km square sampling site code
    - YEAR: survey year
    - ID: landscape area polygon identifier (unique within a year)
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad and Priority Habitat name
    - AREA: habitat area within the 1km polygon (square metres)
    - LC07, LC07_NUM: ITE Land Class 2007 codes
    - COUNTRY, COUNTY: location details
    - EZ_DESC_07: Environmental Zone description

- LANDSCAPE_AREA_FEATURE_ATT_1990.csv
  - Purpose: Additional attributes for areas within 1km squares
  - Key columns (selected):
    - YEAR, SQUARE, ID
    - THEME, THEME_NAME: thematic category and description (land use)
    - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME
    - SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME
    - PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME
    - STRUCTURE_USE, STRUCTURE_USE_NAME
    - PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME
    - ROAD_VERGE_A, ROAD_VERGE_A_NAME
    - ROAD_VERGE_B, ROAD_VERGE_B_NAME
    - MODAL_DBH, MODAL_DBH_NAME
    - LC07, LC07_NUM
    - COUNTRY, COUNTY
    - EZ_DESC_07

## Key fields and relationships
- Spatial unit: 1km square (SQUARE) with a polygon ID (ID) per year (YEAR)
- HAB file links habitat area (AREA) to habitat codes and landscape classifications (LC07)
- ATT file provides rich per-area attributes (themes, species, structure, physiography, road verge, DBH, etc.)
- Use SQUARE, YEAR, and ID to join HAB and ATT for complete per-area records

## How to use in GIS
- Join HAB_1990 and ATT_1990 on (YEAR, SQUARE, ID) to create a full per-area feature dataset
- Map habitat extents within 1km squares and classify by BROAD_HABITAT_NAME or LC07
- Use THEME_NAME, SPECIES_NAME, STRUCTURE_USE_NAME, and other attributes for thematic mapping and analysis
- Integrate with environmental zone (EZ_DESC_07) and location fields (COUNTRY, COUNTY) for regional analyses

## Data usage and acknowledgments
- All use of Countryside Survey data must be acknowledged
- Required acknowledgement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
- Copyright: Countryside Survey © NERC - Centre for Ecology & Hydrology. All rights reserved.
- Include above acknowledgment on copies, publications, reports, and presentations

## References and methodology
- Countryside Survey website and publications for project overview and methodologies
- ITE Land Classification of Great Britain (Bunce et al.)
- Guidance on Biodiversity Broad Habitat Classification (Jackson, 2000)
- ITE Land Classification 2007 dataset (Bunce et al., 2007)
- Related links and DOIs provided for deeper methodological context

## Practical notes
- Data resolution is 1km squares; consider aggregation when mapping at coarser scales
- Data may reference multiple classifications (LC07, EZ_DESC_07); ensure consistent cross-walking when integrating with other datasets
- Data quality and consistency challenges typical of large, multi-source eco-survey datasets; verify joins and metadata when integrating into workflows