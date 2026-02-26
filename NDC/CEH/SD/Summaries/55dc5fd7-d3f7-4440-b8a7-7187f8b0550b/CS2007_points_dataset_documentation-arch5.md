# Landscape point feature data 2007 [Countryside Survey], Great Britain

## Overview
- Dataset describing landscape point features from 566 1km squares across Great Britain, sampled in 2007.
- File: LANDSCAPE_PT_FEATURES_2007.csv
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology
- Version: 1; Date: 04-2-2016

## Data structure and contents
- Spatial and temporal identifiers
  - SQUARE: 1km square sampling site code (text)
  - YEAR: Year of survey (number)
  - ID: Landscape point identifier (number; unique within a year)
- Thematic and attribute fields
  - THEME, THEME_NAME: Theme code and description
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME: Primary attribute code and label
  - SPECIES, SPECIES_NAME: Species code and name
  - PROPORTION, PROPORTION_RANGE: Species cover code and textual range
  - USE, USE_NAME: Structures theme land use
- Feature specifics and condition
  - BUFFER: Buffer around veteran tree or pond
  - TREE_DEAD, MISSING_LIMBS, DEAD_WOOD, DEAD_MISSING_BARK, LIGHTNING_STRIKES, HOLLOW_TRUNK
  - MODAL_DBH, MODAL_DBH_RANGE: Modal diameter at breast height and range
  - VETERAN_TREE_TYPE, VETERAN_TREE_TYPE_NAME: Veteran tree type and label
  - EPIPHYTE_COVER, EPIPHYTE_COVER_NAME: Epiphytic cover code and label
  - IVY_COVER, IVY_COVER_RANGE: Ivy cover code and range
  - CANOPY_LIVE, CANOPY_LIVE_RANGE: Percent canopy live code and range
- Classification and geography
  - LC07, LC07_NUM: ITE Land Classification 2007
  - COUNTRY: Country (England ENG, Scotland SCO, Wales WAL)
  - COUNTY07: County or council area
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Documentation and references
  - Notes that data usage requires acknowledgement
  - Links to related publications and methodologies

## Access, usage, and governance
- Data ownership and rights
  - Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - All CS data must be acknowledged in any use
  - Copyright: Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Acknowledgement requirements
  - Exact wording to be used on all copies, publications, and presentations:
    - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
- Documentation and references
  - Countryside Survey Website: general project overview and methodologies
  - Key publications related to land classification and biodiversity classifications (e.g., ITE Land Classification GB 1996/2007, JNCC guidance)
  - DOIs and links provided in the official metadata

## Data quality, standards, and stewardship considerations
- Complex, multi-code structure (themes, attributes, species, environmental classifications) requiring careful metadata mapping and consistent coding when integrating with other datasets
- Compatibility across many codes and ranges (e.g., PROPORTION, CANOPY_LIVE, DBH ranges) necessitates robust data dictionaries and validation routines
- Documentation of provenance and versioning critical for reproducibility (Version 1: 04-2-2016)
- Suitable for enabling discovery and reuse by data users, provided metadata is complete and acknowledgment requirements are followed

## References and related resources
- Countryside Survey Website: general overview and methodologies
- Bunce et al. (1996, 2007): ITE Land Classification of Great Britain
- Jackson (2000): Guidance on Biodiversity Broad Habitat Classification
- Additional references and DOIs listed in the dataset documentation for deeper methodological context

## Practical notes for data stewards
- Ensure metadata remains aligned with dataset contents (columns, codes, and ranges)
- Enforce and communicate the proper acknowledgment requirement in all downstream uses
- Maintain links to cited references and any updated classifications or revisions
- Provide clear guidance on how to interpret multi-code fields when sharing with data users across systems