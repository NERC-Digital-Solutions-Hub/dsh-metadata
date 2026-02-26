# Landscape linear feature data 1998 [Countryside Survey], Great Britain

## Overview
- Dataset describing landscape linear features from 412 1km squares across Great Britain, sampled in 1998.
- Source: Countryside Survey, data owned by NERC - Centre for Ecology & Hydrology (CEH).
- Includes a primary feature table and a secondary species composition table, with extensive attribute coding and descriptors.
- All use must be acknowledged, with copyright and acknowledgement requirements specified.

## Data content and structure
- LANDSCAPE_LINEAR_FEATURES_1998.csv comprises two main blocks:
  - Feature-level attributes (one record per landscape linear feature event):
    - Key identifiers: SQUARE (1km square code), YEAR, LINEAR_ID (within-year feature id), EVENT_ID (within-year event id), EVENT_FROM (start in metres), EVENT_TO (end in metres).
    - Descriptive fields: THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME.
    - Physical characteristics: HEIGHT, HEIGHT_RANGE, BASE_HEIGHT, BASE_HEIGHT_RANGE, WIDTH, WIDTH_RANGE, MODAL_DBH, MODAL_DBH_RANGE.
    - Condition and management: CONDITION, CONDITION_DESCRIPTION, HISTORIC_MANAGEMENT, EVIDENCE_MANAGEMENT, EVIDENCE_MGT_DESCRIPTION, STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS, VERTICAL_GAPPINESS, VERTICAL_GAPPINESS_RANGE.
    - Margins and composition: MARGIN_WIDTH_LEFT, MARGIN_WIDTH_LEFT_RANGE, MARGIN_WIDTH_RIGHT, MARGIN_WIDTH_RIGHT_RANGE, SPECIES_COMPOSITION, SPECIES_COMP_DESCRIPTION.
    - Classification and location: LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07.
  - Species composition for each landscape linear feature event:
    - KEY: SPECIES (code), SPECIES_NAME, PROPORTION, PROPORTION_RANGE, LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07.
- The data uses coded fields with corresponding descriptive ranges (e.g., HEIGHT_RANGE, WIDTH_RANGE) and references to external classifications (ITE/Land Class 2007) and country/county identifiers.

## Data provenance, use, and rights
- Data originates from the Countryside Survey project; © NERC - Centre for Ecology & Hydrology.
- Acknowledgement requirements:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- References and methodologies linked to a set of publications and the Countryside Survey website. Citations provide context for interpretation and usage.

## How Data Leaders can use this dataset
- Assess landscape structural features and their ecological attributes across Great Britain for policy or program evaluation.
- Integrate with other data sources to understand spatial patterns, feature conditions, and species composition at 1km-square resolution.
- Support data product development with clear metadata: track feature themes, attributes, margins, and canopy measures; ensure discoverability via codes and ranges.
- Facilitate co-ownership and feedback loops by aligning feature-level data with user needs (policy colleagues, researchers, partners) and iterating data products accordingly.
- Use the species composition block to analyze biodiversity components associated with woody linear features, in conjunction with Land Classification (ITE/LG07) and environmental zone descriptors.

## Data quality, standards, and governance considerations
- Extensive use of coded fields and range descriptors requires clear interpretation guidelines and maintained lookup tables.
- Metadata describes data structure but additional quality indicators (e.g., data completeness, temporal relevance) are not explicitly stated.
- Requires consistent acknowledgment in all copies, publications, and presentations.
- Potential challenges for Data Leaders: ensuring up-to-date data use rights, reconciling older 1998 data with newer datasets, and coordinating with wider data communities to avoid duplication.

## References and publications
- Countryside Survey Website and project documentation for methodology and broader context.
- Key references on land classification and biodiversity classifications, including:
  - Bunce et al. (1996, 2007) on ITE Land Classification of Great Britain (Merlewood/Land Classification, 2007 dataset)
  - Jackson (2000) guidance on Biodiversity Broad Habitat Classification definitions and relationships
- Data Centre entries and DOIs linked via the Countryside Survey outputs.