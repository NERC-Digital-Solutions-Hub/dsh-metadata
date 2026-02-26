# Freshwater pond quality data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Source: Countryside Survey data; reference Murphy & Weatherby (2008) Countryside Survey. Freshwater Manual; CS Technical Report No.5/07.
- Purpose: Data table descriptions for pond-related data collected during the 2007 Countryside Survey, describing site information, macrophytes, and water quality.
- Tables included: POND_SITE_INFO.csv, POND_MACROPHYTES.csv, POND_WATER_QUALITY.csv.
- Acknowledgement: All CS data must be acknowledged as Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.

## Tables and key fields

### POND_SITE_INFO.csv
- SQUARE — Type: Text. Description: Countryside Survey square code.
- YEAR — Type: Number. Description: Year of survey.
- AREA — Type: Number. Description: Approximate pond area (m2) from pond condition sheet.
- SURVEY_DATE — Type: Date. Description: Date pond surveyed.
- TOTAL_SUB_SP — Type: Number. Description: Total submerged species recorded.
- TOTAL_FL_SP — Type: Number. Description: Total floating-leaved species recorded.
- TOTAL_EM_SP — Type: Number. Description: Total emergent species recorded.
- TOTAL_WET_SP — Type: Number. Description: Total wetland species recorded overall.
- RARE_SP — Type: Number. Description: Contains rare species? 1 or 0.
- GT30_PLANT_SP — Type: Number. Description: Greater than 30 species recorded? 1 or 0.
- PSYM_GT75 — Type: Number. Description: PSYM score greater than 75%? 1 or 0.
- PSYM_ASSESSMENT — Type: Text. Description: PSYM assessment.
- BAPPH_07 — Type: Number. Description: Designated as BAP Priority Habitat? 1 or 0.
- WATER — Type: Text. Description: Contains water? Y or N (surveyed pond only).
- COND_SURVEY — Type: Number. Description: Condition survey undertaken? Y or (see field).
- OPEN_PA — Type: Number. Description: Pond in area of open public access? 1 = yes.
- VIEW_PROW — Type: Number. Description: Visibility from a public right of way? 1 = yes.
- LC07 — Type: Text. Description: Land class 2007.
- LC07_NUM — Type: Number. Description: Land class 2007 (numeric code).
- ENV_ZONE_2007 — Type: Text. Description: Environmental zone (see key below).
- COUNTRY — Type: Text. Description: England (Eng), Scotland (Sco) or Wales (Wal).

### POND_MACROPHYTES.csv
- SQUARE — Text. Countryside Survey square code.
- YEAR — Number. Year of survey.
- SPECIES — Text. Name of plant species.
- PLANT_TYPE — Text. Type of plant (Submerged; Floating; Emergent; Trees & Shrubs; Algae; Other wetland).
- COVER_FLOATING, COVER_SUBMERGED, COVER_EMERGENT, COVER_TREE_SHADE — Type: Number. Description: Percentage covers for totals where PLANT_TYPE corresponds.
- COVER — Type: Number. Description: Percentage cover for totals where PLANT_TYPE indicates cover.
- LC07 — Text. Land class 2007.
- LC07_NUM — Number. Land class 2007 (numeric code).
- ENV_ZONE_2007 — Text. Environmental zone.
- COUNTRY — Text. England, Scotland or Wales.

### POND_WATER_QUALITY.csv
- SQUARE — Text. Countryside Survey square code.
- YEAR — VARCHAR2. Year of survey.
- POND_AREA — Number. Area of pond (m2).
- DRAWDOWN_HEIGHT — Number. Drawdown height (cm).
- PROPORTION_WATER_LEFT_IN_POND — Number. Proportion of water left in the pond (%).
- DRIED_OUT — Number. Indicator of dried out pond.
- PH — Number. pH.
- CONDUCTIVITY — Number. Conductivity (mS/l).
- ALKALINITY — Number. Alkalinity (mg/l).
- TURBIDITY — Number. Turbidity (ranked scale; 1 = turbid, 4 = clear).
- PO4_P — Number. PO4-P (mg/l).
- TON — Number. TON (mg/l).
- LC07 — Text. Land class 2007.
- LC07_NUM — Number. Land class 2007 (numeric code).
- ENV_ZONE_2007 — Text. Environmental zone.
- COUNTRY — Text. England, Scotland or Wales.

## Key to Environmental Zones
- 1 — Easterly lowlands (England)
- 2 — Westerly lowlands (England)
- 3 — Uplands (England)
- 4 — Lowlands (Scotland)
- 5 — Intermediate uplands and Islands (Scotland)
- 6 — True uplands (Scotland)
- 8 — Lowlands (Wales)
- 9 — Uplands (Wales)

## Data usage and licensing
- All uses of Countryside Survey data must be acknowledged.
- Acknowledgement text (to use on publications, presentations, etc.):
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.