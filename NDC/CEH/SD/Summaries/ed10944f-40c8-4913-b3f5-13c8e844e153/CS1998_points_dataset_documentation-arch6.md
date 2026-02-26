# Landscape point feature data 1998 [Countryside Survey], Great Britain

## Overview
- Dataset of landscape point features from 538 1km squares across Great Britain, sampled in 1998/99.
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology.
- Purpose: Capture landscape feature information at point locations for broad ecological and land-use context.

## Data structure and contents
- File: LANDSCAPE_PT_FEATURES_1998.csv
- Key columns and meaning:
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey
  - ID: Landscape point identifier (unique within a year)
  - THEME and THEME_NAME: Theme code and descriptive name
  - PRIMARY_ATTRIBUTE and PRIMARY_ATTRIBUTE_NAME: Primary attribute code and description
  - SPECIES and SPECIES_NAME: Species code and name
  - PROPORTION and PROPORTION_RANGE: Species cover code and its range
  - USE and USE_NAME: Structures theme land use
  - BUFFER: Buffer around veteran tree or pond
  - VETERAN_TREE-related fields: TREE_DEAD, MISSING_LIMBS, DEAD_WOOD, DEAD_MISSING_BARK, LIGHTNING_STRIKES, HOLLOW_TRUNK
  - MODAL_DBH and MODAL_DBH_RANGE: Modal diameter at breast height (DBH) information
  - VETERAN_TREE_TYPE and VETERAN_TREE_TYPE_NAME: Veteran tree type code and name
  - EPIPHYTE_COVER and EPIPHYTE_COVER_NAME: Epiphytic cover code and description
  - IVY_COVER and IVY_COVER_RANGE: Ivy cover code and range
  - CANOPY_LIVE and CANOPY_LIVE_RANGE: Percent canopy live
  - LC07 and LC07_NUM: ITE Land Class 2007 classification
  - COUNTRY: Country (England ENG, Scotland SCO, Wales WAL)
  - COUNTY07: County or Council for location
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Data types: mix of numeric codes and text descriptions; many fields include both a code and a human-readable name.

## Data quality considerations
- Data comprises many coded attributes that require reference tables for full interpretation (e.g., THEME, SPECIES, CANOPY_LIVE, LC07).
- As with broader Countryside Survey data, potential data quality considerations include variability in data availability across squares and years, and the need for data cleaning and standardization when combining with other sources.

## Usage and applications
- Enables analysis of landscape features across Great Britain at a 1km scale, including veteran trees, canopy characteristics, epiphytic and ivy cover, land-use themes, and habitat classifications.
- Supports self-serve data exploration, dashboards, pivot tables, reports, and charts for end users.
- Useful for integrative analyses with other Countryside Survey data and classifications (e.g., ITE Land Classification, Biodiversity Broad Habitats).

## Attribution and licensing
- Acknowledgement required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Copyright: Countryside Survey © NERC-Centre for Ecology & Hydrology. All rights reserved.
- All uses must include the specified acknowledgement on copies, publications, and presentations.

## Related publications and references
- Countryside Survey Website (general overview and methodologies).
- ITE Merlewood Land Classification of Great Britain (1996) and related works describing land classification methods.
- Guidance on Biodiversity Broad Habitat Classification (terrestrial and freshwater) and its relationship to other classifications (e.g., JNCC reports).
- ITE Land Classification of Great Britain 2007 dataset (Bunce et al., 2007) with associated DOI/links.
- Additional resources and documents accessible via the Countryside Survey website.