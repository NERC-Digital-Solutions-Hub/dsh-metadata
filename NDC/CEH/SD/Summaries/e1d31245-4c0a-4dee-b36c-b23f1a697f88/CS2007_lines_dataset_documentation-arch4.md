# Landscape linear feature data 2007 [Countryside Survey], Great Britain

- Landscape linear features from 442 1km squares across Great Britain, as sampled in 2007.
- Data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey ©.
- File: LANDSCAPE_LINEAR_FEATURES_2007.csv detailing feature attributes and species composition.

## Data structure and content

- Feature data (per linear feature):
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey (2007)
  - LINEAR_ID: Landscape linear feature identifier (unique within a year)
  - EVENT_ID: Landscape linear feature event identifier (unique within a year)
  - EVENT_FROM / EVENT_TO: Start and end positions along the feature (metres)
  - THEME / THEME_NAME: Theme codes and names
  - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME
  - HEIGHT / HEIGHT_RANGE
  - BASE_HEIGHT / BASE_HEIGHT_RANGE
  - WIDTH / WIDTH_RANGE
  - MODAL_DBH / MODAL_DBH_RANGE
  - CONDITION / CONDITION_DESCRIPTION
  - HISTORIC_MANAGEMENT / EVIDENCE_MANAGEMENT / EVIDENCE_MGT_DESCRIPTION
  - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS
  - VERTICAL_GAPPINESS / VERTICAL_GAPPINESS_RANGE
  - MARGIN_WIDTH_LEFT / MARGIN_WIDTH_LEFT_RANGE
  - MARGIN_WIDTH_RIGHT / MARGIN_WIDTH_RIGHT_RANGE
  - SPECIES_COMPOSITION / SPECIES_COMP_DESCRIPTION
  - LC07 / LC07_NUM (ITE Land Classification of Great Britain 2007)
  - COUNTRY (England, Scotland, Wales)
  - COUNTY07
  - EZ_DESC_07 (Countryside Survey Environmental Zone description)

- Species data (per feature event):
  - SQUARE / YEAR / EVENT_ID
  - SPECIES / SPECIES_NAME
  - PROPORTION / PROPORTION_RANGE
  - LC07 / LC07_NUM
  - COUNTRY / COUNTY07
  - EZ_DESC_07

- Notes:
  - LINEAR_ID is unique within a year; EVENT_ID likewise unique within a year.
  - Data uses coded attribute schemes (e.g., height, width, DBH, margins, etc.) and ITE Land Classification (LC07).

## Metadata, rights, and provenance

- All use of Countryside Survey data must be acknowledged with:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Relevant sources and references for context and methodology:
  - Countryside Survey website (general overview and methodologies)
  - Bunce et al. (1996, 1981, 2007) on ITE Land Classification of Great Britain
  - Jackson (2000) guidance on Biodiversity Broad Habitat Classification
  - DOI and links for ITE Land Classification of Great Britain 2007 dataset: 10.5285/5f0605e4-aa2a-48ab-b47c-bf5510823e8f
  - Additional publications and documentation accessible via the Countryside Survey website

## Practical considerations for data governance and reuse

- Data can support spatial and ecological analyses of landscape linear features and species composition at 1km-square resolution for 2007.
- The dataset integrates feature-level attributes with species composition within the ITE land classification framework, enabling cross-referencing with land cover and habitat classifications.
- Since the data are year-specific (2007) and feature IDs are year-scoped, cross-year analyses require careful harmonisation and metadata checks.
- Data quality and discoverability depend on consistent metadata, standardised codes (LC07, height/width categories, etc.), and adherence to the acknowledgement requirements.

## Relevance to data-leadership and strategy

- Demonstrates end-to-end data lifecycle: collection in the field, coding and attribute definitions, metadata standards, and licensing requirements.
- Illustrates the importance of clear attribution, provenance links, and methodological references when sharing datasets externally.
- Highlights the need for data standards, documentation, and user guidance to support co-ownership and effective dissemination of data products.
- Provides a model for integrating structural feature data with taxonomic composition within a common land-classification framework, supporting broader data collaboration and reuse.