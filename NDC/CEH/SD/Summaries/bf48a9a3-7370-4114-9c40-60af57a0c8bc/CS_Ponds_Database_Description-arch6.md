# Freshwater pond quality data 2007 [Countryside Survey] Data Table Descriptions

- A set of data table descriptions from the Countryside Survey 2007 focusing on freshwater pond quality, published by NERC - Centre for Ecology & Hydrology.
- Documents three main data tables and a key to environmental zones, plus guidance on usage and acknowledgement.
- Intended to support analysis of pond sites, macrophyte communities, and water quality for ecological assessment and monitoring.

## POND_SITE_INFO.csv — General pond site information

- SQUARE: Countryside Survey square code (text)
- YEAR: Year of survey (number)
- AREA: Approximate pond area from pond condition sheet (m2)
- SURVEY_DATE: Date pond surveyed (date)
- TOTAL_SUB_SP / TOTAL_FL_SP / TOTAL_EM_SP / TOTAL_WET_SP: Total submerged, floating-leaved, emergent, and wetland species counts (numbers)
- RARE_SP: Contains rare species? (1/0)
- GT30_PLANT_SP: Greater than 30 plant species recorded? (1/0)
- PSYM_GT75: PSYM score >75%? (1/0)
- PSYM_ASSESSMENT: PSYM assessment (text)
- BAPPH_07: Designated as BAP Priority Habitat? (1/0)
- WATER: Contains water? (Y/N; for surveyed pond)
- COND_SURVEY: Condition survey undertaken? (Y/blank)
- OPEN_PA: Pond in area of open public access? (1/0)
- VIEW_PROW: Visibility from a public right of way? (1/0)
- LC07 / LC07_NUM: Land class 2007 (text and numeric code)
- ENV_ZONE_2007: Environmental zone (text; see zone key)
- COUNTRY: England, Scotland or Wales

- A secondary component provides variables from the Pond Condition recording sheet, describing:
  - SQUARE, YEAR, VARIABLE, DESCRIPTION, CODE, PERCENT, CODE_DESC, RANK, TYPE
  - LC07 / LC07_NUM, ENV_ZONE_2007, COUNTRY (as above)

## POND_MACROPHYTES.csv — Macrophyte records from ponds

- SQUARE: Countryside Survey square code (text)
- YEAR: Year of survey (number)
- SPECIES: Plant species name (text)
- PLANT_TYPE: Type of plant (e.g., SUBMERGED, FLOATING, Emergent, Trees & Shrubs, Algae, OTHER)
- COVER_FLOATING / COVER_SUBMERGED / COVER_EMERGENT / COVER: Percentage cover for totals by plant type (numbers)
- LC07 / LC07_NUM: Land class 2007 (text and numeric code)
- ENV_ZONE_2007: Environmental zone (text)
- COUNTRY: England, Scotland or Wales (text)

## POND_WATER_QUALITY.csv — Environmental and chemical data (ponds)

- SQUARE: Countryside Survey square code (text)
- YEAR: Survey year (the dataset uses VARCHAR2 for year)
- POND_AREA: Area of pond (m2)
- DRAWDOWN_HEIGHT: Drawdown height (cm)
- PROPORTION_WATER_LEFT_IN_POND: Proportion of water left in the pond (%)
- DRIED_OUT: Indicator of dried out pond (numeric)
- PH: pH (numeric)
- CONDUCTIVITY: Conductivity (mS/l)
- ALKALINITY: Alkalinity (mg/l)
- TURBIDITY: Turbidity (ranked scale; 1 = turbid, 4 = clear)
- PO4_P: PO4-P (mg/l)
- TON: TON (mg/l)
- LC07 / LC07_NUM: Land class 2007 (text and numeric code)
- ENV_ZONE_2007: Environmental zone (text)
- COUNTRY: England, Scotland or Wales (text)

## Key to Environmental Zones

- Zone Code 1: Easterly lowlands (England)
- Zone Code 2: Westerly lowlands (England)
- Zone Code 3: Uplands (England)
- Zone Code 4: Lowlands (Scotland)
- Zone Code 5: Intermediate uplands and Islands (Scotland)
- Zone Code 6: True uplands (Scotland)
- Zone Code 8: Lowlands (Wales)
- Zone Code 9: Uplands (Wales)

## Usage and Acknowledgement

- All use of Countryside Survey data must be acknowledged as follows:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## References

- Murphy, John; Weatherby, Anita. 2008. Countryside Survey. Freshwater Manual. NERC/Centre for Ecology & Hydrology, 71pp. CS Technical Report No.5/07. (CS_UK_2007_TR5 document and related materials)