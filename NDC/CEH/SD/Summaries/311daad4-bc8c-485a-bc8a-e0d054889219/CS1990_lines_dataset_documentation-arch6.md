# Landscape linear feature data 1990 [Countryside Survey], Great Britain

## Overview
- Dataset capturing landscape linear features from 325 1km squares across Great Britain as surveyed in 1990 (Countryside Survey).
- Data stored in LANDSCAPE_LINEAR_FEATURES_1990.csv with two linked components: feature-level attributes and species-level composition.

## Dataset scope and structure
- Coverage: Great Britain (England, Scotland, Wales), 1990, based on 1km square sampling sites.
- Feature-level attributes (per linear feature event):
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey
  - LINEAR_ID: Landscape linear feature identifier (unique within a year)
  - EVENT_ID: Feature event identifier (unique within a year)
  - EVENT_FROM / EVENT_TO: Start and end positions along the feature (in metres)
  - THEME / THEME_NAME: Theme code and description
  - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME: Primary attribute code and description
  - HEIGHT / HEIGHT_RANGE: Height code and description
  - BASE_HEIGHT / BASE_HEIGHT_RANGE: Base height code and description
  - WIDTH / WIDTH_RANGE: Width code and description
  - MODAL_DBH / MODAL_DBH_RANGE: Modal diameter at breast height code and description
  - CONDITION / CONDITION_DESCRIPTION: Condition code and description
  - HISTORIC_MANAGEMENT / EVIDENCE_MANAGEMENT / EVIDENCE_MGT_DESCRIPTION: Signs of historic or current management
  - STAKED_TREES / TREE_PROTECTORS / LINE_STUMPS: Feature presence indicators
  - VERTICAL_GAPPINESS / VERTICAL_GAPPINESS_RANGE: Vertical gaps in woody linear features
  - MARGIN_WIDTH_LEFT / MARGIN_WIDTH_LEFT_RANGE: Left margin width code and description
  - MARGIN_WIDTH_RIGHT / MARGIN_WIDTH_RIGHT_RANGE: Right margin width code and description
  - SPECIES_COMPOSITION / SPECIES_COMP_DESCRIPTION: Species composition code and description for the woody feature
  - LC07 / LC07_NUM: ITE Land Classification 2007 terms
  - COUNTRY / COUNTY07 / EZ_DESC_07: Geographic and environmental zone descriptors
- Species-level attributes (per species within a feature event):
  - SQUARE / YEAR / EVENT_ID: Identifier context
  - SPECIES / SPECIES_NAME: Species code and name
  - PROPORTION / PROPORTION_RANGE: Proportion of species within the feature
  - LC07 / LC07_NUM: ITE Land Classification context
  - COUNTRY / COUNTY07 / EZ_DESC_07: Geographic and environmental descriptors
- All use of Countryside Survey (CS) data must be acknowledged; data are copyright to NERC CEH.

## Data use and potential outputs
- Create self-serve data products: dashboards, pivot tables, and charts to explore:
  - Spatial distribution of linear features by country, county, and environmental zone
  - Feature attributes (height, width, base height, condition) across regions
  - Species composition along linear features and across themes
  - Temporal crosswalks with land classification (ITE LC07) and related ecological descriptors
- Data integration opportunities:
  - Link feature events to LC07 classifications and EZ descriptions for ecological or policy analyses
  - Combine feature-level data with species-level data to analyze habitat structure and biodiversity context
- Outputs can support policy, planning, and communication by providing accessible summaries of woody linear features and their management signs.

## Data quality, assumptions, and caveats
- Feature and species data are tied to specific survey years (1990) and sampling sites (1km squares); cross-year analyses require careful alignment.
- Many attributes are coded with linked descriptive ranges (e.g., HEIGHT, WIDTH, PROPORTION) requiring reference to accompanying descriptions for interpretation.
- Relevant geographic and environmental context is provided via LC07, COUNTRY, COUNTY07, and EZ_DESC_07 fields to support contextual analyses.

## Acknowledgement and licensing
- All use of CS data must include the following acknowledgement:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## References and further reading
- Countryside Survey Website: General overview and methodologies
- Bunce, R.G.H. et al. (1996) ITE Merlewood Land Classification of Great Britain. Journal of Biogeography, 23, 625-634
- Bunce, R.G.H. et al. (1981) Land Classes in Great Britain: Preliminary Descriptions for Users of the Merlewood Method of Land Classification
- Jackson, D.L. (2000) Guidance on the interpretation of the Biodiversity Broad Habitat Classification (JNCC Report 307)
- Bunce, R.G.H. et al. (2007) ITE Land Classification of Great Britain 2007. NERC Environmental Information Data Centre
- Countryside Survey Publications and links: http://www.countrysidesurvey.org.uk/