# Landscape point feature data 1998 [Countryside Survey], Great Britain

- A dataset of landscape point features from 538 1km squares across Great Britain, sampled in 1998/99 as part of Countryside Survey.
- Data are © NERC - Centre for Ecology & Hydrology; intended for map-based data products and GIS analyses.

## Data structure and contents

- Core identifiers and location
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey
  - ID: Landscape point identifier (unique within a year)
- Thematic and attribute information
  - THEME / THEME_NAME: Theme code and name
  - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME: Primary attribute code and name
  - SPECIES / SPECIES_NAME: Species code and name
  - PROPORTION / PROPORTION_RANGE: Species cover code and range
  - USE / USE_NAME: Structures theme land use
  - BUFFER: Buffer around veteran tree or pond
- Veteran tree features
  - TREE_DEAD, MISSING_LIMBS, DEAD_WOOD, DEAD_MISSING_BARK, LIGHTNING_STRIKES, HOLLOW_TRUNK
  - MODAL_DBH / MODAL_DBH_RANGE: Modal diameter at breast height and range
  - VETERAN_TREE_TYPE / VETERAN_TREE_TYPE_NAME: Veteran tree type code and name
- Additional flora and canopy indicators
  - EPIPHYTE_COVER / EPIPHYTE_COVER_NAME: Epiphytic species cover
  - IVY_COVER / IVY_COVER_RANGE: Ivy cover code and range
  - CANOPY_LIVE / CANOPY_LIVE_RANGE: Percent canopy live
- Classification and location context
  - LC07 / LC07_NUM: ITE Land Classification of Great Britain 2007
  - COUNTRY: England, Scotland, or Wales
  - COUNTY07: County or Council
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Documentation note
  - All use of Countryside Survey data must be acknowledged with the provided attribution and copyright statement

## Spatial scope and sampling

- Geographic scope: Great Britain
- Sampling scale: 1km square resolution, 538 squares
- Temporal scope: Survey conducted in 1998/99

## Data quality, standards and considerations for GIS use

- Data are code-based with textual name fields to aid interpretation; several fields require reference tables/lookup datasets to resolve codes (e.g., THEME, SPECIES, CANOPY_LIVE, LC07).
- Data designed to be combined or layered with other Countryside Survey outputs (e.g., Land Classification LC07) for richer map products.
- Users should be aware of potential inconsistencies across years or datasets when integrating with other sources; appropriate joins and data cleaning may be required.

## How to use in GIS and map products

- Suitable for map-based visualizations of habitat features, veteran trees, epiphyte/ivy cover, and canopy density across the landscape.
- Can be enriched by linking to lookup tables for readable names and to supplementary classifications (e.g., LC07) for thematic mapping.
- Useful for spatial analyses at the 1km grid scale, such as distribution of veteran trees, species cover, and land-use patterns.

## Licensing, attribution and provenance

- Countryside Survey data must be acknowledged in all copies, publications, and presentations.
- Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
- Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- References and publications are provided to support methodologies and interpretation (see citations below).

## References and sources

- Countryside Survey Website: general overview and methodologies
- Bunce et al. 1996; ITE Merlewood Land Classification of Great Britain
- Bunce et al. 2007; ITE Land Classification of Great Britain 2007
- Jackson 2000; Guidance on Biodiversity Broad Habitat Classification
- Additional documentation and data centre links (DOIs and URLs provided)