# Landscape linear feature data 1990 [Countryside Survey], Great Britain

## Overview
- Dataset describing landscape linear features from 325 1km squares across Great Britain, sampled in 1990 as part of the Countryside Survey.
- Composed of two main data components: 
  - Landscape linear features attributes (spatial/feature-level data)
  - Species composition for each landscape linear feature event
- Dataset version: Version 1: 04-2-2016. Copyright: Countryside Survey data © NERC - Centre for Ecology & Hydrology.

## Data Structure and Key Fields
- Landscape linear features table:
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey
  - LINEAR_ID: Feature identifier (unique within a year)
  - EVENT_ID: Feature event identifier (unique within a year)
  - EVENT_FROM / EVENT_TO: Start and end of feature along the line (metres)
  - THEME / THEME_NAME: Theme code and description
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
  - LC07 / LC07_NUM (ITE Land Classification)
  - COUNTRY / COUNTY07
  - EZ_DESC_07
- Species composition table (per EVENT_ID):
  - SPECIES / SPECIES_NAME
  - PROPORTION / PROPORTION_RANGE
  - LC07 / LC07_NUM
  - COUNTRY / COUNTY07
  - EZ_DESC_07
- All codes have descriptive ranges or text descriptors to aid interpretation.
- Important constraint: LINEAR_ID and EVENT_ID are only unique within a given year.

## Data Quality, Standards, and Governance
- Uses ITE Merlewood Land Classification (LC07) as part of the data description and classification framework.
- Attributes rely on coded fields with accompanying descriptive ranges (e.g., HEIGHT, WIDTH, PROPORTION).
- Metadata includes environmental zone description (EZ_DESC_07) and references to established classifications and methodologies.
- Clear usage requirement: all uses must acknowledge Countryside Survey data and include the specified copyright notice.

## Access, Licensing, and Citations
- Acknowledgement requirement: 
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- References and publications section provides:
  - Countryside Survey website and methodology links
  - Key literature on ITE Land Classification and related classifications (Bunce et al. 1996, 2007; Jackson 2000)
  - DOI and links for the ITE Land Classification of Great Britain 2007 dataset

## Data Stewardship and Governance Actions
- Ingest into data catalog with mappings to a data dictionary for both feature-level and species composition tables.
- Attach the required acknowledgement text to metadata records and data products; ensure downstream users reproduce the proper citation.
- Maintain versioning and provenance notes (originating survey year: 1990; versioned metadata as of 2016-02-04).
- Document interpretation guidance for coded fields (LC07, PROPORTION, HEIGHT, etc.) and provide user-friendly definitions.
- Establish data access controls and any usage limitations tied to the Countryside Survey data.
- Consider periodic data quality checks and notes on any potential updates or errata related to the 1990 dataset.