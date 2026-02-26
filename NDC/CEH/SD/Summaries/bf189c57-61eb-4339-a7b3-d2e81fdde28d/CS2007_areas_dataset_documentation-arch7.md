# Landscape area data 2007 [Countryside Survey], Great Britain

## Overview
- Two CSV data files documenting landscape habitat areas and attributes for 591 1km squares across Great Britain in 2007.
- Refused access areas are excluded.
- Data are owned by NERC - Centre for Ecology & Hydrology; Countryside Survey data. All uses must include the specified acknowledgement and copyright notice.
- Version: 1: 15-1-2016.

## Data structure and contents

- LANDSCAPE_AREA_FEATURE_HAB_2007.csv (Habitat areas)
  - SQUARE: 1km square sampling site code (text)
  - YEAR: Year of survey
  - ID: Landscape area polygon identifier (unique within a year)
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad and Priority Habitat name (Jackson, 2000)
  - AREA: Area of habitat within the 1km polygon (square metres)
  - LC07: ITE Land Class 2007 code (text)
  - LC07_NUM: ITE Land Class 2007 number
  - COUNTRY: Country (England ENG, Scotland SCO, Wales WAL)
  - COUNTY: County (England & Wales) or Council (Scotland)
  - EZ_DESC_07: Countryside Survey Environmental Zone description

- LANDSCAPE_AREA_FEATURE_ATT_2007.csv (Additional attributes)
  - YEAR, SQUARE, ID: Identifiers as above
  - THEME, THEME_NAME: Theme code and description (land use)
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME: Primary attribute code and description
  - SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME: Species-related information
  - PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME: Primary qualifier
  - STRUCTURE_USE, STRUCTURE_USE_NAME: Structure use details
  - PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME: Inland physiography cover description
  - ROAD_VERGE_A, ROAD_VERGE_A_NAME: Transport theme road verge A width
  - ROAD_VERGE_B, ROAD_VERGE_B_NAME: Transport theme road verge B width
  - MODAL_DBH, MODAL_DBH_NAME: Modal Diameter at Breast Height (DBH)
  - MOSAIC_PRECENT_AREA: Proportion of area assigned to Broad Habitat in a mosaic habitat
  - LC07, LC07_NUM: ITE Land Class 2007 codes (referencing HAB dataset)
  - COUNTRY, COUNTY: Geographic location details
  - EZ_DESC_07: Countryside Survey Environmental Zone description

## Key attributes and classifications
- Broad Habitat classification (BROAD_HABITAT, BROAD_HABITAT_NAME)
- ITE Land Classification 2007 (LC07, LC07_NUM)
- Environmental Zone description (EZ_DESC_07)
- Landscape detail attributes: species presence/cover, structure use, physiography, road verge characteristics, modal DBH, mosaic habitat proportion

## Spatial and temporal scope
- Year: 2007
- Geographic area: Great Britain (England, Scotland, Wales)
- Grid: 591 1km squares
- Administrative units: COUNTRY and COUNTY (or Council in Scotland)

## Data quality and usage notes
- All uses of Countryside Survey data require explicit acknowledgement of data ownership and copyright.
- Data provide per-square habitat areas and per-area attribute details suitable for GIS analyses of landscape composition, land-use classification, and habitat distribution.
- The ID field is unique within a year; cross-dataset joins should use SQUARE and ID (and YEAR) for alignment.

## Potential GIS applications
- Map-based visualization of habitat extent by 1km square and by Broad Habitat.
- Join HAB and ATT datasets to analyze habitat characteristics, land-use themes, and environmental zones.
- Analyze spatial patterns by LC07 land classes, mosaic habitat proportions, and physiography.
- Integrate with road verge attributes and DBH for forested or managed landscapes.
- Comparative analyses across 591 squares to assess landscape change or conservation prioritization.

## Access, licensing, and references
- Acknowledgement required: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Publications and references include:
  - Countryside Survey Website (overview and methodologies)
  - Bunce et al. (1996; 1981) ITE Merlewood Land Classification papers
  - Jackson (2000) guidance on Biodiversity Broad Habitat Classification
  - Bunce et al. (2007) ITE Land Classification of Great Britain 2007
- Link and DOIs provided in the references for deeper methodological context.