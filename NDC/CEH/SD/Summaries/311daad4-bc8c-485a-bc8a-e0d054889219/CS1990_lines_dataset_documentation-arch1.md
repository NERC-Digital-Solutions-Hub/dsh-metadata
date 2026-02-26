# Landscape linear feature data 1990 [Countryside Survey], Great Britain

- Version: 1: 04-2-2016. Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology

- Scope and coverage
  - Landscape linear features from 325 1km squares across Great Britain, sampled in 1990

- Data structure
  - Feature-level dataset (Landscape linear features)
    - SQUARE: 1km square sampling site code
    - YEAR: year of survey (1990)
    - LINEAR_ID: feature identifier (unique within year)
    - EVENT_ID: feature event identifier (unique within year)
    - EVENT_FROM / EVENT_TO: start and end positions along the feature (metres)
    - THEME / THEME_NAME: thematic classification
    - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME: primary attribute and description
    - HEIGHT / HEIGHT_RANGE: height code and description
    - BASE_HEIGHT / BASE_HEIGHT_RANGE: base height code and description
    - WIDTH / WIDTH_RANGE: width code and description
    - MODAL_DBH / MODAL_DBH_RANGE: modal diameter at breast height code and description
    - CONDITION / CONDITION_DESCRIPTION: condition code and description
    - HISTORIC_MANAGEMENT / EVIDENCE_MANAGEMENT / EVIDENCE_MGT_DESCRIPTION: signs of historic and current management
    - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS: presence/absence indicators
    - VERTICAL_GAPPINESS / VERTICAL_GAPPINESS_RANGE: vertical gaps in woody linear features
    - MARGIN_WIDTH_LEFT / MARGIN_WIDTH_LEFT_RANGE: left margin width
    - MARGIN_WIDTH_RIGHT / MARGIN_WIDTH_RIGHT_RANGE: right margin width
    - SPECIES_COMPOSITION / SPECIES_COMP_DESCRIPTION: species composition details
    - LC07 / LC07_NUM: ITE Land Classification of Great Britain 2007 (codes/descriptions)
    - COUNTRY: country (ENG, SCO, WAL)
    - COUNTY07: county or council
    - EZ_DESC_07: Countryside Survey Environmental Zone description

  - Species-level composition per event
    - SQUARE, YEAR, EVENT_ID
    - SPECIES / SPECIES_NAME: species code and name
    - PROPORTION / PROPORTION_RANGE: proportion code and description
    - LC07 / LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07: cross-referenced classifications

- Data usage and licensing
  - All Countryside Survey data must be acknowledged
  - Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey ©; data rights reserved

- Context, references, and provenance
  - Countryside Survey website and methodological documents
  - ITE Land Classification (Bunce et al. 1996; 2007) and related guidance
  - JNCC biodiversity classification guidance
  - Data centre records and DOIs linked in the references

- Relevance for analysts
  - Allows investigation of relationships between landscape linear features and environmental classifications, management signals, and species composition
  - Enables analyses of feature dimensions (height, width, margins), condition, and historic/evident management in relation to land class and environmental zones
  - Potential challenges to consider
    - Year-specific snapshot (1990) limits temporal inference
    - 1km-square scale may affect local-level conclusions
    - Coding schemes (heights, widths, proportions) require careful mapping to descriptions
    - Data integration requires attention to crosswalks for LC07 and EZ descriptors