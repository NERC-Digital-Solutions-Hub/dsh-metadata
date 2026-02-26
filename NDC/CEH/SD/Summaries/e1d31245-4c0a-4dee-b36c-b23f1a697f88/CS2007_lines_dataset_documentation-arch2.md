# Landscape linear feature data 2007 [Countryside Survey], Great Britain

## Overview
- Landscape linear features data from 442 1km squares across Great Britain, sampled in 2007 as part of the Countryside Survey.
- Data owned by NERC - Centre for Ecology & Hydrology; copyright applies.
- Included as part of a standardized environmental monitoring effort to assess landscape features and their attributes over time.

## Dataset scope and content
- Two main data blocks within the CSV:
  - Landscape linear features: attributes describing each feature and its context
  - Species composition for each feature: species codes, names, and proportions within each feature
- Key attributes (selected): 
  - SQUARE (1km site code), YEAR, LINEAR_ID (per year), EVENT_ID (per year), EVENT_FROM and EVENT_TO (start/end positions in metres)
  - THEME and THEME_NAME; PRIMARY_ATTRIBUTE and PRIMARY_ATTRIBUTE_NAME
  - HEIGHT, HEIGHT_RANGE, BASE_HEIGHT, BASE_HEIGHT_RANGE
  - WIDTH and WIDTH_RANGE
  - MODAL_DBH and MODAL_DBH_RANGE (diameter at breast height)
  - CONDITION and CONDITION_DESCRIPTION
  - HISTORIC_MANAGEMENT, EVIDENCE_MANAGEMENT, EVIDENCE_MGT_DESCRIPTION
  - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS
  - VERTICAL_GAPPINESS and VERTICAL_GAPPINESS_RANGE
  - Margin widths (left/right) and ranges
  - SPECIES_COMPOSITION and SPECIES_COMP_DESCRIPTION
  - LC07 and LC07_NUM (ITE Land Classification 2007)
  - COUNTRY, COUNTY07, EZ_DESC_07 (Countryside Survey Environmental Zone)
- Species block includes: SPECIES, SPECIES_NAME, PROPORTION and PROPORTION_RANGE, plus the same geographic/classification fields as above.

## Data structure notes
- LINEAR_ID and EVENT_ID are unique within a year.
- SQUARE identifies the 1km sampling site; data are organized per landscape linear feature with start/end positions along the feature.
- EZ_DESC_07 provides environmental zone context; LC07 codes reflect land classification.

## Data usage and governance
- All use of Countryside Survey data must be acknowledged with the provided notice:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey ©; Database Right/Copyright applies.
- Data can be used for monitoring environmental health and policy performance over time, typically via standardised methods and outputs (reports, maps, charts).
- Practices emphasize data validation, quality assurance, cleaning, and transformation, with outputs stored and uploaded to appropriate portals.
- Encouraged to combine CS data with other relevant datasets to increase value and to enable broader data access.

## Access, rights, and references
- Acknowledgement and copyright must accompany all copies, publications, reports, and presentations.
- References and further information:
  - Countryside Survey Website (general overview and methodologies)
  - ITE Merlewood Land Classification references (LC07) and related publications
  - JNCC Biodiversity Broad Habitat guidance (related classifications)
  - DOIs/Links provided in the references section of the dataset

## Analytical context for monitoring
- Enables temporal and spatial analysis of landscape linear features and their ecological characteristics.
- Supports assessment of canopy structure, management history, species composition, and physical attributes along linear features.
- Useful for cross-square comparisons and longitudinal monitoring, with potential integration with other Countryside Survey data or external environmental datasets.
- To maximize utility, plan to link with additional datasets and ensure data accessibility through standard portals.