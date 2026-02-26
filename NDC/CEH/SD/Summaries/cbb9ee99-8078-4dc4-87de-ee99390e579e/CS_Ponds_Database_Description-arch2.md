# Freshwater pond quality data 2007 [Countryside Survey] Data Table Descriptions

- The document describes freshwater pond data collected in 2007 as part of the Countryside Survey, covering site information, macrophyte species, and water quality measurements. It accompanies the Countryside Survey Freshwater Manual (2008) and is © NERC - Centre for Ecology & Hydrology.

## Data Tables

- POND_SITE_INFO_V_0_1.csv
  - General pond-site information across survey squares and years
  - Key fields:
    - SQUARE: Countryside Survey square code
    - YEAR: Year of survey
    - AREA: Approximate pond area (m2)
    - SURVEY_DATE: Date pond was surveyed
    - Sub- and macro-vegetation metrics: TOTAL_SUB_SP, TOTAL_FL_SP, TOTAL_EM_SP, TOTAL_WET_SP
    - RARE_SP: Indicates presence of rare species (1/0)
    - GT30_PLANT_SP: More than 30 species recorded? (1/0)
    - PSYM_GT75: PSYM score > 75%? (1/0)
    - PSYM_ASSESSMENT: PSYM assessment text
    - BAPPH_07: Designated as BAP Priority Habitat? (1/0)
    - WATER: Contains water? (Y/N for surveyed pond)
    - COND_SURVEY: Condition survey undertaken? (Y/blank)
    - OPEN_PA: Pond in open public access area? (1=yes)
    - VIEW_PROW: Visibility from public right of way? (1=yes)
    - LC07 / LC07_NUM: Land class 2007 (text and numeric code)
    - ENV_ZONE_2007: Environmental zone (see key)
    - COUNTRY: England, Scotland, or Wales

- POND_MACROPHYTES.csv
  - Macrophyte records from ponds
  - Key fields:
    - SQUARE, YEAR
    - SPECIES: Plant species name
    - PLANT_TYPE: Type (SUBMERGED, FLOATING, Emergent, Trees & Shrubs, Algae, OTHER)
    - COVER: Percentage cover for totals where PLANT_TYPE applies
    - COVER_FLOATING / COVER_SUBMERGED / COVER_EMERGENT / COVER_TREE_SHADE: specific cover categories
    - LC07 / LC07_NUM, ENV_ZONE_2007, COUNTRY: Land class, zone, country

- POND_WATER_QUALITY.csv
  - Environmental and chemical data for each pond
  - Key fields:
    - SQUARE, YEAR
    - POND_AREA: Pond area (m2)
    - DRAWDOWN_HEIGHT: Drawdown height (cm)
    - PROPORTION_WATER_LEFT_IN_POND: Proportion of water left (%)
    - DRIED_OUT: Indicator pond dried out
    - PH, CONDUCTIVITY, ALKALINITY, TURBIDITY
    - PO4_P: Phosphate (mg/l)
    - TON: TON (mg/l)
    - LC07 / LC07_NUM, ENV_ZONE_2007, COUNTRY: Land class, zone, country

## Key variables and coding

- Land classification
  - LC07: Land class 2007 (text)
  - LC07_NUM: Land class 2007 (numeric code)
- Environmental zones
  - ENV_ZONE_2007: Environmental zone code (see key below)

- Environmental zone key
  - Zone Code 1: Easterly lowlands (England)
  - Zone Code 2: Westerly lowlands (England)
  - Zone Code 3: Uplands (England)
  - Zone Code 4: Lowlands (Scotland)
  - Zone Code 5: Intermediate uplands and Islands (Scotland)
  - Zone Code 6: True uplands (Scotland)
  - Zone Code 8: Lowlands (Wales)
  - Zone Code 9: Uplands (Wales)

- Country
  - Eng, Sco, or Wal (England, Scotland, or Wales)

## Usage notes and provenance

- Data are provided to enable standardised, comparable monitoring outputs and temporal analyses of pond condition and associated biodiversity and chemistry.
- The dataset draws on the Countryside Survey methodology and links to the Countryside Survey Freshwater Manual (Murphy & Weatherby, 2008).
- Acknowledgement and copyright
  - Acknowledge: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey ©: Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
  - All CS data must be acknowledged when used in copies, publications, reports, or presentations.