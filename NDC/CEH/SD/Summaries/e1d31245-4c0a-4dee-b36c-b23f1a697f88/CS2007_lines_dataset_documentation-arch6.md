# Landscape linear feature data 2007 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey, Great Britain, year 2007.
- Landscape linear features sampled across 442 1km squares.
- Data © NERC - Centre for Ecology & Hydrology.
- Intended to support analysis of woody linear features (WLFs) and their characteristics, with accompanying species information.

## Data structure and key fields
- Landscape linear features table (per 1km square and feature event)
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey (2007)
  - LINEAR_ID: Feature identifier (unique within a year)
  - EVENT_ID: Feature event identifier (unique within a year)
  - EVENT_FROM / EVENT_TO: Start and end of feature along the linear (in metres)
  - THEME / THEME_NAME: Theme code and description
  - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME: Primary attribute code and description
  - HEIGHT / HEIGHT_RANGE: Height code and range
  - BASE_HEIGHT / BASE_HEIGHT_RANGE: Base height code and range
  - WIDTH / WIDTH_RANGE: Width code and range
  - MODAL_DBH / MODAL_DBH_RANGE: Modal diameter at breast height (DBH) code and range
  - CONDITION / CONDITION_DESCRIPTION: Condition code and description
  - HISTORIC_MANAGEMENT / EVIDENCE_MANAGEMENT / EVIDENCE_MGT_DESCRIPTION: Signs of historic/evidence of management
  - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS: Presence/absence indicators
  - VERTICAL_GAPPINESS / VERTICAL_GAPPINESS_RANGE: Vertical gappiness code and range
  - MARGIN_WIDTH_LEFT / MARGIN_WIDTH_LEFT_RANGE: Left margin width code and range
  - MARGIN_WIDTH_RIGHT / MARGIN_WIDTH_RIGHT_RANGE: Right margin width code and range
  - SPECIES_COMPOSITION / SPECIES_COMP_DESCRIPTION: Species composition code and description
  - LC07 / LC07_NUM: ITE Land Classification 2007 codes
  - COUNTRY / COUNTY07: Country and administrative area
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Species composition table (per event)
  - SQUARE / YEAR / EVENT_ID: Link to feature event
  - SPECIES / SPECIES_NAME: Species code and name
  - PROPORTION / PROPORTION_RANGE: Species proportion code and range
  - LC07 / LC07_NUM / COUNTRY / COUNTY07 / EZ_DESC_07: Contextual classifications and location
- Use and attribution
  - All use of Countryside Survey data must be acknowledged with the provided statement.

## How to use and potential data products
- Self-serve data products:
  - Dashboards showing feature counts, lengths, and attributes by theme, country, and county.
  - Pivot tables summarising feature heights, widths, and DBH distributions.
  - Maps of linear features by square, with attribute-based filtering (e.g., height, width, condition).
- Analytical possibilities:
  - Explore relationships between feature morphology (height, width, DBH) and management signals or historical indicators.
  - Compare LC07 land classification with landscape linear feature characteristics.
  - Analyze species composition within linear features and link to environmental zones (EZ_DESC_07).
  - Assess spatial patterns and environmental contexts (COUNTRY, COUNTY07) of linear features.
- Data integration:
  - Combine with other Countryside Survey data or external datasets to enrich policy or planning analyses at local council or private sector levels.

## Data quality and caveats
- Year-limited: data correspond to survey conducted in 2007; temporal trends require additional years.
- Unique identifiers are defined within each year (LINEAR_ID, EVENT_ID), not across multiple years.
- Formats include multiple attribute encodings (codes and human-readable ranges); careful cross-walk may be needed for analysis.
- Some fields are descriptive codes with accompanying range descriptions; ensure correct interpretation for analyses.

## Licensing, acknowledgment, and access
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text to use on copies, publications, and presentations:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- The dataset references several publications and the Countryside Survey website for methodologies and classifications.

## References and further reading
- Countryside Survey Website: general overview and methodologies.
- Bunce et al. (1996, 1981) ITE Merlewood Land Classification of Great Britain – descriptions and relevance.
- Jackson (2000) Guidance on Biodiversity Broad Habitat Classification interpretation (JNCC Report 307).
- Bunce et al. (2007) ITE Land Classification of Great Britain 2007 – dataset and methodology.
- Data Centre references and DOIs for the ITE Land Classification 2007 dataset.