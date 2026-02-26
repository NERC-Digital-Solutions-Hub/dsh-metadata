# Landscape linear feature data 2007 [Countryside Survey], Great Britain

## Overview
- A dataset of landscape linear features from 442 1km squares across Great Britain, sampled in 2007 as part of the Countryside Survey.
- Data owned by NERC - Centre for Ecology & Hydrology (CEH); Countryside Survey ©.
- Document version: 1; date: 04-02-2016.

## Data Content
- Landscape linear features (WLF) dataset with extensive attribute fields:
  - SQUARE, YEAR, LINEAR_ID (unique within a year), EVENT_ID (unique within a year), EVENT_FROM (start in metres), EVENT_TO (end in metres).
  - THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME.
  - HEIGHT, HEIGHT_RANGE, BASE_HEIGHT, BASE_HEIGHT_RANGE.
  - WIDTH, WIDTH_RANGE.
  - MODAL_DBH, MODAL_DBH_RANGE.
  - CONDITION, CONDITION_DESCRIPTION.
  - HISTORIC_MANAGEMENT, EVIDENCE_MANAGEMENT, EVIDENCE_MGT_DESCRIPTION.
  - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS.
  - VERTICAL_GAPPINESS, VERTICAL_GAPPINESS_RANGE.
  - MARGIN_WIDTH_LEFT, MARGIN_WIDTH_LEFT_RANGE, MARGIN_WIDTH_RIGHT, MARGIN_WIDTH_RIGHT_RANGE.
  - SPECIES_COMPOSITION, SPECIES_COMP_DESCRIPTION.
  - LC07, LC07_NUM (ITE Land Classification 2007).
  - COUNTRY (ENG/SCO/WAL), COUNTY07, EZ_DESC_07 (Countryside Survey Environmental Zone description).
- Species composition data linked to WLF events:
  - SQUARE, YEAR, EVENT_ID.
  - SPECIES, SPECIES_NAME, PROPORTION, PROPORTION_RANGE.
  - LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07.
- All data include clear coded values with descriptive ranges and taxonomy where applicable.

## Data Source, Versioning and Classification
- Source: Countryside Survey data; data collection year 2007.
- Includes alignment with ITE Land Classification of Great Britain (LC07) and environmental zoning (EZ_DESC_07).
- Country and regional identifiers: COUNTRY, COUNTY07.

## Usage, Access and Acknowledgement
- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement text:
  - Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Acknowledgement and copyright notice must be used on all copies, publications, reports, and presentations.

## Data Governance and Quality Considerations
- Rich metadata and coded attribute schemes support standardized monitoring and comparison.
- Potential challenges for monitoring teams:
  - Complex transformation and interpretation of numerous coded fields (themes, attributes, heights, widths, DBH, etc.).
  - Metadata completeness and consistency across datasets to ensure verifiability.
  - Data sharing constraints due to copyright and licensing.
- Data provenance is explicit (Countryside Survey 2007), aiding traceability and quality assurance.

## Relevance for Monitoring Frameworks
- Provides structural habitat information (linear features) and associated species composition data, useful for assessing landscape connectivity, woody feature management, and habitat quality.
- The dataset leverages established classifications (ITE LC07) and environmental zoning (EZ_DESC_07), facilitating comparability with other datasets and over time.
- Supports governance-focused monitoring through explicit data ownership, usage restrictions, and required attribution.
- Enables generation of reports, charts, or dashboards to inform policy decisions and future monitoring planning.

## References and Related Publications
- Countryside Survey Website: general overview and methodologies.
- Bunce et al. (1996, 2007): ITE Merlewood/Land Classification of Great Britain and related descriptions.
- Jackson (2000): Guidance on Biodiversity Broad Habitat Classification interpretations.
- Countryside Survey (2007) dataset references and DOI links:
  - ITE Land Classification of Great Britain 2007 dataset (doi:10.5285/5f0605e4-aa2a-48ab-b47c-bf5510823e8f).
- Additional resources and links provided in the dataset documentation.