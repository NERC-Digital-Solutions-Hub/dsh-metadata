# Landscape area data 1984 [Countryside Survey], Great Britain

## Overview
- Provides areas of Broad and Priority Habitats from 379 1km squares across Great Britain, sampled in 1984.
- Two CSV files cover habitat areas and additional attributes, with extensive metadata and cross-links to classification schemes.
- Data owned by NERC - Centre for Ecology & Hydrology; 1984 Countryside Survey data are © and must be acknowledged in all uses.

## Data files and structure
- LANDSCAPE_AREA_FEATURE_HAB_1984.csv
  - Core habitat areas per 1km square
  - Key columns include SQUARE, YEAR, ID, BROAD_HABITAT, BROAD_HABITAT_NAME, AREA, LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07
- LANDSCAPE_AREA_FEATURE_ATT_1984.csv
  - Additional attributes for areas within the 1km squares
  - Columns include YEAR, SQUARE, ID, THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME, SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME, PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME, STRUCTURE_USE, STRUCTURE_USE_NAME, PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME, ROAD_VERGE_A, ROAD_VERGE_A_NAME, ROAD_VERGE_B, ROAD_VERGE_B_NAME, MODAL_DBH, MODAL_DBH_NAME, LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07
- Acknowledgement and copyright
  - All use of Countryside Survey data must be acknowledged with the provided text.
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © - Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## Key fields and data semantics
- SQUARE: 1km square sampling site code (text)
- YEAR: Year of survey (numeric)
- ID: Landscape area polygon identifier (unique within a year)
- HAB file specific
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad and Priority Habitat name (Jackson, 2000)
  - AREA: Area of habitat within the 1km polygon (square metres)
  - LC07, LC07_NUM: ITE Land Classification 2007 codes
  - COUNTRY, COUNTY: Location metadata
  - EZ_DESC_07: Environmental Zone description
- ATT file specific
  - THEME, THEME_NAME: Theme/land-use descriptions
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME: Primary attribute and description
  - SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME: Species-related data
  - PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME: Qualifier details
  - STRUCTURE_USE, STRUCTURE_USE_NAME: Structure use information
  - PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME: Physiography-related coverage
  - ROAD_VERGE_A, ROAD_VERGE_A_NAME; ROAD_VERGE_B, ROAD_VERGE_B_NAME: Road verge descriptors
  - MODAL_DBH, MODAL_DBH_NAME: Modal Diameter at Breast Height
  - LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07: Classification and location fields (aligned with HAB data)

## Data accuracy, provenance and governance
- Provenance: Countryside Survey data from 1984, with linkage to ITE Land Classification (1996/2007) and biodiversity broad habitat references.
- Classification crosswalks: Includes LC07 codes and names, and references to broad habitat and environmental zone descriptions.
- Temporal and spatial scope: Historical snapshot from 1984 across 379 1km squares in Great Britain.
- Data quality considerations for stewards: Recognize potential need to harmonize legacy classifications with newer schemes; ensure consistent use of SQUARE, YEAR, and ID across HAB and ATT files; verify alignment of LC07 and EZ_DESC_07 with related documentation.
- Usage constraints: Proper acknowledgment in all copies, publications, and presentations; rights reserved by NERC-CEH.

## Usage, attribution, and references
- Acknowledgement requirement: Include the specified Countryside Survey acknowledgement in all outputs.
- References and publications
  - Countryside Survey Website (general overview and methodologies)
  - Bunce et al. (1996, 2007) on ITE Land Classification of Great Britain
  - Jackson (2000) on Biodiversity Broad Habitat Classification
  - NERC Environmental Information Data Centre entries for ITE Land Classification 2007
- Links provided for further details and methodologies (Countryside Survey website and referenced papers).