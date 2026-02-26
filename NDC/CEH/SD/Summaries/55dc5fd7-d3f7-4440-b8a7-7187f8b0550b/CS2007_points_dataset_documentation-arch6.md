# Landscape point feature data 2007 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey covering 566 1km squares across Great Britain, sampled in 2007.
- File: LANDSCAPE_PT_FEATURES_2007.csv
- Version: 1 (originally released 04-2-2016)
- Copyright: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; all rights reserved.

## File details and key columns
- Core identifiers:
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey
  - ID: Landscape point identifier (unique within a year)
- Thematic and attribute information:
  - THEME, THEME_NAME
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME
  - SPECIES, SPECIES_NAME
  - PROPORTION, PROPORTION_RANGE
  - EPIPHYTE_COVER, EPIPHYTE_COVER_NAME
  - IVY_COVER, IVY_COVER_RANGE
  - CANOPY_LIVE, CANOPY_LIVE_RANGE
  - USE, USE_NAME
  - BUFFER
- Veteran tree and condition indicators:
  - TREE_DEAD, MISSING_LIMBS, DEAD_WOOD, DEAD_MISSING_BARK
  - LIGHTNING_STRIKES, HOLLOW_TRUNK
  - MODAL_DBH, MODAL_DBH_RANGE
  - VETERAN_TREE_TYPE, VETERAN_TREE_TYPE_NAME
- Geographic and classification context:
  - LC07, LC07_NUM (ITE Land Classification 2007)
  - COUNTRY, COUNTY07
  - EZ_DESC_07 (Environmental Zone description)
- Data usage notes:
  - All use of Countryside Survey data must be acknowledged with the provided attribution text.

## Usage context and purpose
- Provides landscape point-level data with a rich set of habitat, vegetation, land-use, and veteran-tree attributes.
- Enables data products and analyses for broader exploration and self-serve access, consistent with Countryside Survey methodologies and classifications.
- Supports integration with other CS datasets and publications to describe GB countryside biodiversity and landscape structure.

## Data licensing and attribution
- Acknowledgement required: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
- Copyright: Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- The dataset is linked to multiple methodological and reference documents; users should cite relevant sources when publishing analyses.

## References and further reading
- Countryside Survey Website: general overview and methodologies
- Bunce et al. (1996, 2007): ITE Merlewood Land Classification of Great Britain; land classification context
- Jackson (2000): Guidance on Biodiversity Broad Habitat Classification interpretations
- NERC Environmental Information Centre: metadata and data centre references
- DOI/links provided in the document for the 2007 land classification dataset and related publications

## Notes for data support and integration
- The file contains coded fields (e.g., THEME, SPECIES, LC07) requiring lookup tables or documentation to interpret categories accurately.
- Ensure proper citation and attribution in any outputs or presentations that use this data.
- Consider cross-referencing with the Countryside Survey Environmental Zone descriptions and land classification documents for contextual interpretation.