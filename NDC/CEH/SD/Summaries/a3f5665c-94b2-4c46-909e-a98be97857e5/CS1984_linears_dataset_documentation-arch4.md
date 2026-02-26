# Landscape linear features 1984 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey, Great Britain, capturing landscape linear features surveyed in 1984.
- File: LANDSCAPE_LINEAR_FEATURES_1984.csv.
- Coverage: 230 1km squares across Great Britain; data owned by NERC - Centre for Ecology & Hydrology.
- Includes both feature-level attributes and species composition data associated with features.

## Data Content
- Landscape linear features data (feature-level) across sampled 1km squares.
- Two main blocks of columns:
  - Feature attributes:
    - SQUARE, YEAR, LINEAR_ID (unique within a year), EVENT_ID (unique within a year)
    - EVENT_FROM, EVENT_TO (start/end along the linear feature in metres)
    - THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME
    - HEIGHT, HEIGHT_RANGE, BASE_HEIGHT, BASE_HEIGHT_RANGE
    - WIDTH, WIDTH_RANGE
    - MODAL_DBH, MODAL_DBH_RANGE
    - CONDITION, CONDITION_DESCRIPTION
    - HISTORIC_MANAGEMENT, EVIDENCE_MANAGEMENT, EVIDENCE_MGT_DESCRIPTION
    - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS
    - VERTICAL_GAPPINESS, VERTICAL_GAPPINESS_RANGE
    - MARGIN_WIDTH_LEFT, MARGIN_WIDTH_LEFT_RANGE
    - MARGIN_WIDTH_RIGHT, MARGIN_WIDTH_RIGHT_RANGE
    - SPECIES_COMPOSITION, SPECIES_COMP_DESCRIPTION
    - LC07, LC07_NUM (ITE Land Classification 2007)
    - COUNTRY, COUNTY07, EZ_DESC_07
  - Species composition data (per feature per year):
    - SQUARE, EVENT_ID, YEAR
    - SPECIES (code), SPECIES_NAME, PROPORTION, PROPORTION_RANGE
    - LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07

## Key Attributes and What They Capture
- Spatial-temporal identifiers: SQUARE, YEAR, LINEAR_ID, EVENT_ID, plus EVENT_FROM and EVENT_TO for feature length.
- Structural/physical attributes: HEIGHT, HEIGHT_RANGE, BASE_HEIGHT, BASE_HEIGHT_RANGE, WIDTH, WIDTH_RANGE.
- Biological and management signals: MODAL_DBH and RANGE; CONDITION and its description; HISTORIC_MANAGEMENT; EVIDENCE_MANAGEMENT and its description; STAKED_TREES; TREE_PROTECTORS; LINE_STUMPS; VERTICAL_GAPPINESS and RANGE.
- Spatial context and classification: LC07 and LC07_NUM (ITE Land Classification 2007); COUNTRY, COUNTY07; EZ_DESC_07 (Countryside Survey Environmental Zone).
- Species-level context: SPECIES, SPECIES_NAME, PROPORTION, PROPORTION_RANGE; linked with same geographic and land classification fields.

## Data Use and Stewardship
- Designed to support analysis of Woody Linear Features and related landscape structure, management history, and ecological context.
- Metadata-rich, enabling integration with land classification and environmental zone frameworks.
- Useful for understanding feature specifications, spatial distribution, and species composition within landscapes.

## Data Quality, Access, and Licensing
- Acknowledgement and copyright: All CS data must be acknowledged.
- Required notice when using the data in copies, publications, or presentations:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- References and methodological background provided to support interpretation and reuse.

## Licensing and References
- Key references and resources for context and methodology:
  - Countryside Survey website and project overview
  - ITE Merlewood Land Classification and related literature (Bunce et al. 1996; 1981)
  - Jackson, D.L. guidance on biodiversity broad habitats (2000)
  - ITE Land Classification of Great Britain 2007 (Bunce et al. 2007)
- Links and DOIs provided for dataset provenance and related classifications.

## Practical Considerations for Data Leaders
- Data governance: Clear attribution and licensing requirements to ensure compliant reuse.
- Data discovery and integration: Rich attribute set (physical, management, and ecological) facilitates cross-dataset analyses but requires consistent metadata alignment (LC07, EZ_DESC_07, etc.).
- Data availability and gaps: Year-specific snapshot (1984) across 230 squares; plan for temporal analyses or supplementary datasets if trend analysis is needed.
- User needs and workflows: Metadata supports translation of data into landscape-scale insights for policy, planning, or ecological research.
- Potential applications: Landscape structure assessment, historic land management impact studies, habitat connectivity analyses, incorporation into broader GB land classification frameworks.