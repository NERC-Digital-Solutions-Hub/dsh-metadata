# Landscape linear feature data 1984 [Countryside Survey], Great Britain

## Overview
- A dataset from the Countryside Survey detailing landscape linear features sampled in 1984 across 230 1km squares in Great Britain.
- Contains two components: (1) landscape linear features attributes and (2) species composition within woody linear features.
- Data are prepared for analysis of landscape structure, vegetation attributes, and associated environmental classifications.

## Data tables and fields

- Landscape linear features (LANDSCAPE_LINEAR_FEATURES_1984.csv)
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey (1984)
  - LINEAR_ID: Feature identifier (unique within a year)
  - EVENT_ID: Feature event identifier (unique within a year)
  - EVENT_FROM / EVENT_TO: Start and end positions along the feature (in metres)
  - THEME / THEME_NAME: Theme code and descriptive name
  - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME: Primary attribute code and description
  - HEIGHT / HEIGHT_RANGE: Height code and description
  - BASE_HEIGHT / BASE_HEIGHT_RANGE: Base height code and description
  - WIDTH / WIDTH_RANGE: Width code and description
  - MODAL_DBH / MODAL_DBH_RANGE: Modal diameter at breast height code and description
  - CONDITION / CONDITION_DESCRIPTION: Condition code and description
  - HISTORIC_MANAGEMENT: Signs of historic management
  - EVIDENCE_MANAGEMENT / EVIDENCE_MGT_DESCRIPTION: Evidence of management codes and descriptions
  - STAKED_TREES: Presence/absence of staked trees
  - TREE_PROTECTORS: Presence/absence of tree protectors
  - LINE_STUMPS: Presence/absence of a line of stumps
  - VERTICAL_GAPPINESS / VERTICAL_GAPPINESS_RANGE: Vertical gappiness code and description
  - MARGIN_WIDTH_LEFT / MARGIN_WIDTH_LEFT_RANGE: Left margin width code and description
  - MARGIN_WIDTH_RIGHT / MARGIN_WIDTH_RIGHT_RANGE: Right margin width code and description
  - SPECIES_COMPOSITION / SPECIES_COMP_DESCRIPTION: Species composition code and description
  - LC07 / LC07_NUM: ITE Land Classification of Great Britain 2007 codes
  - COUNTRY: Country (England ENG, Scotland SCO, Wales WAL)
  - COUNTY07: County or Council
  - EZ_DESC_07: Countryside Survey Environmental Zone description

- Species composition (embedded within the same feature table structure)
  - SQUARE / EVENT_ID / YEAR: Identifiers linking to the feature
  - SPECIES / SPECIES_NAME: Species code and name
  - PROPORTION / PROPORTION_RANGE: Proportion code and description
  - LC07 / LC07_NUM: ITE Land Classification codes
  - COUNTRY / COUNTY07 / EZ_DESC_07: Geographic/context descriptors

## Spatial and temporal scope
- Year of survey: 1984
- Geographic coverage: Great Britain (England, Scotland, Wales)
- Sampling design: 230 1km square sampling sites; landscape linear features identified within each square
- Identifiers (LINEAR_ID, EVENT_ID) are unique within a given year

## Data rights, citation, and provenance
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Copyright: Countryside Survey © NERC - Centre for Ecology & Hydrology. All rights reserved.
- References and publication guidance are provided to support interpretation and citation.

## References and sources
- Countryside Survey website: general overview and methodologies
- ITE Land Classification of Great Britain (1996, 1981; 2007 release)
  - Bunce et al. (1996) Journal of Biogeography: ITE Merlewood Land Classification
  - Bunce et al. (1981) Merlewood R&D Paper No. 86
  - Bunce et al. (2007) ITE Land Classification of Great Britain 2007
- Jackson (2000): Guidance on biodiversity broad habitat classification
- Data citations and DOIs/links are provided in the references section
- Data archive and metadata are associated with NERC CEH and Countryside Survey materials

## Alignment with analytical aims
- Enables analysis of correlations between landscape linear feature characteristics (height, width, condition, management signals, margins, staked trees, etc.) and land classification (LC07) or environmental zone descriptors (EZ_DESC_07).
- Supports examination of species composition within Woody Linear Features (WLF) and how it relates to feature attributes and landscape context.
- Facilitates descriptive statistics, cross-tabulations, and potential modeling of the likely impact of management practices or environmental classifications on feature structure and composition.
- Documentation and cross-references (ITE LC07, EZ_DESC_07) aid in mapping features to broader landscape classifications for comparative analyses across GB.