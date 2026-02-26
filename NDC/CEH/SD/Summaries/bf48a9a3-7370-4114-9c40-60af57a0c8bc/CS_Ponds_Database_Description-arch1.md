# Freshwater pond quality data 2007 [Countryside Survey] Data Table Descriptions

- The document is a data table description set for Countryside Survey 2007 freshwater ponds, detailing three main tables and their fields, data types, and intended use.
- Data are from Countryside Survey data © NERC - Centre for Ecology & Hydrology and should be read alongside Murphy and Weatherby (2008) Freshwater Manual.

## Tables and primary fields

- POND_SITE_INFO.csv
  - SQUARE: Countryside Survey square code (text)
  - YEAR: Survey year (number)
  - AREA: Approximate pond area (m2) (number)
  - SURVEY_DATE: Date pond surveyed (date)
  - TOTAL_SUB_SP, TOTAL_FL_SP, TOTAL_EM_SP, TOTAL_WET_SP: Totals of submerged, floating-leaved, emergent, and overall wetland species (numbers)
  - RARE_SP: Rare species indicator (1/0)
  - GT30_PLANT_SP: Greater than 30 species record (1/0)
  - PSYM_GT75: PSYM score >75% (1/0)
  - PSYM_ASSESSMENT: PSYM assessment text
  - BAPPH_07: Designated as BAP Priority Habitat? (1/0)
  - WATER: Contains water? (Y/N for surveyed pond)
  - COND_SURVEY: Condition survey undertaken? (Y)
  - OPEN_PA: Pond in area of open public access? (1=yes)
  - VIEW_PROW: Visibility from public right of way? (1=yes)
  - LC07, LC07_NUM: Land class 2007 (text and numeric code)
  - ENV_ZONE_2007: Environmental zone (text; see key)
  - COUNTRY: England/Scotland/Wales (Eng/Sco/Wal)

- POND_MACROPHYTES.csv
  - SQUARE, YEAR: As above
  - SPECIES: Plant species name
  - PLANT_TYPE: Type (SUBMERGED, FLOATING, Emergent, Trees&Shrubs, Algae, Other wetland)
  - COVER_FLOATING, COVER_SUBMERGED, COVER_EMERGENT, COVER_TREE_SHADE: Percentage covers by plant type (percentages)
  - COVER: Total cover for totals where PLANT_TYPE applies
  - LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY: Land class, numeric code, environmental zone, country (as in site info)

- POND_WATER_QUALITY.csv
  - SQUARE, YEAR: As above
  - POND_AREA: Pond area (m2)
  - DRAWDOWN_HEIGHT: Drawdown height (cm)
  - PROPORTION_WATER_LEFT_IN_POND: Proportion of water left (%)
  - DRIED_OUT: Indicator of dried-out pond
  - PH: pH
  - CONDUCTIVITY: Conductivity (mS/l)
  - ALKALINITY: Alkalinity (mg/l)
  - TURBIDITY: Turbidity (ranked 1-4; turbid=1, clear=4)
  - PO4_P: PO4-P (mg/l)
  - TON: TON (mg/l)
  - LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY: Land class, numeric code, environmental zone, country (as in site info)

## Environmental zones

- Zone Code mappings (Environment Zone key)
  - 1 = Easterly lowlands (England)
  - 2 = Westerly lowlands (England)
  - 3 = Uplands (England)
  - 4 = Lowlands (Scotland)
  - 5 = Intermediate uplands and Islands (Scotland)
  - 6 = True uplands (Scotland)
  - 8 = Lowlands (Wales)
  - 9 = Uplands (Wales)
- These zone codes are used in LC07 and ENV_ZONE_2007 fields to classify environmental context.

## Data provenance, access, and usage

- Data originate from Countryside Survey and are governed by copyright and acknowledgement requirements.
- Acknowledgement to be used on all copies and publications: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and copyright notice.
- References point to Countryside Survey 2007 materials and the Freshwater Manual (Murphy & Weatherby, 2008).

## How analysts can use this data

- Link across tables using SQUARE and YEAR to build site-level pond profiles.
- Analyze relationships between:
  - Species richness and composition (TOTAL_SUB_SP, TOTAL_FL_SP, TOTAL_EM_SP, TOTAL_WET_SP) and water quality metrics (pH, turbidity, conductivity, PO4_P, TON).
  - Macrophyte cover by plant type (COVER_*) and pond environmental variables (POND_AREA, DRAWDOWN_HEIGHT, PROPORTION_WATER_LEFT_IN_POND).
  - Presence of rare species or PSYM indicators with habitat quality (BAPPH_07, PSYM_GT75, PSYM_ASSESSMENT).
  - Land class and environmental zone context (LC07, LC07_NUM, ENV_ZONE_2007) in relation to pond condition and water chemistry.
- Use for time-series or cross-sectional analyses at the pond level, with year fixed at 2007 for this dataset.
- Metadata and codes enable reproducibility and data discovery within CEH/NERC data portals.

## Data types and documentation notes

- Tables include a mix of text, numeric, date, and categorical indicators.
- FIELD descriptions provide unit guidance (e.g., area in m2, pH units, conductivity in mS/l) and coding for flags (1/0, Y/N).
- Environmental zone key and country codes facilitate regional comparisons and standardization across datasets.

## Acknowledgement and rights

- All use requires acknowledging Countryside Survey data ownership and copyright as described.
- Links to primary documentation include the Countryside Survey Freshwater Manual (Murphy & Weatherby, 2008) and associated data tables.