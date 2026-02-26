# Landscape linear feature data 1998 [Countryside Survey], Great Britain

## Overview
- A Countryside Survey data product from 1998, covering landscape linear features sampled across 412 1km squares in Great Britain.
- Data version: 1: 04-2-2016. © NERC - Centre for Ecology & Hydrology.
- Intended for GIS-based map visualisations and analysis of woody linear features within the Countryside Survey framework.
- Data are presented with attribution and are derived from multiple sources and classifications (notably ITE Land Classification).

## Data scope and structure
- Two related tabular components are provided:
  - Linear feature attributes (per event) for each 1km square, including geometry along the feature and a suite of descriptive attributes.
  - Species composition attributes linked to each linear feature event (per species, within the same square/event context).
- Coverage details:
  - Landscape linear features sampled within 412 1km squares across Great Britain.
  - Each linear feature event is defined by spatial context within a 1km square and by a start (EVENT_FROM) and end (EVENT_TO) position along the feature (metres).
- Key fields in the Linear Feature table (SQUARE to EZ_DESC_07):
  - SQUARE, YEAR, LINEAR_ID, EVENT_ID, EVENT_FROM, EVENT_TO
  - THEME, THEME_NAME
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME
  - HEIGHT, HEIGHT_RANGE, BASE_HEIGHT, BASE_HEIGHT_RANGE
  - WIDTH, WIDTH_RANGE
  - MODAL_DBH, MODAL_DBH_RANGE
  - CONDITION, CONDITION_DESCRIPTION
  - HISTORIC_MANAGEMENT, EVIDENCE_MANAGEMENT, EVIDENCE_MGT_DESCRIPTION
  - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS
  - VERTICAL_GAPPINESS, VERTICAL_GAPPINESS_RANGE
  - MARGIN_WIDTH_LEFT, MARGIN_WIDTH_LEFT_RANGE
  - MARGIN_WIDTH_RIGHT, MARGIN_WIDTH_RIGHT_RANGE
  - SPECIES_COMPOSITION, SPECIES_COMP_DESCRIPTION
  - LC07, LC07_NUM
  - COUNTRY, COUNTY07
  - EZ_DESC_07
- Key fields in the Species Composition table (aligned with SQUARE, EVENT_ID, YEAR context):
  - SPECIES, SPECIES_NAME, PROPORTION, PROPORTION_RANGE
  - LC07, LC07_NUM
  - COUNTRY, COUNTY07
  - EZ_DESC_07

## Data usage and GIS considerations
- The dataset is designed to support map-based visualization of woody linear features and their attributes across GB.
- Attribute-rich features enable thematic mapping (e.g., by THEME, HEIGHT, WIDTH, DBH, CONDITION) and by management signals (historic/evidence of management).
- Species composition data allow per-feature, per-species mapping and aggregation (e.g., proportions of species within a woody linear feature).
- Country and administrative context (COUNTRY, COUNTY07) support regional analyses and layering with administrative boundaries.
- ITE Land Classification references (LC07, LC07_NUM) provide a standardized ecological classification context for each feature.
- Environmental context (EZ_DESC_07) supports environmental zone-based filtering or symbolization.
- Limitations for GIS mapping:
  - Geometry is defined in terms of start/end positions along a feature within a 1km square; precise spatial geometry across GB likely requires additional geospatial references beyond the tabular data.
  - The dataset reflects a snapshot from 1998; historical analyses should account for temporal changes when combining with newer data.

## Acknowledgement and licensing
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text to use on copies, publications, presentations:
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## References and further information
- Countryside Survey Website: general overview and methodologies
- Bunce, R.G.H., Barr, C.J., Clarke, R.T., Howard, D.C. & Lane, A.M.J. (1996) ITE Merlewood Land Classification of Great Britain
- Bunce, R.G.H., Barr, C.J., Whittaker, H.A. (1981) Land Classes in Great Britain: Preliminary Descriptions for Users of the Merlewood Method
- Jackson, D.L. (2000) Guidance on the interpretation of the Biodiversity Broad Habitat Classification
- Bunce, R.G.H.; Barr, C.J.; Clarke, R.T.; Howard, D.C.; Scott, W.A. (2007) ITE Land Classification of Great Britain 2007
- Countryside Survey data citations and DOIs/links via the CEH/NERC data centre and associated publications.