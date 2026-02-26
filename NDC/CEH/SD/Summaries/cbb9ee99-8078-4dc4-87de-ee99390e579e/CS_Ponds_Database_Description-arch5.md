# Freshwater pond quality data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Defines three CSV tables that accompany the Countryside Survey freshwater dataset: Pond site information, macrophyte records, and pond water quality.
- Serves as the data dictionary and metadata reference to accompany the Countryside Survey Freshwater Manual ( Murphy & Weatherby 2008).

## Tables and key fields

- POND_SITE_INFO_V_0_1.csv
  - General pond-site information with fields such as:
    - SQUARE (Countryside Survey square code)
    - YEAR (survey year)
    - AREA (approximate pond area in m2)
    - SURVEY_DATE (date pond was surveyed)
    - Submerged, floating-leaved, emergent, and total wetland species counts (TOTAL_SUB_SP, TOTAL_FL_SP, TOTAL_EM_SP, TOTAL_WET_SP)
    - RARE_SP, GT30_PLANT_SP, PSYM_GT75, PSYM_ASSESSMENT
    - BAPPH_07 (BAP Priority Habitat indicator)
    - WATER, COND_SURVEY, OPEN_PA, VIEW_PROW
    - LC07, LC07_NUM (Land class 2007)
    - ENV_ZONE_2007, COUNTRY
  - Also includes flags and descriptors related to pond condition and classification.

- POND_MACROPHYTES.csv
  - Macrophyte records with fields such as:
    - SQUARE, YEAR, SPECIES, PLANT_TYPE (Submerged, Floating, Emergent, Trees& Shrubs, Algae, Other wetland)
    - COVER_FLOATING, COVER_SUBMERGED, COVER_EMERGENT, COVER (percent covers)
    - LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY
  - Describes plant occurrences and cover by plant type across ponds.

- POND_WATER_QUALITY.csv
  - Environmental and chemical data for surveyed ponds with fields such as:
    - SQUARE, YEAR (note YEAR may be VARCHAR2 in this table)
    - POND_AREA, DRAWDOWN_HEIGHT, PROPORTION_WATER_LEFT_IN_POND, DRIED_OUT
    - PH, CONDUCTIVITY, ALKALINITY, TURBIDITY, PO4_P, TON
    - LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY
  - Captures water quality metrics and pond physical characteristics.

## Standards and classifications

- Environmental zones: Key to Environmental Zones (ENV_ZONE_2007) with a mapping to zone descriptions (1 = Easterly lowlands Eng, 2 = Westerly lowlands Eng, 3 = Uplands Eng, 4 = Lowlands Scotland, 5 = Intermediate uplands/Islands Scotland, 6 = True uplands Scotland, 8 = Lowlands Wales, 9 = Uplands Wales).
- Land class: LC07 and LC07_NUM reference the ITE Land Classification of Great Britain 2007.
- Country coding: COUNTRY field indicates England (Eng), Scotland (Sco), or Wales (Wal).

## Data quality, governance, and provenance

- Data types vary by table (e.g., SURVEY_DATE as date; YEAR sometimes numeric; YEAR as VARCHAR2 in water quality), which has implications for data integration and validation.
- Tables include descriptive fields (DESCRIPTION, CODE, CODE_DESC, RANK, TYPE, YEAR) for variables drawn from the pond condition recording sheet, enabling traceability and interpretation.
- PSYM fields (PSYM_GT75, PSYM_ASSESSMENT) provide a multimetrics assessment, supporting cross-table usability and user needs.

## Licensing, acknowledgement, and usage

- All Countryside Survey data must be acknowledged.
- Required acknowledgement text:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Data usage and sharing should reference the Countryside Survey materials and the related manuals (Murphy & Weatherby 2008).

## Practical considerations for Data Stewards

- Ensure consistent metadata alignment across the three tables (POND_SITE_INFO_V_0_1.csv, POND_MACROPHYTES.csv, POND_WATER_QUALITY.csv).
- Validate cross-table keys (SQUARE, YEAR) to enable reliable joins and aggregations.
- Normalize data types where possible (e.g., harmonize YEAR field formats; confirm surface area units in AREA across tables).
- Maintain and communicate adherence to environmental zone and land class coding standards (ENV_ZONE_2007, LC07, LC07_NUM).
- Preserve and enforce the required acknowledgement when data are used or published.
- Be aware of potential challenges when integrating with other CS datasets: incomplete user needs, data inhomogeneity across formats, and the need for updates to reflect ongoing surveys.

## References and further reading

- Murphy, John; Weatherby, Anita. 2008 Countryside Survey. Freshwater Manual. NERC/Centre for Ecology & Hydrology, 71pp. CS Technical Report No.5/07.
- ITE Land Classification of Great Britain 2007 (LC07) and related ENV_ZONE_2007 documentation.
- Countryside Survey data access and documentation at NERC CEH and associated portals.