# Freshwater pond quality data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Describes freshwater pond data collected as part of the Countryside Survey (CS) 2007.
- Data tables provide site-level information, macrophyte composition, and water quality measurements from surveyed ponds.
- Source references: Murphy, John; Weatherby, Anita. 2008 Countryside Survey. Freshwater Manual. NERC/CEH; CS Technical Report No.5/07.

## Data Tables and Descriptions
- POND_SITE_INFO.csv
  - General pond site attributes across CS squares and survey year.
  - Key fields: SQUARE (CS square code), YEAR, AREA (pond area in m2), SURVEY_DATE, TOTAL_SUB_SP, TOTAL_FL_SP, TOTAL_EM_SP, TOTAL_WET_SP, RARE_SP, GT30_PLANT_SP, PSYM_GT75, PSYM_ASSESSMENT, BAPPH_07, WATER, OPEN_PA, VIEW_PROW, LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.
  - Additional status indicators: COND_SURVEY (condition survey undertaken), and descriptive fields related to land class and environmental zones.
- POND_MACROPHYTES.csv
  - Macrophyte species recorded in ponds.
  - Key fields: SQUARE, YEAR, SPECIES, PLANT_TYPE (Submerged, Floating, Emergent, Trees& Shrubs, Algae, Other), COVER or COVER_FLOATING/COVER_SUBMERGED/COVER_EMERGENT, LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.
- POND_WATER_QUALITY.csv
  - Environmental and chemical pond data.
  - Key fields: SQUARE, YEAR, POND_AREA, DRAWDOWN_HEIGHT, PROPORTION_WATER_LEFT_IN_POND, DRIED_OUT, PH, CONDUCTIVITY, ALKALINITY, TURBIDITY, PO4_P, TON, LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.
- Key mappings and classifications
  - Key to Environmental Zones (ENV_ZONE_2007): zone codes map to descriptive environmental zones (e.g., Easterly lowlands England, uplands Scotland, etc.).
  - Land Classification: LC07 and LC07_NUM provide the ITE Land Classification of Great Britain 2007 codes.
  - Country indicates England, Scotland, or Wales.

## Variables and Metrics of Interest
- Pond site and survey context: square code, year, survey date, pond area.
- Biodiversity metrics: counts of submerged, floating-leaved, emergent, and total wetland species; rare species indicator; BAP Priority Habitat designation (BAPPH_07); PSYM score indicators (PSYM_GT75, PSYM_ASSESSMENT).
- Vegetation cover: percentage cover by macrophyte type (COVER values for submerged, floating, emergent; additional cover fields for trees/shade or other categories).
- Water quality and physical-chemical parameters: pH, conductivity, alkalinity, turbidity, phosphate (PO4_P), TON; pond drawdown height; proportion of water remaining; dried-out status.
- Habitat classification: LC07 codes with numeric equivalents (LC07_NUM) and ENvIRONMENTAL zone classifications (ENV_ZONE_2007).
- Accessibility and openness indicators: OPEN_PA (public access), WATER presence flag, VIEW_PROW (visibility from public right of way).

## Data Governance, Quality and Usage Considerations
- Metadata completeness and standardization: fields draw on CS standard recording sheets and the ITE Land Classification framework; some fields may require data transformation or careful metadata interpretation (e.g., YEAR as VARCHAR2 in some tables).
- Data sharing and openness: underlying data and outputs should be shared with appropriate governance; note presence of numerous location- and species-level data that may require careful handling for dissemination.
- Data quality and provenance: data are compiled from pond condition sheets and survey records; quality assurance, cleaning, transformation, and clear presentation (through reports, charts, or dashboards) are implied aims for making the data usable in monitoring workflows.
- Data governance and provenance barriers: potential barriers include siloed datasets, need for metadata, and ensuring datasets meet standards before storage or sharing.

## Acknowledgement and Usage Conditions
- All Countryside Survey data must be acknowledged in outputs.
- Acknowledgement statement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey ©; all rights reserved.
- Public sharing of the data used is encouraged, but requires proper acknowledgement and adherence to copyright.

## References
- Murphy, John; Weatherby, Anita. 2008 Countryside Survey. Freshwater Manual. NERC/Centre for Ecology & Hydrology. 71pp. CS Technical Report No.5/07.