# Freshwater pond quality data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Describes three Countryside Survey freshwater pond data tables (2007) used for GIS and map-based data products.
- Data produced by NERC – Centre for Ecology & Hydrology; referenced in Murphy & Weatherby (2008) Countryside Survey Freshwater Manual.
- Tables enable integration of pond site information, macrophyte composition, and water quality for spatial analysis and visualization.
- Data are UK-wide (England, Scotland, Wales) and include environmental zone and land-class coding.

## Data Tables and Key Fields

- POND_SITE_INFO_V_0_1.csv
  - SQUARE: Countryside Survey square code (text) – join key.
  - YEAR: Survey year (number).
  - AREA: Approximate pond area (m2).
  - SURVEY_DATE: Date pond surveyed.
  - TOTAL_SUB_SP, TOTAL_FL_SP, TOTAL_EM_SP, TOTAL_WET_SP: Counts of submerged, floating-leaved, emergent, and overall wetland species.
  - RARE_SP: Indicates presence of rare species (1/0).
  - GT30_PLANT_SP: Greater than 30 species (1/0).
  - PSYM_GT75, PSYM_ASSESSMENT: Predictive System for Multimetrics metrics and assessment (1/0 and text).
  - BAPPH_07: Designated as BAP Priority Habitat? (1/0).
  - WATER: Contains water? (Y/N for surveyed pond).
  - COND_SURVEY: Condition survey undertaken? (Y/N).
  - OPEN_PA, VIEW_PROW: Public access and visibility from public right of way (1/0).
  - LC07, LC07_NUM: Land classification 2007 (text and numeric code) per Bunce et al.
  - ENV_ZONE_2007: Environmental zone (text).
  - COUNTRY: England, Scotland or Wales.

- POND_MACROPHYTES.csv
  - SQUARE, YEAR: Join keys.
  - SPECIES: Plant species name.
  - PLANT_TYPE: Submerged, Floating, Emergent, Trees & Shrubs, Algae, Other wetland.
  - COVER_FLOATING, COVER_SUBMERGED, COVER_EMERGENT, COVER_TREE_SHADE: Percent cover for each plant type (where applicable).
  - COVER: Overall percent cover (totals where PLANT_TYPE indicates cover data).
  - LC07, LC07_NUM: Land classification 2007 (text and numeric code).
  - ENV_ZONE_2007, COUNTRY: Environmental zone and country (as above).

- POND_WATER_QUALITY.csv
  - SQUARE, YEAR: Join keys (YEAR as VARCHAR2 in this table).
  - POND_AREA: Pond area (m2).
  - DRAWDOWN_HEIGHT: Drawdown height (cm).
  - PROPORTION_WATER_LEFT_IN_POND: Percent water remaining.
  - DRIED_OUT: Pond dried out indicator.
  - PH, CONDUCTIVITY, ALKALINITY, TURBIDITY, PO4_P, TON: Water quality/chemistry parameters.
  - LC07, LC07_NUM: Land classification 2007 (text and numeric code).
  - ENV_ZONE_2007, COUNTRY: Environmental zone and country.

- Key cross-table identifiers
  - SQUARE and YEAR are the primary keys to align records across tables for GIS joins.
  - LC07/ENV_ZONE_2007/COUNTRY provide standardized context for spatial analysis and classification.

## Environmental Zones
- Key to Environmental Zones (ENV_ZONE_2007)
  - 1: Easterly lowlands (England)
  - 2: Westerly lowlands (England)
  - 3: Uplands (England)
  - 4: Lowlands (Scotland)
  - 5: Intermediate uplands and Islands (Scotland)
  - 6: True uplands (Scotland)
  - 8: Lowlands (Wales)
  - 9: Uplands (Wales)

## Data Standards and Use
- Land classification: LC07 and LC07_NUM reference the ITE Land Classification of Great Britain 2007.
- Environmental zones: ENV_ZONE_2007 provides zonal context with a linked key.
- Country field: COUNTRY indicates England (Eng), Scotland (Sco), or Wales (Wal).
- Survey year: 2007 Countryside Survey data; includes approximate pond area and condition indicators.
- Data integration: Suitable for creating pond-level GIS features by joining tables on SQUARE and YEAR, enabling maps of pond distribution, macrophyte communities, and water quality.

## Usage Notes for GIS Specialists
- Ideal for map-based analyses and dashboards that illustrate pond presence, species richness (submerged, floating, emergent), vegetation cover, and water quality gradients.
- Use joins on SQUARE and YEAR to build comprehensive pond features with attached macrophyte and water quality attributes.
- Leverage environmental zone and land classification as contextual layers to examine spatial patterns and management implications.
- Acknowledge data properly in any maps, publications, or presentations.

## Acknowledgement and Licensing
- All Countryside Survey data must be acknowledged.
- Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © NERC- Centre for Ecology & Hydrology. All rights reserved.
- Include data citations as per the provided notice in any copies, publications, or presentations.

## References
- Murphy, John; Weatherby, Anita. 2008. Countryside Survey Freshwater Manual. NERC/Centre for Ecology & Hydrology, 71pp. CS Technical Report No.5/07. CEH Project Number: C03259.
- Additional source: ITE Land Classification of Great Britain 2007 (for LC07/LC07_NUM).