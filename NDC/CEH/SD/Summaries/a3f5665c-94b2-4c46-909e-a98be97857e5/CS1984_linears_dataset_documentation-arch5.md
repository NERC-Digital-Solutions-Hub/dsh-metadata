# Landscape linear feature data 1984 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey, focusing on landscape linear features sampled across 230 1km squares in Great Britain in 1984.
- Data owned by NERC - Centre for Ecology & Hydrology; version 1: 04-02-2016.
- Acknowledgement and copyright: All CS data usage requires the provided acknowledgement text; copyright reserved.

## Data content and structure
- LANDSCAPE_LINEAR_FEATURES_1984.csv file details:
  - Feature-level attributes (first block):
    - SQUARE (1km sampling site code), YEAR, LINEAR_ID (unique within a year), EVENT_ID (unique within a year)
    - EVENT_FROM and EVENT_TO (start/end along linear, metres)
    - THEME and THEME_NAME
    - PRIMARY_ATTRIBUTE and PRIMARY_ATTRIBUTE_NAME
    - HEIGHT, HEIGHT_RANGE, BASE_HEIGHT, BASE_HEIGHT_RANGE
    - WIDTH, WIDTH_RANGE
    - MODAL_DBH and MODAL_DBH_RANGE
    - CONDITION and CONDITION_DESCRIPTION
    - HISTORIC_MANAGEMENT and EVIDENCE_MANAGEMENT; EVIDENCE_MGT_DESCRIPTION
    - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS
    - VERTICAL_GAPPINESS and VERTICAL_GAPPINESS_RANGE
    - MARGIN_WIDTH_LEFT and MARGIN_WIDTH_LEFT_RANGE
    - MARGIN_WIDTH_RIGHT and MARGIN_WIDTH_RIGHT_RANGE
    - SPECIES_COMPOSITION and SPECIES_COMP_DESCRIPTION
    - LC07 and LC07_NUM (ITE Land Classification 2007)
    - COUNTRY (ENG/SCO/WAL), COUNTY07, EZ_DESC_07 (Environmental Zone)
  - Species composition block (per-event/species data):
    - SQUARE, EVENT_ID, YEAR
    - SPECIES (code), SPECIES_NAME
    - PROPORTION and PROPORTION_RANGE
    - LC07 and LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07
- Each LINEAR_ID is unique within a year; each EVENT_ID is unique within a year.
- The dataset aligns with ITE Land Classification references and includes environmental zone descriptors and country/administrative metadata.

## Metadata, provenance, and documentation
- Includes references to methodology and classifications:
  - ITE Merlewood/Land Classification of Great Britain (1996, 1981)
  - ITE Land Classification of Great Britain 2007 (LC07)
  - Biodiversity Broad Habitat classifications guidance
- Country/area metadata: COUNTRY (ENG/SCO/WAL), COUNTY07, EZ_DESC_07
- Public references and links provided for methodology and classification context (Countryside Survey website and linked publications).

## Use, attribution, and licensing
- Data must be acknowledged in all copies, publications, and presentations:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology
- Acknowledgement and copyright notices apply to all uses of the data.

## Access, sharing, and dissemination
- The dataset supports uploading to relevant portals and catalogues; dataset holders are expected to catalogue and share in appropriate data repositories.
- Documentation includes extensive references to external sources and methodologies to support discoverability and reuse.

## Data quality, governance, and stewardship considerations
- Data quality and interoperability:
  - Complex attribute set with multiple codes and ranges (e.g., HEIGHT, BASE_HEIGHT, WIDTH, MODAL_DBH, etc.) requiring controlled vocabularies and consistent interpretation.
  - Large, feature-based data spanning multiple derived attributes; ensure alignment across systems when sharing.
- Governance and standards:
  - Two-part structure: feature attributes and species composition per event; requires careful integration and schema consistency.
  - Use of multiple classification schemes (THEME, PRIMARY_ATTRIBUTE, LC07) and environment zone descriptors; maintain consistent vocabularies.
- Operational challenges for data stewards:
  - Timely access from data creators and adherence to metadata standards.
  - Harmonizing data across different systems/formats if merging with other datasets.
  - Handling potentially outdated data (1984) while preserving provenance and traceability.
  - Ensuring updates and embargo or sharing limitations are respected in downstream portals.

## References and publications
- Countryside Survey Website and related methodology documents
- Bunce et al. (1996, 2007) ITE Land Classification of Great Britain
- Jackson (2000) guidance on Biodiversity Broad Habitat Classification
- Directorate references and DOIs/links as listed in the dataset documentation