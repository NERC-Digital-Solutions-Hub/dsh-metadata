# Landscape linear feature data 2007 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey (GB, 2007) describing landscape linear features sampled in 442 1km squares across Great Britain.
- Contains two related components: (1) landscape linear features attributes and measurements; (2) species composition associated with each linear feature event.
- Aimed at enabling map-based visualization and spatial analysis of woody linear features, their attributes, and associated species.

## Data structure and key fields

- Landscape linear features (per feature event)
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey (2007)
  - LINEAR_ID: Landscape linear feature identifier (unique within a year)
  - EVENT_ID: Landscape linear feature event identifier (unique within a year)
  - EVENT_FROM / EVENT_TO: Start and end positions along the linear feature (metres)
  - THEME / THEME_NAME: Theme code and descriptive name
  - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME: Primary attribute code and description
  - HEIGHT / HEIGHT_RANGE: Height code and description
  - BASE_HEIGHT / BASE_HEIGHT_RANGE: Base height code and description
  - WIDTH / WIDTH_RANGE: Width code and description
  - MODAL_DBH / MODAL_DBH_RANGE: Modal diameter at breast height (DBH) code and description
  - CONDITION / CONDITION_DESCRIPTION: Condition code and description
  - HISTORIC_MANAGEMENT / EVIDENCE_MANAGEMENT / EVIDENCE_MGT_DESCRIPTION: Signs of historic and present management
  - STAKED_TREES / TREE_PROTECTORS / LINE_STUMPS: Presence/absence indicators for staked trees, tree protectors, and stumps
  - VERTICAL_GAPPINESS / VERTICAL_GAPPINESS_RANGE: Vertical gaps in woody linear feature
  - MARGIN_WIDTH_LEFT / MARGIN_WIDTH_LEFT_RANGE: Left margin width code and description
  - MARGIN_WIDTH_RIGHT / MARGIN_WIDTH_RIGHT_RANGE: Right margin width code and description
  - SPECIES_COMPOSITION / SPECIES_COMP_DESCRIPTION: Species composition code and description
  - LC07 / LC07_NUM: ITE Land Classification (GB 2007) and numeric code
  - COUNTRY: Country within GB (ENG / SCO / WAL)
  - COUNTY07: County or council area
  - EZ_DESC_07: Countryside Survey Environmental Zone description

- Species composition (per event)
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey (2007)
  - EVENT_ID: Landscape linear feature event identifier (unique within a year)
  - SPECIES / SPECIES_NAME: Species code and name
  - PROPORTION / PROPORTION_RANGE: Proportion code and descriptive range
  - LC07 / LC07_NUM: ITE Land Classification (GB 2007) and numeric code
  - COUNTRY / COUNTY07: Geographical location
  - EZ_DESC_07: Environmental Zone description

- General notes
  - All use of Countryside Survey data must be acknowledged (see copyright/acknowledgement below).

## Spatial and temporal coverage
- Year of survey: 2007
- Geographic extent: Great Britain (England, Scotland, Wales)
- Sampling unit: 1km squares; 442 squares sampled

## Data use, acknowledgment, and licensing
- Acknowledgement requirements
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Data usage: Acknowledgement must be used on copies, publications, reports, and presentations.

## References and references to methodologies
- Countryside Survey Website: general overview and methodologies
- Bunce et al. (1996, 1981) Merlewood ITE Land Classification references
- Jackson (2000) Biodiversity Broad Habitat Classification guidance
- Bunce et al. (2007) ITE Land Classification of Great Britain 2007 (dataset reference and DOI)
- Additional links and DOIs provided in the dataset notes

## Practical GIS considerations
- Use for map-based visualization of woody linear features and their attributes across GB at the 2007 snapshot.
- Features are identified by LINEAR_ID within each YEAR; EVENT_FROM/TO denote linear segment extents in metres, suitable for rendering as lines within each SQUARE.
- Two-part dataset: main linear feature attributes and per-event species composition; can be joined on SQUARE, YEAR, and EVENT_ID.
- LC07 classifications enable thematic mapping of land classes alongside linear features.
- Coordinate-free representation (per-square data); may require spatial joining to 1km square polygons or integration with other GB land cover layers for full map contexts.

## Caveats and data quality
- Data may come from multiple sources and resolutions; harmonization may be needed for cross-dataset analysis.
- Some fields use coded values with accompanying descriptive ranges; careful decoding required for accurate interpretation.
- The 2007 snapshot may not reflect changes in subsequent years; longitudinal analyses require additional years of data (if available).