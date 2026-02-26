# Landscape linear feature data 1990 [Countryside Survey], Great Britain

## Overview
- A Countryside Survey data item describing landscape linear features (woody linear features) observed in 1990 across 325 1km squares in Great Britain.
- Data source: Countryside Survey (© NERC - Centre for Ecology & Hydrology). All use must be acknowledged; data owned by NERC-CEH; copyright reserved.

## Data structure and content
- Two primary components:
  - Landscape linear features table (LANDSCAPE_LINEAR_FEATURES_1990.csv)
  - Species composition table (per feature) with species-level details
- Feature-level fields include:
  - SQUARE, YEAR, EVENT_ID (unique within year), LINEAR_ID (unique within year)
  - EVENT_FROM and EVENT_TO (start/end positions in metres along feature)
  - THEME and THEME_NAME; PRIMARY_ATTRIBUTE and PRIMARY_ATTRIBUTE_NAME
  - HEIGHT, HEIGHT_RANGE; BASE_HEIGHT and BASE_HEIGHT_RANGE
  - WIDTH and WIDTH_RANGE; MODAL_DBH and MODAL_DBH_RANGE
  - CONDITION and CONDITION_DESCRIPTION
  - HISTORIC_MANAGEMENT, EVIDENCE_MANAGEMENT, EVIDENCE_MGT_DESCRIPTION
  - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS
  - VERTICAL_GAPPINESS and VERTICAL_GAPPINESS_RANGE
  - MARGIN_WIDTH_LEFT and MARGIN_WIDTH_LEFT_RANGE
  - MARGIN_WIDTH_RIGHT and MARGIN_WIDTH_RIGHT_RANGE
  - SPECIES_COMPOSITION and SPECIES_COMP_DESCRIPTION
  - LC07 and LC07_NUM (ITE Land Classification 2007)
  - COUNTRY and COUNTY07; EZ_DESC_07 (Countryside Survey Environmental Zone description)
- Species composition fields include:
  - SQUARE, YEAR, EVENT_ID, SPECIES, SPECIES_NAME, PROPORTION, PROPORTION_RANGE
  - LC07 and LC07_NUM; COUNTRY, COUNTY07; EZ_DESC_07

## Key variables and coding
- The dataset uses codes with descriptive names (e.g., THEME, PRIMARY_ATTRIBUTE, HEIGHT, WIDTH, CONDITION, EVIDENCE_MANAGEMENT) and accompanying range/name fields for interpretation.
- Land classification and geographic context:
  - LC07/LC07_NUM describe ITE Land Classification (Great Britain, 2007)
  - COUNTRY and COUNTY07 locate squares within England, Scotland, or Wales
  - EZ_DESC_07 provides environmental zone descriptions
- Species data links species codes to names and proportion within each linear feature event.

## Spatial and temporal coverage
- Temporal: Survey year 1990
- Spatial: 325 sampled 1km squares across Great Britain (England, Scotland, Wales)

## Data usage, attribution, and governance
- Acknowledgement required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
- Licensing: Countryside Survey data © database rights/copyright; all rights reserved
- Data provenance supports integration with ITE Land Classification and related Countryside Survey methodologies
- Metadata and data management considerations:
  - Some fields rely on lookups (THEME_NAME, PROPORTION_RANGE, etc.)
  - Data may require transformation for modern formats; ensure metadata completeness and data provenance when reused

## Relevance for monitoring frameworks
- Provides detailed, feature-level data on woody linear features, useful for:
  - Assessing habitat structure and connectivity via linear features
  - Linking landscape features to land classification (ITE LC07) and environmental zones (EZ_DESC_07)
  - Analyzing stand attributes (height, diameter, condition, margins, management signals)
  - Incorporating species composition within linear features for biodiversity monitoring
- Supports longitudinal analysis when combined with other years of Countryside Survey data and related publications

## Practical considerations and limitations
- Temporal limitation: data from 1990; may need integration with other years for trend analysis
- Metadata gaps: requires careful handling of code-to-description lookups and crosswalks
- Data transformation: formats and field codes may require substantial preprocessing to standardize for dashboards or reports
- Governance: ensure appropriate data sharing and clear attribution when disseminating outputs

## References and lineage
- Countryside Survey Website (general overview and methodologies)
- Bunce et al. (1996) ITE Merlewood Land Classification of Great Britain; methodology and relevance
- Bunce et al. (1981, 2007) descriptions/updates of land classification
- Jackson (2000) guidance on Biodiversity Broad Habitat Classification and its relation to other classifications
- NERC Environmental Information Data Centre entries for ITE Land Classification of Great Britain 2007
- Related datasets and publications cited for context and crosswalks

## Supporting notes for practitioners
- Use the features and species tables together to quantify habitat structure and biodiversity contributions of landscape linear features
- Leverage LC07 and EZ_DESC_07 for environmental zoning and land classification analyses
- Maintain proper attribution and cite the Countryside Survey materials and referenced publications in all outputs
- Plan for data upgrading or linkage with subsequent Countryside Survey years to enable trend analyses and monitoring over time