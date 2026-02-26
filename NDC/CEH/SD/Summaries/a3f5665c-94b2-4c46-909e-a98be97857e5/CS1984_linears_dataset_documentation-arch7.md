# Landscape linear feature data 1984 [Countryside Survey], Great Britain

## Overview
- Dataset describing landscape linear features from 230 1km squares across Great Britain, sampled in 1984 (Countryside Survey).
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology.

## Data content and schema

- Primary dataset: LANDSCAPE_LINEAR_FEATURES_1984.csv
- Spatial unit and timing:
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey (1984)
- Feature identification:
  - LINEAR_ID: Landscape linear feature identifier (unique within a year)
  - EVENT_ID: Landscape linear feature event identifier (unique within a year)
  - EVENT_FROM / EVENT_TO: Start and end positions along the linear feature (in metres)
- Attribute group 1: Feature characteristics
  - THEME / THEME_NAME
  - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME
  - HEIGHT / HEIGHT_RANGE
  - BASE_HEIGHT / BASE_HEIGHT_RANGE
  - WIDTH / WIDTH_RANGE
  - MODAL_DBH / MODAL_DBH_RANGE
  - CONDITION / CONDITION_DESCRIPTION
  - HISTORIC_MANAGEMENT
  - EVIDENCE_MANAGEMENT / EVIDENCE_MGT_DESCRIPTION
  - STAKED_TREES
  - TREE_PROTECTORS
  - LINE_STUMPS
  - VERTICAL_GAPPINESS / VERTICAL_GAPPINESS_RANGE
  - MARGIN_WIDTH_LEFT / MARGIN_WIDTH_LEFT_RANGE
  - MARGIN_WIDTH_RIGHT / MARGIN_WIDTH_RIGHT_RANGE
  - SPECIES_COMPOSITION / SPECIES_COMP_DESCRIPTION
  - LC07 / LC07_NUM (ITE Land Classification 2007)
  - COUNTRY / COUNTY07
  - EZ_DESC_07 (Environmental Zone description)
- Attribute group 2: Species composition (within linear features)
  - SPECIES / SPECIES_NAME
  - PROPORTION / PROPORTION_RANGE
  - LC07 / LC07_NUM
  - COUNTRY / COUNTY07
  - EZ_DESC_07
- Rights and usage:
  - All use of Countryside Survey data must be acknowledged.

## Spatial and domain context

- Features mapped as linear elements within 1km square sampling units.
- Attributes support map-based visualization of woody linear features and their characteristics (height, width, DBH, condition, management indicators, margins, gaps, species composition).
- Contextual codes included: LC07 (ITE Land Classification 2007), country, county, and environmental zone descriptions.

## Data quality, limitations, and considerations

- IDs (LINEAR_ID, EVENT_ID) are unique only within a given year; cross-year integration requires careful handling.
- Data reflect the 1984 Countryside Survey, with potential limitations in resolution, standardization, and completeness.
- Data span multiple attributes that may require cleaning or harmonization for integrated GIS analyses.

## Usage notes and citations

- Acknowledgement requirement for CS data: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and copyright notice.
- References and methodological context available through the Countryside Survey website and associated literature (ITE Land Classification, JNCC guidance, etc.).

## Practical notes for GIS workflows

- Suitable for creating map-based visualizations of woody linear features along 1km grids.
- Use SQUARE and YEAR to join with other 1km grid data; line features are defined by EVENT_FROM to EVENT_TO along each linear feature.
- Leverage attributes for thematic mapping (e.g., height, width, DBH, condition, management signs, margins, vertical gaps, species composition) and for filtering (e.g., by LC07, country, EZ_DESC_07).