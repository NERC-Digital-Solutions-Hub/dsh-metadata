# Landscape linear feature data 1984 [Countryside Survey], Great Britain

## Overview
- Dataset derived from the Countryside Survey (1984) across 230 1km squares in Great Britain.
- File: LANDSCAPE_LINEAR_FEATURES_1984.csv containing feature-level and, separately, species-level attributes.
- Source and rights: Countryside Survey data © NERC - Centre for Ecology & Hydrology; CEH dataset curated and versioned (as of 04-02-2016).

## Data structure and fields
- Feature-level attributes (one row per landscape linear feature per square/year):
  - SQUARE, YEAR, LINEAR_ID (unique within a year), EVENT_ID (unique within a year)
  - EVENT_FROM, EVENT_TO (start/end positions in metres)
  - THEME, THEME_NAME; PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME
  - HEIGHT, HEIGHT_RANGE; BASE_HEIGHT, BASE_HEIGHT_RANGE
  - WIDTH, WIDTH_RANGE
  - MODAL_DBH, MODAL_DBH_RANGE
  - CONDITION, CONDITION_DESCRIPTION
  - HISTORIC_MANAGEMENT; EVIDENCE_MANAGEMENT, EVIDENCE_MGT_DESCRIPTION
  - STAKED_TREES; TREE_PROTECTORS; LINE_STUMPS
  - VERTICAL_GAPPINESS, VERTICAL_GAPPINESS_RANGE
  - MARGIN_WIDTH_LEFT, MARGIN_WIDTH_LEFT_RANGE
  - MARGIN_WIDTH_RIGHT, MARGIN_WIDTH_RIGHT_RANGE
  - SPECIES_COMPOSITION, SPECIES_COMP_DESCRIPTION
  - LC07, LC07_NUM (ITE Land Classification 2007)
  - COUNTRY, COUNTY07
  - EZ_DESC_07 (Countryside Survey Environmental Zone description)
- Species-level attributes (linked by SQUARE, EVENT_ID, YEAR):
  - SPECIES, SPECIES_NAME
  - PROPORTION, PROPORTION_RANGE
  - LC07, LC07_NUM
  - COUNTRY, COUNTY07
  - EZ_DESC_07

## Access, usage and attribution
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- References and methodology materials are available via the Countryside Survey website and related publications (ITE Land Classification); citations and links provided with the dataset.

## References and provenance
- Countryside Survey Website: General overview and methodologies.
- ITE Merlewood Land Classification of Great Britain (1996) and related documents (LC07 descriptions and updates).
- JNCC guidance and other biodiversity classification references (2000) linked to LC07 and habitat concepts.
- Persistent identifiers and DOIs available for key publications (as provided in the dataset documentation).

## Relevance for monitoring frameworks
- Demonstrates a structured, codified dataset for environmental health monitoring:
  - Spatially explicit: ties features to 1km squares and geographic identifiers (COUNTRY, COUNTY07).
  - Temporally explicit: year (1984) with event-level delineations along linear features.
  - Rich attribute set: physical (height, width, base height), condition and management history, presence of supports (stakes, protectors), vegetation attributes (species composition), and land classification codes (LC07).
  - Interoperability: uses standard classifications (ITE LC07) and environmental zone descriptions (EZ_DESC_07), enabling integration with other monitoring datasets.
  - governance and provenance: clear ownership, copyright, and citation requirements, with published references to methodologies.

## Considerations and limitations
- Temporal scope is a single historical year (1984); not a current time series by itself, though compatible with other Countryside Survey data.
- Data use requires explicit acknowledgement, which can influence dissemination practices.
- The dataset uses coded fields (themes, attributes, classifications) and requires mapping to human-readable terms for interpretation.
- Metadata sufficiency for all users depends on access to the accompanying documentation and referenced publications.
- Transformation or harmonisation may be needed to integrate with modern data formats or other GB-wide environmental datasets.