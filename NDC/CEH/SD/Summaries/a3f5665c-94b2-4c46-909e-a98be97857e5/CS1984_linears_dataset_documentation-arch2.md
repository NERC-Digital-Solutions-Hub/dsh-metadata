# Landscape linear feature data 1984 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey, capturing landscape linear features sampled in 1984 across 230 1km squares in Great Britain.
- Delivered as a CSV with extensive attribute fields describing each linear feature and associated species data.
- Includes geographic (SQUARE, COUNTRY, COUNTY07), temporal (YEAR), and feature-specific information.

## Data Structure and Key Fields
- Core identifiers and geometry
  - SQUARE (1km square code)
  - YEAR (survey year)
  - EVENT_ID (feature event identifier within a year)
  - LINEAR_ID (feature identifier within a year)
  - EVENT_FROM / EVENT_TO (start and end positions along the feature in metres)
- Feature attributes
  - THEME / THEME_NAME
  - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME
  - HEIGHT / HEIGHT_RANGE
  - BASE_HEIGHT / BASE_HEIGHT_RANGE
  - WIDTH / WIDTH_RANGE
  - MODAL_DBH / MODAL_DBH_RANGE
  - CONDITION / CONDITION_DESCRIPTION
  - HISTORIC_MANAGEMENT / EVIDENCE_MANAGEMENT / EVIDENCE_MGT_DESCRIPTION
  - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS
  - VERTICAL_GAPPINESS / VERTICAL_GAPPINESS_RANGE
  - MARGIN_WIDTH_LEFT / MARGIN_WIDTH_LEFT_RANGE
  - MARGIN_WIDTH_RIGHT / MARGIN_WIDTH_RIGHT_RANGE
  - SPECIES_COMPOSITION / SPECIES_COMP_DESCRIPTION
  - LC07 / LC07_NUM (ITE Land Classification 2007)
  - COUNTRY / COUNTY07
  - EZ_DESC_07 (Environmental Zone description)
- Species data (per event)
  - SPECIES / SPECIES_NAME
  - PROPORTION / PROPORTION_RANGE
  - LC07 / LC07_NUM
  - COUNTRY / COUNTY07
  - EZ_DESC_07
- Notes
  - The dataset includes both feature-level attributes and species composition attributes, with the latter repeated for species entries associated with each feature event.

## Data Use and Standards
- Data are intended to be analyzed using standardised methods to categorise environmental health and landscape characteristics.
- Outputs are typically presented as reports, maps, and charts, with datasets stored/uploaded to appropriate data portals.
- Quality assurance workflow includes data verification, cleaning, and transformation prior to analysis.

## Access and Acknowledgement
- All use of Countryside Survey data must be acknowledged with:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology and Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology and Hydrology. All rights reserved.
- Data copyright and licensing are explicitly stated.

## Relevant Publications & References
- Countryside Survey Website (general project overview and methodologies)
- Bunce, R.G.H., et al. (1996) ITE Merlewood Land Classification of Great Britain
- Bunce, R.G.H., Barr, C.J., Whittaker, H.A. (1981) Land Classes in Great Britain: Preliminary Descriptions
- Jackson, D.L. (2000) Guidance on interpretation of the Biodiversity Broad Habitat Classification
- Bunce, R.G.H., et al. (2007) ITE Land Classification of Great Britain 2007
- Links and DOIs provided for further methodology and data access

## Practical Analytic Opportunities for Environment Monitoring
- Assess environmental condition consistency across the landscape using standardised feature attributes (height, width, condition, management indicators).
- Monitor changes over time by integrating 1984 data with subsequent Countryside Survey waves.
- Combine landscape feature data with species composition and land classification (LC07) to explore habitat structure and biodiversity associations.
- Enable data-sharing and reproducibility by storing datasets in designated portals and maintaining proper acknowledgements.

## Important Considerations
- Year-specific dataset (1984) with 230 sampled 1km squares; suitable for cross-year comparisons when integrated with other survey years.
- Many fields are coded with ranges and codes (e.g., HEIGHT_RANGE, PROPORTION_RANGE) requiring reference to codebooks for interpretation.
- Feature and species data are linked within events, with unique identifiers scoped to each year.