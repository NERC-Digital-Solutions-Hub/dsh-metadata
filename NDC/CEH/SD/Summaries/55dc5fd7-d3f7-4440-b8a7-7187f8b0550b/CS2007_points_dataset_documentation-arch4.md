# Landscape point feature data 2007 [Countryside Survey], Great Britain

## Overview
- A dataset of landscape point features collected in 566 1km squares across Great Britain during the 2007 Countryside Survey.
- Data are owned by NERC - Centre for Ecology & Hydrology (CEH); copyright and acknowledgement requirements apply.
- Contains a wide range of landscape attributes at point locations, including species presence/cover, veteran tree characteristics, land use, and landscape classification codes.

## Data structure and key fields
- Spatial and sampling identifiers:
  - SQUARE: 1km square site code
  - YEAR: survey year
  - ID: landscape point identifier (unique within a year)
- Thematic and attribute details:
  - THEME and THEME_NAME
  - PRIMARY_ATTRIBUTE and PRIMARY_ATTRIBUTE_NAME
  - SPECIES and SPECIES_NAME
  - PROPORTION and PROPORTION_RANGE (species cover)
  - USE and USE_NAME (Structures land use)
  - BUFFER, TREE_DEAD, MISSING_LIMBS, DEAD_WOOD, DEAD_MISSING_BARK, LIGHTNING_STRIKES, HOLLOW_TRUNK
  - VETERAN_TREE_TYPE and VETERAN_TREE_TYPE_NAME
  - MODAL_DBH and MODAL_DBH_RANGE
  - EPIPHYTE_COVER and EPIPHYTE_COVER_NAME
  - IVY_COVER and IVY_COVER_RANGE
  - CANOPY_LIVE and CANOPY_LIVE_RANGE
- Classification and geography:
  - LC07 and LC07_NUM (ITE Land Classification 2007)
  - COUNTRY and COUNTY07
  - EZ_DESC_07 (Environmental Zone description)
- Data quality and usability:
  - Many fields use codes with accompanying descriptive names; users should reference metadata for interpretation and any updates.

## Provenance, licensing and references
- Acknowledgement and copyright:
  - Acknowledge Countryside Survey data owned by NERC - CEH; “Countryside Survey ©” and database rights apply.
- References and documentation:
  - Countryside Survey website and methodology documents
  - ITE Land Classification of Great Britain (Bunce et al. 1996; 2007)
  - Guidance on Biodiversity Broad Habitat Classification (Jackson 2000)
  - Related NERC Environmental Information Data Centre records and DOIs

## Data quality, access and governance
- Data quality considerations:
  - Data are collected per year and per 1km square; ID is unique within a year, which affects cross-year linkage.
  - Several attributes rely on coded values requiring reference tables for interpretation (e.g., THEME, SPECIES, CANOPY_LIVE, LC07 codes).
- Access and usage governance:
  - Data must be used with proper acknowledgment language; copyright protections apply.
  - Useful alongside other Countryside Survey data and external datasets for broader landscape and biodiversity analyses.

## Implications and guidance for Data Leaders
- Holistic data system view:
  - Integrate landscape point features with other Countryside Survey datasets (e.g., land classification, environmental zones) to support comprehensive analysis.
- Data discovery, standards and metadata:
  - Ensure metadata availability for code mappings (e.g., theme, species, land class) to improve discoverability and reuse.
  - Leverage LC07 and related classifications to harmonize with other GB datasets.
- Data quality and governance:
  - Track year-specific snapshots; plan for cross-year comparisons with consistent identifiers and provenance.
  - Maintain clear acknowledgment language in all outputs (publications, dashboards, presentations).
- Collaboration and stewardship:
  - Coordinate with the data community and CEH to align data products with user needs (policy colleagues, researchers, partners) and support co-ownership of data products.
  - Use as a foundation for developing richer, multi-source landscape data products with transparent lineage and quality indicators.

## Additional references and reading
- Countryside Survey website: general overview and methodologies
- Bunce et al. (1996, 2007): ITE Merlewood/GB Land Classification
- Jackson (2000): Guidance on Biodiversity Broad Habitat Classification
- NERC Environmental Information Data Centre entries for Countryside Survey datasets and DOIs