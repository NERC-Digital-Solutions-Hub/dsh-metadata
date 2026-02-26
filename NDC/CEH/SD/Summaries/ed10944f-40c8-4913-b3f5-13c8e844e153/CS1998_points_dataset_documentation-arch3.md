# Landscape point feature data 1998 [Countryside Survey], Great Britain

## Overview
- Provides landscape point features from 538 1km squares across Great Britain sampled in 1998/99 (Countryside Survey).
- Data collected to support environmental monitoring, biodiversity assessment, and landscape-related decision making.
- Dataset is © NERC - Centre for Ecology & Hydrology; requires acknowledgement in all uses.
- Contains a wide range of attributes describing land use, vegetation, veteran trees, epiphytes, canopy cover, and landscape classifications, linked to regional context (country, county, environmental zones, land class).

## Data structure and key fields
- Location and identification
  - SQUARE: 1km square site code
  - YEAR: year of survey
  - ID: landscape point identifier (unique within a year)
- Thematic and attribute codes
  - THEME / THEME_NAME: theme code and description
  - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME: primary attribute code and description
  - SPECIES / SPECIES_NAME; PROPORTION / PROPORTION_RANGE: species data and cover estimates
  - USE / USE_NAME: structures theme land use
- Habitat and vegetation indicators
  - EPIPHYTE_COVER / EPIPHYTE_COVER_NAME: epiphytic cover
  - IVY_COVER / IVY_COVER_RANGE: ivy cover
  - CANOPY_LIVE / CANOPY_LIVE_RANGE: percent canopy live
  - VETERAN_TREE_TYPE / VETERAN_TREE_TYPE_NAME: veteran tree type
  - TREE_DEAD / DEAD_WOOD / DEAD_MISSING_BARK / HOLLOW_TRUNK: veteran tree condition indicators
  - MODAL_DBH / MODAL_DBH_RANGE: modal diameter at breast height
  - MISSING_LIMBS: veteran tree limb status
- Landscape classification and geography
  - LC07 / LC07_NUM: ITE Land Classification (GB 2007)
  - COUNTRY / COUNTY07: country and administrative area
  - EZ_DESC_07: environmental zone description
- Additional context
  - BUFFER: buffer around veteran tree or pond
  - LIGHTNING_STRIKES, etc.: additional site characteristics
- Data quality and interoperability
  - Data includes coded values with human-readable names, facilitating interpretation and integration with other Countryside Survey datasets and land classifications.

## Data provenance, access, and references
- Source: Countryside Survey (GB), compiled by NERC Centre for Ecology & Hydrology.
- Timeframe: survey conducted in 1998/99.
- Usage requirements: All use must acknowledge Countryside Survey data; copyright and database rights apply.
- References and related materials:
  - Countryside Survey website (general overview and methodologies)
  - ITE Merlewood Land Classification references (Bunce et al. 1996; 1981)
  - JNCC guidance documents on habitat classifications (Jackson 2000)
  - ITE Land Classification GB 2007 dataset (Bunce et al. 2007)
  - DOIs and links provided for datasets and publications in the references section

## Usage, sharing, and governance
- Acknowledgement and copyright notice must accompany all copies, publications, and presentations.
- Data sharing and openness are framed as part of data governance, with explicit emphasis on attribution and data origin.
- Potential barriers for monitoring work (contextual relevance):
  - The dataset is historical (1998/99) and may require integration with more recent data for trend analyses.
  - Metadata completeness and consistent codes across time are important for longitudinal monitoring.
  - Public sharing of underlying data necessitates careful governance and documentation.

## Relevance to monitoring framework authors
- Provides a rich, standardized set of landscape features and attributes suitable for developing environmental health indicators at broad scales (1km grid, GB coverage).
- Supports assessments of habitat structure (canopy, veteran trees, epiphytes), land use, and landscape classification, enabling policy evaluation and reporting.
- Facilitates cross-walks with land classifications (ITE LC07/LC07_NUM) and environmental zone descriptors for integrated monitoring.
- Highlights data governance needs (acknowledgement, provenance, metadata quality) that are critical when commissioning or integrating monitoring datasets.