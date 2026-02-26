# Landscape linear feature data 1998 [Countryside Survey], Great Britain

- The dataset documents landscape linear features sampled in 1998 across 412 1km squares in Great Britain.
- Source and rights: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; acknowledgement required on all copies and outputs.

## Data scope and contents

- File: LANDSCAPE_LINEAR_FEATURES_1998.csv
- Features covered: Landscape linear features within 1km sampling squares, sampled in 1998.
- Geography: Great Britain (England, Scotland, Wales) across 412 1km squares.
- Temporal coverage: Year of survey is 1998 (YEAR).
- Feature identifiers:
  - SQUARE: 1km square sampling site code
  - LINEAR_ID: feature identifier (unique within a year)
  - EVENT_ID: feature event identifier (unique within a year)
  - EVENT_FROM / EVENT_TO: start and end positions along the linear feature (metres)
- Feature attributes (selected examples):
  - THEME / THEME_NAME, PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME
  - HEIGHT / HEIGHT_RANGE, BASE_HEIGHT / BASE_HEIGHT_RANGE
  - WIDTH / WIDTH_RANGE
  - MODAL_DBH / MODAL_DBH_RANGE
  - CONDITION / CONDITION_DESCRIPTION
  - HISTORIC_MANAGEMENT / EVIDENCE_MANAGEMENT / EVIDENCE_MGT_DESCRIPTION
  - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS
  - VERTICAL_GAPPINESS / VERTICAL_GAPPINESS_RANGE
  - MARGIN_WIDTH_LEFT / MARGIN_WIDTH_LEFT_RANGE
  - MARGIN_WIDTH_RIGHT / MARGIN_WIDTH_RIGHT_RANGE
  - SPECIES_COMPOSITION / SPECIES_COMP_DESCRIPTION
  - LC07 / LC07_NUM (ITE Land Classification 2007)
  - COUNTRY, COUNTY07, EZ_DESC_07
- Species-related data (per event or segment):
  - SQUARE, EVENT_ID, YEAR
  - SPECIES / SPECIES_NAME
  - PROPORTION / PROPORTION_RANGE
  - LC07 / LC07_NUM
  - COUNTRY, COUNTY07, EZ_DESC_07

## Data structure and coverage details

- Two related data blocks within the dataset:
  - Landscape linear feature attributes (feature-level details for each linear feature)
  - Species composition attributes (species codes/names and their proportions within features)
- Classification and geography:
  - ITE Land Classification (LC07) linked to GB classifications
  - Country and county-level geographic fields
  - Countryside Survey Environmental Zone (EZ_DESC_07)
- Acknowledgement requirement: All use of Countryside Survey data must be acknowledged using provided wording.

## Data quality, provenance and references

- Data are produced as part of the Countryside Survey program and follow standardized methodologies.
- Key references and sources for methodology and classification:
  - Countryside Survey project overview and methodologies
  - ITE Merlewood Land Classification (GB) and 2007 update
  - Guidance on biodiversity broad habitats and related classifications (JNCC/JNCC-typologies)
- Publications and links provided for deeper methodological context and dataset descriptions.

## Use, outputs and integration

- Intended uses align with monitoring environmental health and policy performance over time.
- Typical outputs include clear formats such as reports, maps, and charts that summarise environmental features and their attributes.
- Data can be quality-assured, transformed, and integrated with other datasets to increase value beyond single-use applications.
- Datasets should be stored and uploaded to appropriate portals as part of routine data management.

## Access, rights and acknowledgements

- Acknowledgement and copyright notice must accompany all copies, publications, and presentations:
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## Relevant publications and references

- Countryside Survey website and linked methodologies
- ITE Land Classification of Great Britain (1996, 2007)
- Guidance on interpretation of Biodiversity Broad Habitat Classification (JNCC, 2000)
- Additional supporting documents and DOIs/links provided for dataset usage and classification details