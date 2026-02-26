# Landscape linear feature data 1998 [Countryside Survey], Great Britain Version: 1: 04-2-2016

## Overview
- A Countryside Survey dataset describing landscape linear features sampled across 412 1km squares in Great Britain in 1998.
- Includes two main data components within LANDSCAPE_LINEAR_FEATURES_1998.csv:
  - Feature-level attributes for each landscape linear feature (e.g., location, geometry, physical attributes, management signals, and environmental context).
  - Species composition associated with woody linear features (proportions by species within features).
- Data are provided as unique identifiers per year (LINEAR_ID and EVENT_ID) and are linked to the 1km square SQUARE and survey YEAR (1998).

## Data content and structure
- Feature attributes (primary fields):
  - SQUARE, YEAR, LINEAR_ID, EVENT_ID
  - EVENT_FROM, EVENT_TO (start/end along the feature in metres)
  - THEME, THEME_NAME
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME
  - HEIGHT, HEIGHT_RANGE
  - BASE_HEIGHT, BASE_HEIGHT_RANGE
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
  - COUNTRY (England/Scotland/Wales), COUNTY07
  - EZ_DESC_07 (Environmental Zone description)
- Species composition (second table-like set of columns within the same dataset):
  - SQUARE, EVENT_ID, YEAR
  - SPECIES (code), SPECIES_NAME
  - PROPORTION, PROPORTION_RANGE
  - LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07
- Notes on identifiers and year:
  - LINEAR_ID and EVENT_ID are unique within a given year.
  - YEAR records the survey year (1998).
- Additional context:
  - Includes cross-references to land classification and environmental zone descriptions (LC07, EZ_DESC_07) to support ecosystem context analyses.
  - All data are accompanied by a copyright notice and required acknowledgement.

## Data provenance and rights
- Acknowledgement required on all copies, publications, presentations:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## Potential uses for data
- Exploratory analysis and visualization of landscape linear features across Great Britain, 1998.
- Investigations of feature geometry and physical attributes (height, width, DBH) and their variation by region (COUNTRY, COUNTY07) and land classification (LC07).
- Analyses of management signals and historic/evidence of management associated with linear features.
- Examination of species composition within woody linear features and its relation to feature attributes and environmental context.
- Creation of dashboards, pivot tables, maps, and self-serve reports for non-technical end users.
- Data can be cross-referenced with LC07 (ITE land classification) and EZ_DESC_07 (environmental zones) for habitat and biodiversity assessments.

## Data quality, accessibility, and cautions
- Data pertain to a single year (1998) and are linked to 412 sampled 1km squares.
- The dataset uses coded fields (THEME, HEIGHT, CONDITION, etc.) that require documentation or reference to accompanying metadata for correct interpretation.
- Cross-references to ITE Land Classification (LC07) and environmental zones (EZ_DESC_07) are provided for ecological context.
- Proper data use requires the stated acknowledgement and adherence to licensing/copyright restrictions.

## References and publications
- Countryside Survey website and methodological documentation for the Countryside Survey project.
- ITE Land Classification references:
  - Bunce et al. (1996, 2007) Merlewood/Land Classification of Great Britain documents.
  - Jackson (2000) guidance on Biodiversity Broad Habitat Classification interpretations.
- Additional links and DOIs provided in the dataset documentation for in-depth methodology and data provenance.