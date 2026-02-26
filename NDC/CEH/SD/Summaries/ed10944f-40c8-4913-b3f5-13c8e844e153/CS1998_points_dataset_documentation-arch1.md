# Landscape point feature data 1998 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey (Great Britain) covering landscape point features sampled in 1998/99.
- Spatial scope: 538 one-kilometre squares across Great Britain.
- File: LANDSCAPE_PT_FEATURES_1998.csv (version 1: 04-2-2016).
- Source and rights: Countryside Survey data © NERC - Centre for Ecology & Hydrology. All rights reserved; acknowledgement required on all copies and publications.

## Dataset structure and contents
- Core identifiers and scope
  - SQUARE: 1km square sampling site code
  - YEAR: survey year
  - ID: landscape point identifier (unique within a year)
- Thematic and attribute data
  - THEME, THEME_NAME: feature theme code and description
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME: primary attribute code and label
  - SPECIES, SPECIES_NAME: species code and name
  - PROPORTION, PROPORTION_RANGE: species cover/value
  - USE, USE_NAME: land-use/structures theme use code and label
  - BUFFER: buffer around veteran tree or pond
- Veteran tree and structural indicators
  - TREE_DEAD, MISSING_LIMBS, DEAD_WOOD, DEAD_MISSING_BARK, LIGHTNING_STRIKES, HOLLOW_TRUNK
  - VETERAN_TREE_TYPE, VETERAN_TREE_TYPE_NAME
  - MODAL_DBH, MODAL_DBH_RANGE
- Biodiversity and cover indicators
  - EPIPHYTE_COVER, EPIPHYTE_COVER_NAME
  - IVY_COVER, IVY_COVER_RANGE
  - CANOPY_LIVE, CANOPY_LIVE_RANGE
- Classification and geography
  - LC07, LC07_NUM: ITE Land Classification (GB 2007)
  - COUNTRY (England, Scotland, Wales), COUNTY07
  - EZ_DESC_07: Countryside Survey environmental zone description
- Notes on data usage
  - All use of CS data must be acknowledged with the provided citation text

## How this data can be used (analytical value)
- Correlation and pattern discovery
  - Relate landscape features (theme attributes, vegetation cover, veteran tree status) to land use and geography
  - Explore relationships between canopy live cover, epiphyte/ivy cover, and land classifications
- Modeling and predictions
  - Develop models predicting landscape feature presence or cover by square, year, or region
  - Integrate with ITE Land Classification (GB 2007) for cross-walk analyses
- Baseline and historical comparisons
  - Establish baseline landscape feature distributions for 1998/99 to compare with later surveys or other time points
- Spatial aggregation and reporting
  - Aggregate by SQUARE, COUNTY07, COUNTRY to inform regional biodiversity or habitat assessments
- Data integration-ready
  - Designed to be combined with other CS datasets and environmental classifications; supports multi-source analyses

## Data quality, limitations, and considerations
- Temporal scope
  - Snapshot from 1998/99; may not reflect current landscape conditions
- Spatial granularity
  - 1km square scale; some features are point-based within squares and may require careful spatial interpretation
- Complexity and standardization
  - Numerous coded fields (themes, attributes, species) that require careful metadata interpretation for proper cross-dataset use
- Data access and usability
  - Some datasets in environmental science are dispersed; this CS dataset emphasizes metadata and provenance
- Attribution and licensing
  - Must acknowledge Countryside Survey and CEH/NERC; ensure proper citation in analyses and outputs

## Attribution and references
- Acknowledgement text (to be used on publications): Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Key resources and publications
  - Countryside Survey Website (general overview and methodologies)
  - Bunce et al. (1996, 2007): ITE Land Classification of Great Britain and related materials
  - Jackson (2000): Guidance on Biodiversity Broad Habitat Classification interpretations
  - Related datasets and DOIs/links provided in the references

## Practical notes for analysts
- Plan for data cleaning and harmonization when merging with other CS datasets or external classifications
- Use LC07 (ITE Land Classification 2007) codes to align with land cover classifications in GB
- Leverage CANOPY_LIVE, EPIPHYTE_COVER, and IVY_COVER for habitat and biodiversity analyses
- Consider veteran tree indicators (dead, hollow, bark condition) for ecosystem resilience studies
- Ensure explicit data provenance and proper CS data acknowledgment in all outputs