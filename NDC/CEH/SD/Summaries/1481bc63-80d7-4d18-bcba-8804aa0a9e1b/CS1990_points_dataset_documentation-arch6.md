# Landscape point feature data 1990 [Countryside Survey], Great Britain

## Overview
- Landscape point features from 451 1km squares across Great Britain, sampled in 1990.
- Source: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology (CEH).
- Dataset file: LANDSCAPE_PT_FEATURES_1990.csv containing per-site feature observations.

## Data contents and structure
- Sampling unit: 1km square (SQUARE) with a yearly record (YEAR).
- Identifier: ID is unique within each year.
- Feature coding: THEME (code) and THEME_NAME; PRIMARY_ATTRIBUTE (code) and PRIMARY_ATTRIBUTE_NAME.
- Biological data: SPECIES (code) and SPECIES_NAME; PROPORTION (cover) and PROPORTION_RANGE.
- Land use: USE (code) and USE_NAME.
- Woody feature: MODAL_DBH (code) and MODAL_DBH_RANGE.
- Land classification: LC07 (text code) and LC07_NUM.
- Geography: COUNTRY (ENG, SCO, WAL) and COUNTY07.
- Environment: EZ_DESC_07 describes Countryside Survey Environmental Zone.
- All fields include human-readable name equivalents for codes.

## How to use
- Interpret coded values using corresponding NAME fields for clarity.
- Combine with LC07 (ITE Land Classification) for landscape classification context.
- Potential analyses:
  - Spatial distribution of landscape features across GB 1km squares.
  - Relationships between land use, species cover, and DBH characteristics.
  - Cross-tabulations between theme attributes and environmental zones.
- Output options: dashboards, pivot tables, and reports with guidance on tool usage.

## Data quality and access considerations
- Acknowledge Countryside Survey data in all uses.
- Data involves multiple classifications and codes; ensure consistent interpretation across outputs.
- Country-level and county-level fields enable regional filtering and analysis.

## Acknowledgement and rights
- Acknowledgement requirement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Copyright: Countryside Survey ©; Database Right/Copyright NERC-CEH. All rights reserved.
- Use in publications, presentations, and copies must include the acknowledgement.

## References and further information
- Countryside Survey website: http://www.countrysidesurvey.org.uk/
- ITE Merlewood Land Classification references (Bunce et al., 1996; 1981) and ITE Land Classification 2007 (Bunce et al., 2007) with DOIs/links.
- Jackson, D.L. (2000) guidance on Biodiversity Broad Habitat Classification (JNCC Report 307).
- NERC Environmental Information Data Centre DOI references for ITE Land Classification 2007 dataset.
- Additional documentation and methodologies available through the Countryside Survey publications and links provided.