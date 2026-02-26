# Landscape linear feature data 2007 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey (2007) detailing landscape linear features across Great Britain.
- Based on 442 1km sampling squares.
- Data owned by NERC - Centre for Ecology & Hydrology; all rights reserved.
- File: Landscape_LINEAR_FEATURES_2007.csv.
- Contains two linked sets of columns: feature-level attributes (describing linear features) and species composition associated with each feature.

## Data content and structure
- Feature-level data (per landscape linear feature event located within a 1km square):
  - SQUARE, YEAR, LINEAR_ID (unique within year), EVENT_ID (unique within year)
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
  - COUNTRY (ENG, SCO, WAL), COUNTY07
  - EZ_DESC_07 (Countryside Survey Environmental Zone description)
- Species-level data (per feature event):
  - SPECIES (code), SPECIES_NAME, PROPORTION, PROPORTION_RANGE
  - LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07
- Notes: The dataset is structured to link species composition to the corresponding landscape linear feature event and its square location.

## Scope and coverage
- Geography: Great Britain (England, Scotland, Wales)
- Temporal coverage: Survey data from 2007
- Spatial resolution: 1km square sampling with linear features characterized within each square

## Usage, attribution, and access
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text to include: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and copyright notice.
- Data are © NERC - CEH; all rights reserved.
- References and methodology available via the Countryside Survey website and associated publications.

## Relevant references and sources
- Countryside Survey Website (general project overview and methodologies)
- Bunce et al. (1996, 1996, 2007) ITE Merlewood Land Classification of Great Britain
- Bunce et al. (1981) Land Classes in Great Britain: Preliminary Descriptions
- Jackson (2000) Guidance on Biodiversity Broad Habitat Classification
- ITE Land Classification of Great Britain 2007 (Datasets and DOIs provided in references)

## Potential analytical applications for analysts
- Correlate landscape linear feature attributes (height, width, margins, vertical gaps) with land classification (LC07) and environmental zones (EZ_DESC_07).
- Examine species composition along woody linear features and relate to management signals (historic and evidence of management).
- Assess spatial patterns of linear features across 1km squares and their ecological attributes (condition, DBH proxies, margins).
- Integrate with other Countryside Survey data to model how linear features relate to biodiversity or habitat quality across Great Britain.
- Use EVENT_FROM/EVENT_TO to study the geographic extent of features within squares and link to environmental variables.
- Explore relationships between feature geometry (width, margins) and structural indicators (MODAL_DBH, HEIGHT) for habitat assessment.

## Notes on data quality and limitations
- Data are limited to 2007 and to 442 1km squares, which may constrain longitudinal or national-scale trend analysis.
- Many attributes use coded ranges (e.g., HEIGHT, WIDTH, PROPORTION) that require reference to code descriptions for interpretation.
- Data integrity depends on accurate linkage between feature and species composition via EVENT_ID within each square/year.