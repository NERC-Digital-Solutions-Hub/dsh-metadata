# Freshwater pond quality data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Data from the Countryside Survey 2007, focused on freshwater pond quality.
- Document provides table descriptions and field-level metadata for three main CSV tables and associated variables.
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology; references Murphy & Weatherby (2008) Freshwater Manual for context.
- Tables describe general pond site information, macrophyte recordings, and pond water quality; includes environmental zone classifications and country.

## Tables and key fields

### POND_SITE_INFO.csv
- Purpose: General information regarding pond sites.
- Key fields:
  - SQUARE: Countryside Survey square code (text)
  - YEAR: Year of survey (number)
  - AREA: Approximate pond area from pond condition sheet (m2) (number)
  - SURVEY_DATE: Date pond surveyed (date)
  - TOTAL_SUB_SP, TOTAL_FL_SP, TOTAL_EM_SP, TOTAL_WET_SP: counts of submerged, floating-leaved, emergent, and total wetland species (numbers)
  - RARE_SP: Contains rare species? (1 or 0)
  - GT30_PLANT_SP: Greater than 30 species recorded? (1 or 0)
  - PSYM_GT75: PSYM score greater than 75%? (1 or 0)
  - PSYM_ASSESSMENT: PSYM assessment (text)
  - BAPPH_07: Designated as BAP Priority Habitat? (1 or 0)
  - WATER: Contains water? (Y or N, for surveyed pond)
  - COND_SURVEY: Condition survey undertaken? (Y or blank)
  - OPEN_PA: Pond in area of open public access? (1=yes)
  - VIEW_PROW: Visibility from a public right of way? (1=yes)
  - LC07, LC07_NUM: Land class 2007 (text and numeric code)
  - ENV_ZONE_2007: Environmental zone (text)
  - COUNTRY: England, Scotland or Wales (text)

### POND_MACROPHYTES.csv
- Purpose: Macrophytes recorded from ponds during Countryside Survey.
- Key fields:
  - SQUARE, YEAR: as above
  - SPECIES: Name of plant species (text)
  - PLANT_TYPE: Type of plant (Submerged, Floating, Emergent, Trees & Shrubs, Algae, Other wetland)
  - COVER_FLOATING, COVER_SUBMERGED, COVER_EMERGENT, COVER_TREE_SHADE: Percent cover for totals by plant type (numbers)
  - COVER: Percentage cover for totals where PLANT_TYPE is a cover category (number)
  - LC07, LC07_NUM: Land class 2007 (text and numeric)
  - ENV_ZONE_2007: Environmental zone (text)
  - COUNTRY: England, Scotland or Wales (text)

### POND_WATER_QUALITY.csv
- Purpose: Environmental and chemical data for surveyed ponds.
- Key fields:
  - SQUARE, YEAR: as above (YEAR stored as VARCHAR2 in this table)
  - POND_AREA: Area of pond (m2) (number)
  - DRAWDOWN_HEIGHT: Drawdown height (cm) (number)
  - PROPORTION_WATER_LEFT_IN_POND: Proportion of water left in the pond (%) (number)
  - DRIED_OUT: Indicator of dried out pond (number)
  - PH: pH (number)
  - CONDUCTIVITY: Conductivity (mS/l) (number)
  - ALKALINITY: Alkalinity (mg/l) (number)
  - TURBIDITY: Turbidity (ranked scale; 1 = turbid, 4 = clear) (number)
  - PO4_P: PO4-P (mg/l) (number)
  - TON: TON (mg/l) (number)
  - LC07, LC07_NUM: Land class 2007 (text and numeric)
  - ENV_ZONE_2007: Environmental zone (text)
  - COUNTRY: England, Scotland or Wales (text)

## Environmental zone codes
- Key to Environmental Zones provided:
  - Zone codes 1–9 map to descriptions such as Easterly lowlands (England), Westerly lowlands (England), Uplands (England/Scotland/Wales), Lowlands/Highland variants (Scotland/Wales), and other upland categories.
- ENV_ZONE_2007 field uses these zone descriptions to classify pond locations.

## Data governance, provenance, and acknowledgment
- All Countryside Survey data must be acknowledged in publications, presentations, and copies:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Data are linked to the Countryside Survey 2007 freshwater dataset and should be interpreted with the accompanying Freshwater Manual (Murphy & Weatherby, 2008) for full methodological context.

## Practical considerations for Data Stewards
- Ensure metadata consistency across tables, including units (e.g., area in m2, pH, conductivity in mS/l, turbidity scale) and data types.
- Maintain accurate linkages between tables via common keys (SQUARE, YEAR) and ensure year-specific environmental zone mappings (ENV_ZONE_2007) are correctly applied.
- Track and preserve the provenance and licensing restrictions, including the explicit acknowledgment requirements.
- Be mindful of potential data quality issues noted in the broader dataset (e.g., completeness of fields like COND_SURVEY, WATER presence, BAPPH_07 flags) and document any gaps or ambiguities.
- If integrating with other systems, consider the multilingual or code-based references (LC07/ENV_ZONE_2007) and provide needed mappings to ensure interoperability.