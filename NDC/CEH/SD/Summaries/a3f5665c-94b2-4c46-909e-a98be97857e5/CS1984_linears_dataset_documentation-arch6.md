# Landscape linear feature data 1984 [Countryside Survey], Great Britain

## Overview
- Source: Countryside Survey (NERC - Centre for Ecology & Hydrology), Great Britain.
- Timeframe: Survey year 1984.
- Geography: Landscape linear features sampled across 230 1km squares in Great Britain.
- Format: Data appears as a primary features table and a related species composition table (both in CSV format under LANDSCAPE_LINEAR_FEATURES_1984.csv).
- Purpose: Document landscape linear features and their attributes to support analysis, interpretation, and data-driven decision making.

## Data Structure and Key Fields

- Table 1: Landscape linear features
  - SQUARE: 1km square sampling site code.
  - YEAR: Year of survey.
  - LINEAR_ID: Feature identifier (unique within a year).
  - EVENT_ID: Feature event identifier (unique within a year).
  - EVENT_FROM / EVENT_TO: Start and end positions along the feature (in metres).
  - THEME / THEME_NAME: Theme code and descriptive name.
  - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME: Primary attribute code and description.
  - HEIGHT / HEIGHT_RANGE: Height code and descriptive range.
  - BASE_HEIGHT / BASE_HEIGHT_RANGE: Base height code and descriptive range.
  - WIDTH / WIDTH_RANGE: Width code and descriptive range.
  - MODAL_DBH / MODAL_DBH_RANGE: Modal diameter at breast height code and range.
  - CONDITION / CONDITION_DESCRIPTION: Condition code and description.
  - HISTORIC_MANAGEMENT / EVIDENCE_MANAGEMENT / EVIDENCE_MGT_DESCRIPTION: Historic and evidenced management indicators and descriptions.
  - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS: Presence/absence indicators for management features.
  - VERTICAL_GAPPINESS / VERTICAL_GAPPINESS_RANGE: Vertical gappiness code and description.
  - MARGIN_WIDTH_LEFT / MARGIN_WIDTH_LEFT_RANGE: Left margin width code and description.
  - MARGIN_WIDTH_RIGHT / MARGIN_WIDTH_RIGHT_RANGE: Right margin width code and description.
  - SPECIES_COMPOSITION / SPECIES_COMP_DESCRIPTION: Species composition code and description.
  - LC07 / LC07_NUM: ITE Land Classification 2007 codes.
  - COUNTRY (ENG/SCO/WAL): Country code.
  - COUNTY07: County or Council name.
  - EZ_DESC_07: Countryside Survey Environmental Zone description and link.

- Table 2: Species composition per Feature (per EVENT_ID context)
  - SQUARE: 1km square sampling site code.
  - EVENT_ID: Landscape linear feature event identifier (unique within a year).
  - YEAR: Year of survey.
  - SPECIES / SPECIES_NAME: Species code and name.
  - PROPORTION / PROPORTION_RANGE: Proportion code and descriptive range.
  - LC07 / LC07_NUM: ITE Land Classification code and number.
  - COUNTRY / COUNTY07 / EZ_DESC_07: Geographic context and environmental zone description.

- General notes
  - All use of Countryside Survey data must be acknowledged.
  - Acknowledgement text: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and copyright notice.

## How to Use / Data Products

- Self-serve data products
  - Create dashboards or pivot tables to explore patterns in linear features (length along grid, height/width, condition, management history) by square, country, or county.
  - Combine the linear features table with the species composition table to analyze how species distributions relate to structural attributes (height, width, canopy base, etc.) across squares.
- Data integration
  - Cross-walk with ITE Land Classification (LC07) and environmental zone descriptions for contextual analyses.
  - Potential to link to external datasets (e.g., other Countryside Survey datasets) via SQUARE, YEAR, and COUNTY07.
- Analysis ideas
  - Assess relationships between feature condition and management indicators.
  - Examine geographic variation in feature attributes (e.g., height, width, margins) across England, Scotland, and Wales.
  - Explore species composition patterns along linear features and their association with structural attributes.

## Access, Licensing and Acknowledgements

- Ownership and rights: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; all rights reserved.
- Usage requirements: Include the acknowledgement text on all copies, publications, and presentations.
- References and sources: Includes Countryside Survey website and ITE Land Classification publications; links provided within the dataset documentation.

## Practical Considerations for Data Support

- Data interpretation
  - Many attributes use coded values with corresponding descriptive ranges; users should consult the provided THEME_NAME, HEIGHT_RANGE, WIDTH_RANGE, etc., for interpretation.
  - Two linked tables require careful joining on keys (SQUARE, YEAR, EVENT_ID) and, in the second table, EVENT_ID along with SQUARE/YEAR.
- Data quality and completeness
  - Dataset spans 1km squares across GB for a single year (1984); when integrating with other years or datasets, be mindful of potential gaps or format differences.
- Documentation and provenance
  - Referential publications and methodology links are available for deeper understanding of classifications and context (ITE Land Classification 2007, biodiversity classifications, etc.).