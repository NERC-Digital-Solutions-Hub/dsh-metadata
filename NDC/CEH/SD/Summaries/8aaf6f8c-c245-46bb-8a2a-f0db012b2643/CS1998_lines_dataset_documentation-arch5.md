# Landscape linear feature data 1998 [Countryside Survey], Great Britain

## Overview
- Landscape linear features dataset from 412 1km squares across Great Britain, sampled in 1998.
- Version: 1: 04-2-2016.
- Countryside Survey data © NERC - Centre for Ecology & Hydrology.
- Data are organized to support understanding and management of woody linear features, with clear coding for themes, attributes, and species composition.

## Dataset structure and key fields
- Two main components:
  - Landscape linear features (feature records)
    - SQUARE: 1km square sampling site code
    - YEAR: Year of survey
    - LINEAR_ID: Feature identifier (unique within a year)
    - EVENT_ID: Feature event identifier (unique within a year)
    - EVENT_FROM / EVENT_TO: Start and end positions along the feature (metres)
    - THEME / THEME_NAME: Theme code and description
    - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME: Primary attribute code and description
    - HEIGHT / HEIGHT_RANGE: Height code and descriptive range
    - BASE_HEIGHT / BASE_HEIGHT_RANGE: Base height code and range
    - WIDTH / WIDTH_RANGE: Width code and range
    - MODAL_DBH / MODAL_DBH_RANGE: Modal diameter at breast height code and range
    - CONDITION / CONDITION_DESCRIPTION: Condition code and description
    - HISTORIC_MANAGEMENT / EVIDENCE_MANAGEMENT / EVIDENCE_MGT_DESCRIPTION: Signs of historic and ongoing management
    - STAKED_TREES, TREE_PROTECTORS, LINE_STUMPS: Presence/absence indicators
    - VERTICAL_GAPPINESS / VERTICAL_GAPPINESS_RANGE: Vertical gaps in woody linear feature
    - MARGIN_WIDTH_LEFT / MARGIN_WIDTH_LEFT_RANGE: Left margin width code and range
    - MARGIN_WIDTH_RIGHT / MARGIN_WIDTH_RIGHT_RANGE: Right margin width code and range
    - SPECIES_COMPOSITION / SPECIES_COMP_DESCRIPTION: Species composition code and description
    - LC07 / LC07_NUM: ITE Land Classification 2007 code and number
    - COUNTRY / COUNTY07: Country and county/ council area
    - EZ_DESC_07: Countryside Survey Environmental Zone description
  - Species composition (per feature)
    - SQUARE / EVENT_ID / YEAR: Link back to feature
    - SPECIES / SPECIES_NAME: Species code and name
    - PROPORTION / PROPORTION_RANGE: Proportion of species and descriptive range
    - LC07 / LC07_NUM: ITE Land Classification (2007)
    - COUNTRY / COUNTY07: Country and county
    - EZ_DESC_07: Environmental Zone description
- All data are designed to be machine-readable with explicit codes and human-readable descriptions to aid interpretation and reuse.

## Metadata, provenance, and classifications
- Data are sourced from Countryside Survey and are tied to the ITE Land Classification framework (1996/2007 updates referenced in the dataset).
- Columns include coding schemes and descriptive ranges to facilitate interpretation and interoperability.
- The dataset references multiple publications and methodologies, with links and citations provided for context (e.g., ITE Land Classification, Biodiversity Broad Habitat classification guidance).

## Rights, acknowledgement, and citations
- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement text:
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- Suggested references and publications are listed (Countryside Survey website and Bunce et al. 1996/2007; Jackson 2000 guidance; related Land Classification documents).

## Governance and stewardship considerations
- Versioning and provenance are explicit (Version 1: 04-2-2016); ensure clear record of updates and new versions.
- Data stewards should maintain consistent metadata definitions, including code mappings (THEME, ATTRIBUTE, HEIGHT, WIDTH, DBH, CONDITION, etc.) and their ranges to support reproducibility.
- Ensure proper data sharing workflows, including timely updates from data creators and adherence to sharing limitations or embargoes if applicable.
- Documentation should cover data collection methods, quality assurance steps, and any transformations applied before sharing.
- Consideration of user needs and interoperability across systems is important, given potential challenges with diverse formats and large datasets.
- Encourage or provide guidance on proper attribution in all outputs (datasets, publications, presentations) to maintain data lineage.

## Notable references and related resources
- Countryside Survey website: general overview and methodologies.
- ITE Merlewood Land Classification documentation (Bunce et al., 1996; 1981 papers).
- ITE Land Classification of Great Britain 2007 (Bunce et al., 2007) and associated datasets.
- Guidance on Biodiversity Broad Habitat Classification (Jackson, 2000) and related JNCC materials.