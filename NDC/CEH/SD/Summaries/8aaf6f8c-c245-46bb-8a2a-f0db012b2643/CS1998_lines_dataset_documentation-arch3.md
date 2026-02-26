# Landscape linear feature data 1998 [Countryside Survey], Great Britain

## Overview
- Data from the Countryside Survey (Great Britain), 1998, covering landscape linear features sampled across 412 1km squares.
- Carrying organization: NERC - Centre for Ecology & Hydrology; metadata and field definitions provided.
- Version: 1: 04-02-2016; copyright and acknowledgement requirements apply to all uses.

## Data Content and Structure
- Two main data components within LANDSCAPE_LINEAR_FEATURES_1998.csv:
  - Landscape linear features per 1km square:
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
    - MARGIN_LEFT, MARGIN_LEFT_RANGE
    - MARGIN_RIGHT, MARGIN_RIGHT_RANGE
    - SPECIES_COMPOSITION, SPECIES_COMP_DESCRIPTION
    - LC07, LC07_NUM
    - COUNTRY, COUNTY07
    - EZ_DESC_07
  - Species composition per feature event:
    - SQUARE, EVENT_ID, YEAR
    - SPECIES, SPECIES_NAME
    - PROPORTION, PROPORTION_RANGE
    - LC07, LC07_NUM
    - COUNTRY, COUNTY07
    - EZ_DESC_07
- The data captures both the physical characteristics of woody linear features (e.g., hedgerows) and the species composition within those features.

## Key data fields and their implications for monitoring
- Geometry and extent:
  - EVENT_FROM and EVENT_TO enable calculation of feature length along the line.
- Physical structure and condition:
  - HEIGHT, BASE_HEIGHT, WIDTH with ranges for interpretation.
  - MODAL_DBH (dominant diameter at breast height) and BASE_HEIGHT ranges indicate canopy structure and size distribution.
  - CONDITION and CONDITION_DESCRIPTION signal current quality.
- Management signals:
  - HISTORIC_MANAGEMENT, EVIDENCE_MANAGEMENT, EVIDENCE_MGT_DESCRIPTION provide history of interventions and management evidence.
  - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS indicate protection or disturbance measures.
- Gaps and margins:
  - VERTICAL_GAPPINESS and MARGIN_WIDTH_LEFT/RIGHT capture structural connectivity and edge effects.
- Biodiversity context:
  - SPECIES_COMPOSITION and PROPORTION with SPECIES_NAME and LC07 classifications (ITE land classes) give species-level context and habitat classification.
- Geography and classification:
  - COUNTRY, COUNTY07, EZ_DESC_07 provide geographic and environmental zone context.
  - LC07 and LC07_NUM relate to land classification schemes for habitat context.

## Data Use for Monitoring and Policy Evaluation
- Supports evaluation of landscape connectivity and structural integrity of woody linear features (e.g., hedgerows) across Great Britain.
- Enables monitoring of feature condition, historical and evidence-based management actions, and their prevalence.
- Provides biodiversity context through species composition and DBH-related attributes to inform habitat quality assessments.
- Can underpin dashboards, reports, and policy reviews concerning habitat networks and landscape-scale ecological health.

## Data Access, Metadata and Governance
- Usage requires acknowledgement of Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; copyright applies to all copies and outputs.
- Data is provided in CSV with explicit field names and embedded range descriptors, aiding interpretation but potentially requiring transformation for integration with other datasets (e.g., units, codes to categories).

## References and Documentation
- Countryside Survey website and methodologies for broader context and linked documents.
- References to related classifications and habitat/biodiversity frameworks (ITE Land Classification of Great Britain, Biodiversity Broad Habitat Classification) for interpreting LC07 codes and habitat context.