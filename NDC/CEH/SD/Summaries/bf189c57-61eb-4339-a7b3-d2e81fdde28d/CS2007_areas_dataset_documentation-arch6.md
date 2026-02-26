# Landscape area data 2007 [Countryside Survey], Great Britain

## Overview
- Provides landscape-area data from 591 1km squares across Great Britain sampled in 2007.
- Excludes refused access areas.
- Two CSV files are included:
  - LANDSCAPE_AREA_FEATURE_HAB_2007.csv: habitat area by square.
  - LANDSCAPE_AREA_FEATURE_ATT_2007.csv: additional attributes for those areas.
- Data are from the Countryside Survey (© NERC - Centre for Ecology & Hydrology) and use is governed by acknowledgment requirements.

## Datasets and key fields

- LANDSCAPE_AREA_FEATURE_HAB_2007.csv (Habitat area within 1km squares)
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey
  - ID: Landscape area polygon identifier (unique within a year)
  - BROAD_HABITAT: Broad habitat code
  - BROAD_HABITAT_NAME: Broad/priority habitat name (Jackson, 2000)
  - AREA: Area of habitat within the 1km polygon (square metres)
  - LC07 / LC07_NUM: ITE Land Classification 2007
  - COUNTRY, COUNTY: Location metadata
  - EZ_DESC_07: Countryside Survey Environmental Zone description
  - Notes: Refused access areas excluded

- LANDSCAPE_AREA_FEATURE_ATT_2007.csv (Additional attributes per area)
  - YEAR, SQUARE, ID: Keys for joining with HAB file
  - THEME, THEME_NAME: Theme/land-use category
  - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME: Primary attribute coding and description
  - SPECIES / SPECIES_NAME / SPECIES_COVER / SPECIES_COVER_NAME: Species data and cover values
  - PRIMARY_QUALIFIER / PRIMARY_QUALIFIER_NAME: Qualifier details
  - STRUCTURE_USE / STRUCTURE_USE_NAME: Structure/use details
  - PHYSIOGRAPHY_COVER / PHYSIOGRAPHY_COVER_NAME: Physiography cover data
  - ROAD_VERGE_A / ROAD_VERGE_A_NAME: Road verge width category
  - ROAD_VERGE_B / ROAD_VERGE_B_NAME: Additional road verge attributes
  - MODAL_DBH / MODAL_DBH_NAME: Modal Diameter at Breast Height
  - MOSAIC_PRECENT_AREA: Proportion of area in mosaic habitat
  - LC07 / LC07_NUM: ITE Land Classification 2007 (for cross-reference)
  - COUNTRY, COUNTY: Location metadata
  - EZ_DESC_07: Environmental zone description

## How to use

- Link datasets by SQUARE, YEAR, and ID to combine habitat areas with their detailed attributes.
- Create data products (dashboards, pivot tables, maps) to enable self-serve exploration of habitat extent, land-use themes, and attribute distributions across GB.
- Useful for policy support, environmental zoning analyses, and habitat change assessments when combined with other Countryside Survey data.
- Follow acknowledgment requirements when publishing or presenting outputs.

## Data quality, constraints, and interpretation

- Coverage limited to 591 1km squares sampled in 2007; analyses should account for distribution and sampling design.
- Areas with access refusals excluded from the dataset.
- Data describe Broad/Priority habitats and a rich set of ancillary attributes, enabling multidimensional analyses but requiring careful interpretation of codes (LC07, THEME, etc.).

## Access and attribution

- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text:
  - Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Include appropriate citations and references as specified in the dataset documentation.

## References and further reading

- Countryside Survey Website: general overview and methodologies
- Bunce et al. (ITE Land Classification of Great Britain) and related publications
- Jackson (Guidance on Biodiversity Broad Habitat Classification)
- 2007 ITE Land Classification dataset references and DOIs
- Links to the NERC Environmental Information Data Centre records
- See also the Countryside Survey documentation for detailed methodologies and data dictionaries