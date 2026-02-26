# Landscape linear feature data 2007 [Countryside Survey], Great Britain

## Overview
- Dataset capturing landscape linear features from 442 1km squares across Great Britain, surveyed in 2007.
- Part of Countryside Survey data; owned by NERC - Centre for Ecology & Hydrology (CEH).
- Version: 1: 04-2-2016.
- All use of Countryside Survey data must be acknowledged using the specified acknowledgement text.

## Data structure and contents
- Two related datasets described:
  - Landscape linear features (per feature):
    - Key identifiers: SQUARE (1km square code), YEAR, LINEAR_ID (unique within a year), EVENT_ID (unique within a year).
    - Spatial/positional: EVENT_FROM and EVENT_TO (start/end along the feature in metres).
    - Attributes: THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME, HEIGHT, HEIGHT_RANGE, BASE_HEIGHT, BASE_HEIGHT_RANGE, WIDTH, WIDTH_RANGE, MODAL_DBH, MODAL_DBH_RANGE.
    - Condition and management: CONDITION, CONDITION_DESCRIPTION, HISTORIC_MANAGEMENT, EVIDENCE_MANAGEMENT, EVIDENCE_MGT_DESCRIPTION.
    - Feature characteristics: STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS, VERTICAL_GAPPINESS, VERTICAL_GAPPINESS_RANGE, MARGIN_WIDTH_LEFT, MARGIN_WIDTH_LEFT_RANGE, MARGIN_WIDTH_RIGHT, MARGIN_WIDTH_RIGHT_RANGE.
    - Composition and classification: SPECIES_COMPOSITION, SPECIES_COMP_DESCRIPTION, LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07.
  - Species composition (per feature per species):
    - Key identifiers: SQUARE, YEAR, EVENT_ID.
    - Species data: SPECIES (code), SPECIES_NAME, PROPORTION, PROPORTION_RANGE.
    - Classification and location context: LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07.
- Relationships: Species composition is linked to features via SQUARE, YEAR, and EVENT_ID.

## Data standards, provenance, and use
- Land classification: LC07 (ITE Land Classification 2007) and LC07_NUM present for cross-dataset interoperability.
- Geography: COUNTRY and COUNTY07 fields provide regional context; EZ_DESC_07 gives the Countryside Survey Environmental Zone description (with a referenced documentation link).
- Units and coding: Key measurements expressed with both numeric codes and human-readable ranges (e.g., HEIGHT, WIDTH, PROPORTION) and their corresponding RANGE fields.
- Uniqueness and scope: LINEAR_ID and EVENT_ID are unique within a given year, while SQUARE defines the sampling location.
- Documentation and references: Includes extensive references to Countryside Survey methodology and land classification literature (ITE Land Classification of Great Britain 2007; related JNCC and Biogeography sources).

## Data use, access, and governance
- Acknowledgement requirement: Explicit wording required on all copies, publications, and presentations.
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Access and sharing: Data should be uploaded to appropriate portals and catalogues; sharing limitations should be respected, with governance and versioning in place.
- Metadata and documentation: The dataset provides detailed column descriptions and references to standard classifications to support discovery and reuse.
- Copyright: Countryside Survey data © NERC - CEH; all rights reserved.

## Practical considerations for data stewards
- Data integration: When merging with other datasets, harmonize LC07_LC07_NUM and EZ_DESC_07 with compatible classifications and environmental zone schemas.
- Interoperability: Be mindful of legacy formats and codes; ensure consistent interpretation of THEMEs, attribute names, and range fields.
- Data quality and updates: Maintain provenance by tracking year-specific IDs; plan for updates or replacements if newer Countryside Survey releases occur.
- Documentation: Preserve and surface the references provided (Countryside Survey website and associated literature) to aid users in understanding methodologies and classifications.

## References and further reading
- Countryside Survey Website — general project overview and methodologies.
- Bunce, R.G.H., Barr, C.J., Clarke, R.T., Howard, D.C., Lane, A.M.J. (1996, 2007) on ITE Land Classification of Great Britain.
- Jackson, D.L. (2000) Guidance on Biodiversity Broad Habitat Classification and related materials.
- ITE Land Classification of Great Britain 2007 dataset (NERC Environmental Information Data Centre).
- Additional links and DOIs provided in the dataset documentation.