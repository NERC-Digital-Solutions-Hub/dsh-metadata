# Landscape linear feature data 1990 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey (1990) covering landscape linear features across Great Britain.
- Based on 325 1km squares sampled in 1990.
- Provided as LANDSCAPE_LINEAR_FEATURES_1990.csv with two data blocks: feature attributes and species composition per event.
- Includes acknowledgment and licensing requirements: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; all rights reserved.

## Data Structure

### Feature-level attributes (landscape linear features)
- SQUARE: 1km square sampling site code
- YEAR: Year of survey (1990)
- LINEAR_ID: Feature identifier (unique within a year)
- EVENT_ID: Feature event identifier (unique within a year)
- EVENT_FROM, EVENT_TO: Start and end positions along the feature (metres)
- THEME, THEME_NAME: Theme code and description
- PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME: Primary attribute code and description
- HEIGHT, HEIGHT_RANGE: Height code and description
- BASE_HEIGHT, BASE_HEIGHT_RANGE: Base height code and description
- WIDTH, WIDTH_RANGE: Width code and description
- MODAL_DBH, MODAL_DBH_RANGE: Modal diameter at breast height (DBH) code and description
- CONDITION, CONDITION_DESCRIPTION: Condition code and description
- HISTORIC_MANAGEMENT, EVIDENCE_MANAGEMENT, EVIDENCE_MGT_DESCRIPTION: Historic/evidence of management indicators
- STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS: Presence/absence indicators
- VERTICAL_GAPPINESS, VERTICAL_GAPPINESS_RANGE: Vertical gaps in Woody Linear Feature (WLF)
- MARGIN_WIDTH_LEFT, MARGIN_WIDTH_LEFT_RANGE: Left margin width code and description
- MARGIN_WIDTH_RIGHT, MARGIN_WIDTH_RIGHT_RANGE: Right margin width code and description
- SPECIES_COMPOSITION, SPECIES_COMP_DESCRIPTION: Species composition code and description
- LC07, LC07_NUM: ITE Land Classification of Great Britain 2007 codes
- COUNTRY, COUNTY07: Country and administrative area
- EZ_DESC_07: Countryside Survey Environmental Zone description

### Species-level attributes (per event)
- SPECIES: Species code
- SPECIES_NAME: Species name
- PROPORTION, PROPORTION_RANGE: Proportion code and description
- LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07: Land classification and regional context consistent with feature-level data

## Spatial and Temporal Scope
- Temporal: Survey year 1990
- Spatial: 325 1km squares across Great Britain, country-level fields include England (ENG), Scotland (SCO), Wales (WAL); LC07 and EZ descriptors provide regional classification

## How to Use in GIS
- Map-based analysis of landscape linear features within 1km grid cells; link to LC07 land classifications and environmental zones.
- Attribute-rich layer: use THEME, PRIMARY_ATTRIBUTE, HEIGHT/BASE_HEIGHT/WIDTH, DBH, CONDITION, and management indicators for visualization and querying.
- Species composition per event enables per-feature biodiversity context (SPECIES_NAME and PROPORTION).
- Geometry notes: The dataset provides start and end positions along the linear feature (EVENT_FROM to EVENT_TO) within each square, but explicit geographic coordinates are not listed here. To map these features, you may need to integrate with a base linear network or square-level geometries to reconstruct feature geometries.
- Suitable for creating map products that show spatial distribution, feature morphology (height, width, DBH), condition, management indicators, and species composition across the GB 1990 landscape.
- Can be combined with other Countryside Survey layers (e.g., LC07 land classes, environmental zones) to enrich GIS analyses and visualizations.

## Data Quality, Standards, and Cautions
- Data are historical (1990) and may use coded values (with accompanying description fields) that require interpretation.
- IDs (LINEAR_ID, EVENT_ID) are unique within a given year; cross-year comparisons should account for this.
- Data are structured with multiple coded fields (e.g., THEME, HEIGHT, MARGIN_WIDTH); consult accompanying descriptions to ensure correct GIS symbolization and classification.
- Data quality and consistency challenges noted in GIS practice apply (e.g., data scattered across sources, need for cleaning/transformation, standardization of codes).

## Acknowledgement and Licensing
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
- Copyright: Countryside Survey © NERC Centre for Ecology & Hydrology. All rights reserved.

## References and Documentation
- Countryside Survey Website: general overview and methodologies
- Bunce et al. ITE Merlewood Land Classification of Great Britain (1996)
- Bunce et al. ITE Land Classification of Great Britain 2007
- Jackson, D.L. Guidance on Biodiversity Broad Habitat Classification (2000)
- NERC Environmental Information Data Centre entries for LC07 and related datasets