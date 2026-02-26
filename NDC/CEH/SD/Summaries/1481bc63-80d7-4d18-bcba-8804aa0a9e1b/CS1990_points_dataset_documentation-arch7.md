# Landscape point feature data 1990 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey capturing landscape point features from 451 1km squares across Great Britain, sampled in 1990.
- Curated by NERC - Centre for Ecology & Hydrology.
- Aims to support GIS-based map visualisations and spatial analyses of landscape features.

## Dataset structure and key fields
- Spatial key:
  - SQUARE: 1km square sampling site code (primary spatial unit).
  - COUNTRY, COUNTY07: country and county/district location.
  - EZ_DESC_07: Countryside Survey environmental zone description.
- Temporal and identifier fields:
  - YEAR: survey year (1990).
  - ID: landscape point identifier (unique within a year).
- Thematic and attribute fields:
  - THEME, THEME_NAME: theme category.
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME: primary attribute category.
  - SPECIES, SPECIES_NAME: species code and name.
  - PROPORTION, PROPORTION_RANGE: species cover value and range.
  - USE, USE_NAME: land use/structures theme use.
  - MODAL_DBH, MODAL_DBH_RANGE: modal diameter at breast height (DBH) and range.
  - LC07, LC07_NUM: ITE Land Classification of Great Britain 2007 (code and numeric).
- Metadata and provenance:
  - Contains codified values requiring decoding for human-readable mapping.
  - All uses of Countryside Survey data require acknowledgement.

## Spatial scope and sampling details
- 451 1km squares across Great Britain in 1990.
- Data designed for map-based presentation of landscape features, with geographic attributes at the 1km scale.

## How to use in GIS and recommended workflows
- GIS mapping:
  - Map SQUAREs to display spatial distribution of landscape features.
  - Use THEME_NAME, PRIMARY_ATTRIBUTE_NAME, SPECIES_NAME to create thematic layers.
  - Visualise PROPORTION or PROPORTION_RANGE to represent vegetation cover intensity.
  - Overlay LC07 (ITE Land Classification) for land-cover context.
  - Incorporate MODAL_DBH and MODAL_DBH_RANGE for tree size structure layers.
- Data integration:
  - Join by SQUARE with boundary shapefiles and other GB environmental datasets.
  - Decode codes to human-readable attributes (names) for legends and reporting.
- Data preparation considerations:
  - Expect codes needing translation to readable labels (THEME, SPECIES, USE, etc.).
  - 1990 baseline; consider temporal comparisons with other years if available.
  - Be mindful of potential data gaps and resolution limitations (1km scale).

## Quality, caveats, and governance
- Data quality relies on standard Countryside Survey methodologies; preprocessing may be needed to harmonise attributes across sources.
- Data is historical (1990); ensure alignment with current GIS projects and objectives.
- Data management challenges common in GIS work (disparate data sources, resolution limits, data cleaning).

## Attribution and licensing
- Acknowledgement required on all copies, publications, and presentations:
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## References and links
- Countryside Survey Website (general overview and methodologies).
- ITE Merlewood Land Classification of Great Britain (1996) and follow-up documents (classification descriptions and usage).
- JNCC guidance on Biodiversity Broad Habitat Classification (2000) and related literature.
- DOI/links provided for the ITE Land Classification 2007 dataset and related publications.