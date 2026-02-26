# Freshwater pond quality data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Metadata and table descriptions for freshwater pond data collected during the Countryside Survey 2007.
- DataTables cover site information, macrophyte (aquatic plant) records, and pond water quality measurements.
- Source: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology (CEH).

## Data Tables at a Glance

- POND_SITE_INFO_V_0_1.csv
  - General information about pond sites.
  - Key fields include: SQUARE (survey square code), YEAR, AREA (pond area in m2), SURVEY_DATE, counts of submerged/floating/emergent/wetland species, RARE_SP, GT30_PLANT_SP, PSYM_GT75, PSYM_ASSESSMENT, BAPPH_07 (BAP Priority Habitat), WATER (contains water?), OPEN_PA, VIEW_PROW, LC07 and LC07_NUM (land class 2007), ENV_ZONE_2007 (environmental zone), COUNTRY (England/Scotland/Wales).

- POND_MACROPHYTES.csv
  - Macrophyte (aquatic plant) records from ponds.
  - Key fields include: SQUARE, YEAR, SPECIES, PLANT_TYPE (SUBMERGED, FLOATING, Emergent, Trees & Shrubs, Algae, OTHER), COVER (percentage cover), LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.

- POND_WATER_QUALITY.csv
  - Environmental and chemical data for surveyed ponds.
  - Key fields include: SQUARE, YEAR, POND_AREA, DRAWDOWN_HEIGHT, PROPORTION_WATER_LEFT_IN_POND, DRIED_OUT, PH, CONDUCTIVITY, ALKALINITY, TURBIDITY, PO4_P, TON, LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.

## Key Variables and Measurements

- Site-level information (POND_SITE_INFO_V_0_1.csv)
  - Pond size and survey details: AREA (m2), SURVEY_DATE, YEAR.
  - Biodiversity indicators: TOTAL_SUB_SP, TOTAL_FL_SP, TOTAL_EM_SP, TOTAL_WET_SP, RARE_SP, GT30_PLANT_SP, PSYM_GT75, PSYM_ASSESSMENT.
  - Habitat designations: BAPPH_07, OPEN_PA, WATER, COND_SURVEY, VIEW_PROW.
  - Classification and geography: LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.

- Macrophyte records (POND_MACROPHYTES.csv)
  - Species-level data: SPECIES, PLANT_TYPE (SUBMERGED, FLOATING, Emergent, Trees & Shrubs, Algae, OTHER).
  - Abundance/cover: COVER (percentage), plus subcategory COVER_FLOATING, COVER_SUBMERGED, COVER_EMERGENT, COVER_TREE_SHADE.
  - Classification/zone: LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.

- Water quality metrics (POND_WATER_QUALITY.csv)
  - Physical/chemical properties: POND_AREA, DRAWDOWN_HEIGHT, PROPORTION_WATER_LEFT_IN_POND, DRIED_OUT, PH, CONDUCTIVITY, ALKALINITY, TURBIDITY, PO4_P, TON.
  - Classification/zone: LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.

## Environmental Zones

- Key to Environmental Zones provided to interpret ENV_ZONE_2007 values.
  - Zone codes correspond to descriptions such as Easterly lowlands (England), Westerly lowlands (England), Uplands (England), Lowlands/Uplands (Scotland/Wales), etc. Codes include 1–9 with specific regional mappings.

## Data Structure, Linking and Usability

- Common keys across tables enable linking and analysis:
  - SQUARE (survey square code), YEAR, LC07 / LC07_NUM, ENV_ZONE_2007, COUNTRY.
- Enables cross-table analyses, e.g., relating macrophyte cover (POND_MACROPHYTES.csv) to water chemistry (POND_WATER_QUALITY.csv) and site information (POND_SITE_INFO_V_0_1.csv).

## Data Access, Usage and Acknowledgement

- Usage must acknowledge Countryside Survey data owned by NERC - CEH.
- Copyright: Countryside Survey ©; all rights reserved.
- Acknowledgement text to be used on copies, publications, and presentations.

## Potential Analyses and Use Cases for Analysts

- Explore correlations between macrophyte cover/types and water quality metrics (PH, conductivity, turbidity, PO4_P, TON).
- Assess biodiversity indicators (TOTAL_SUB_SP, TOTAL_FL_SP, TOTAL_EM_SP, TOTAL_WET_SP) in relation to pond area, drawdown, and environmental zones.
- Model the Predictive System for Multimetrics (PSYM) outputs and their relationship to pond characteristics and habitat designation (BAPPH_07, PSYM_GT75).
- Compare pond characteristics across environmental zones and countries to identify regional patterns.
- Identify ponds designated as BAP Priority Habitat and analyze associated site characteristics and biodiversity indicators.
- Spatial and temporal linking (within 2007 data) to examine scale-dependent patterns (e.g., pond area vs. macrophyte richness).

## Limitations and Considerations

- Data pertain to the 2007 Countryside Survey; applicability to other years requires caution.
- Some fields may have missing values; consider data quality checks when integrating tables.
- Table version noted for site info: POND_SITE_INFO_V_0_1.csv; ensure compatibility when combining with other releases.
- Scale and access constraints typical of environmental datasets; ensure proper metadata and provenance are maintained.