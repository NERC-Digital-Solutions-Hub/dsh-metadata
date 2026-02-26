# Landscape linear feature data 1998 [Countryside Survey], Great Britain

## Overview
- Landscape linear features sampled in 1998 from 412 1km squares across Great Britain.
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology.
- All use of Countryside Survey data must be acknowledged with the provided attribution.

## Data content and structure
- File: LANDSCAPE_LINEAR_FEATURES_1998.csv
- Two linked sets of columns:
  - Feature-level attributes for each landscape linear feature
  - Species composition for each feature (per year, per event)

## Key fields and what they capture

### Feature attributes (Landscape linear feature)
- SQUARE: 1km square sampling site code
- YEAR: Year of survey (1998)
- LINEAR_ID: Unique landscape linear feature identifier within a year
- EVENT_ID: Feature event identifier within a year
- EVENT_FROM / EVENT_TO: Start and end positions along the feature in metres
- THEME / THEME_NAME: Theme code and descriptive name
- PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME: Primary attribute code and description
- HEIGHT / HEIGHT_RANGE: Height code and descriptive range
- BASE_HEIGHT / BASE_HEIGHT_RANGE: Base height code and descriptive range
- WIDTH / WIDTH_RANGE: Width code and descriptive range
- MODAL_DBH / MODAL_DBH_RANGE: Modal diameter at breast height code and description
- CONDITION / CONDITION_DESCRIPTION: Condition code and description
- HISTORIC_MANAGEMENT: Signs of historic management
- EVIDENCE_MANAGEMENT / EVIDENCE_MGT_DESCRIPTION: Evidence of management and description
- STAKED_TREES: Presence/absence of staked trees
- TREE_PROTECTORS: Presence/absence of tree protectors
- LINE_STUMPS: Presence/absence of line of stumps
- VERTICAL_GAPPINESS / VERTICAL_GAPPINESS_RANGE: Vertical gaps in Woody Linear Feature and its range
- MARGIN_WIDTH_LEFT / MARGIN_WIDTH_LEFT_RANGE: Left margin width code and description
- MARGIN_WIDTH_RIGHT / MARGIN_WIDTH_RIGHT_RANGE: Right margin width code and description
- SPECIES_COMPOSITION / SPECIES_COMP_DESCRIPTION: Species composition code and description
- LC07 / LC07_NUM: ITE Land Classification 2007 and numeric code
- COUNTRY: Country of the 1km square (England ENG, Scotland SCO, Wales WAL)
- COUNTY07: County (or Council in Scotland)
- EZ_DESC_07: Countryside Survey Environmental Zone description (with link to description)

### Species composition (per feature/event)
- SQUARE: 1km square sampling site code
- EVENT_ID: Landscape linear feature event identifier (year-unique)
- YEAR: Year of survey
- SPECIES: Species code
- SPECIES_NAME: Species name
- PROPORTION / PROPORTION_RANGE: Proportion code and descriptive range
- LC07 / LC07_NUM: ITE Land Classification 2007 and numeric code
- COUNTRY: Country (ENG, SCO, WAL)
- COUNTY07: County (or Council)
- EZ_DESC_07: Countryside Survey Environmental Zone description

## Spatial and temporal coverage
- Spatial: Great Britain, across 412 sampled 1km squares
- Temporal: Data from the 1998 Countryside Survey year

## Usage, attribution, and references
- Data use must acknowledge Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Acknowledge with: Countryside Survey data owned by NERC - Centre for Ecology & Hydology. Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Relevant references and sources:
  - Countryside Survey website and general methodology
  - ITE Merlewood Land Classification of Great Britain (1996, 1981)
  - ITE Land Classification of Great Britain 2007 (Bunce et al.)
  - Guidance on Biodiversity Broad Habitat Classification (Jackson, 2000)
  - NERC Environmental Information Data Centre records for the GB land classification dataset
- Links and DOIs provided in the dataset metadata for the classification references

## Practical notes for analysts
- Each LINEAR_ID and EVENT_ID are unique within a single year; cross-year merging should align on SQUARE, YEAR, and EVENT_ID where appropriate.
- The dataset integrates feature attributes with species composition, enabling analyses of structure, composition, and relationships to land classification.
- Be mindful of the coding schemes (HEIGHT, WIDTH, DBH, PROPORTION, etc.) and use the accompanying RANGE descriptions for interpretation.
- When combining with other datasets, ensure consistent COUNTRY/COUNTY07 and EZ_DESC_07 classifications.