# Freshwater pond quality data 2007 [Countryside Survey] Data Table Descriptions

- A Countryside Survey data description for pond-related datasets from 2007, including general site information, macrophyte assemblages, and water quality measurements. The material accompanies the Countryside Survey Freshwater Manual ( Murphy & Weatherby, 2008 ) and is © NERC - Centre for Ecology & Hydrology.

## Tables and their purpose

- POND_SITE_INFO.csv
  - General information about pond sites.
  - Key fields include: SQUARE (site code), YEAR, AREA (m2), SURVEY_DATE, totals of submerged/floatation/emergent/wetland species, RARE_SP, GT30_PLANT_SP, PSYM_GT75, PSYM_ASSESSMENT, BAPPH_07, WATER, COND_SURVEY, OPEN_PA, VIEW_PROW, LC07 and LC07_NUM (Land Classification 2007), ENV_ZONE_2007, COUNTRY.
  - Also includes a separate block described as “Variables from Pond Condition recording sheet” with: SQUARE, VARIABLE, DESCRIPTION, CODE, PERCENT, CODE_DESC, RANK, TYPE, YEAR, LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.

- POND_MACROPHYTES.csv
  - Macrophyte data recorded in ponds.
  - Key fields include: SQUARE, YEAR, SPECIES, PLANT_TYPE (e.g., SUBMERGED, FLOATING, Emergent, Trees & Shrubs, Algae, Other wetland), COVER_FLOATING, COVER_SUBMERGED, COVER_EMERGENT, COVER_TREE_SHADE, COVER, LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.

- POND_WATER_QUALITY.csv
  - Environmental and chemical data for sampled ponds.
  - Key fields include: SQUARE, YEAR, POND_AREA, DRAWDOWN_HEIGHT, PROPORTION_WATER_LEFT_IN_POND, DRIED_OUT, PH, CONDUCTIVITY, ALKALINITY, TURBIDITY (ranked scale: turbid = 1, clear = 4), PO4_P, TON, LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.

## Environmental zones and classification

- Key to Environmental Zones: mapping for ENV_ZONE_2007 (with codes 1–9) corresponding to regional descriptions (e.g., Easterly/Westerly lowlands, uplands/lowlands in England, Scotland, and Wales).

- LC07/Land Classification 2007: references to the ITE Land Classification of Great Britain 2007 for standardised land-cover context.

## Data governance and attribution

- All Countryside Survey data must be acknowledged with:
  - Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
  - Copyright: Countryside Survey © NERC - Centre for Ecology & Hydrology. All rights reserved.

- Source and accompanying materials:
  - Primary reference: Murphy, John; Weatherby, Anita. 2008. Countryside Survey. Freshwater Manual. NERC/Centre for Ecology & Hydrology, 71pp. (CS Technical Report No.5/07).
  - Link to related technical report: CS_UK_2007_TR5.

## Relevance for Data Leaders

- Provides a cohesive dataset foundation for pond ecology analyses, linking site-level information, macrophyte communities, and water quality, enabling end-to-end data product development.
- Highlights the importance of consistent metadata (LC07, ENV_ZONE_2007, COUNTRY) to support cross-dataset joins (e.g., by SQUARE and YEAR).
- Demonstrates the need for standardized taxonomic and environmental classifications (e.g., Land Classification 2007, environmental zones) to enhance interoperability and reuse across networks.
- Illustrates data governance requirements (acknowledgement and rights) essential for multi-party data sharing and dissemination.
- Indicates potential data-management tasks: ensuring data from the three tables is discoverable, correctly formatted, and kept up to date; managing metadata for variables from the pond condition recording sheet; and integrating legacy survey data with newer or external data sources.