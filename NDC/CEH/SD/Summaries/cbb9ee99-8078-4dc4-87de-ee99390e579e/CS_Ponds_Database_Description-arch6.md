# Freshwater pond quality data 2007 [Countryside Survey] Data Table Descriptions

- Overview
  - Presents data table descriptions for Countryside Survey freshwater pond quality data from 2007.
  - Three main tables described: pond site information, pond macrophytes, and pond water quality.
  - Includes a key to environmental zones and a note on required acknowledgement and rights.

- Tables and key variables
  - POND_SITE_INFO_V_0_1.csv
    - Site and survey metadata: SQUARE, YEAR, SURVEY_DATE, AREA (m2).
    - Pond biology counts: TOTAL_SUB_SP, TOTAL_FL_SP, TOTAL_EM_SP, TOTAL_WET_SP.
    - Species and habitat flags: RARE_SP, GT30_PLANT_SP, PSYM_GT75, PSYM_ASSESSMENT, BAPPH_07.
    - Water-related and accessibility fields: WATER, OPEN_PA, VIEW_PROW.
    - Land classification and environment: LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.
  - POND_MACROPHYTES.csv
    - Macrophyte records: SQUARE, YEAR, SPECIES, PLANT_TYPE (Submerged; Floating; Emergent; Trees& Shrubs; Algae; Other).
    - Coverage data: COVER_FLOATING, COVER_SUBMERGED, COVER_EMERGENT, COVER_TREE_SHADE, COVER.
    - Land class and environment fields: LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.
  - POND_WATER_QUALITY.csv
    - Pond attributes: SQUARE, YEAR, POND_AREA, DRAWDOWN_HEIGHT (cm), PROPORTION_WATER_LEFT_IN_POND, DRIED_OUT.
    - Water chemistry: PH, CONDUCTIVITY, ALKALINITY, TURBIDITY (rank scale), PO4_P, TON.
    - Classification and geography: LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.

- Environmental zones
  - Includes a Key to Environmental Zones mapping zone codes to descriptions (e.g., Easterly lowlands, uplands, lowlands of Wales, etc.).

- Data quality and integration notes
  - Data types vary across tables; fields may require harmonisation (e.g., year formats, units like cm, m2, and scale for turbidity).
  - Join across tables typically via SQUARE and YEAR to build pond-level datasets or aggregated products.
  - POND_SITE_INFO_V_0_1.csv provides foundational pond context; POND_MACROPHYTES.csv adds species composition and cover by plant type; POND_WATER_QUALITY.csv supplies chemical and physical water metrics.

- Usage guidance for data support
  - Use the three tables to create self-serve analyses and dashboards on pond quality (biological, chemical, and physical attributes).
  - Validate data consistency and handle patchy or multi-format fields when merging from multiple sources.
  - Leverage PSYM-related fields for multimetric scoring and related assessments; use ENV_ZONE_2007 and LC07 for ecological classification analyses.
  - Consider country and environmental zone context when comparing ponds across regions.

- Provenance and acknowledgement
  - Data are owned by NERC - Centre for Ecology & Hydrology; Countryside Survey ©.
  - All use requires the acknowledgement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and the copyright notice.
  - Reference to Murphy, John; Weatherby, Anita. 2008 Countryside Survey. Freshwater Manual for further methodological context.

- Related references
  - Murphy, John; Weatherby, Anita. 2008 Countryside Survey. Freshwater Manual. NERC/Centre for Ecology & Hydrology.

- Practical note
  - Year of survey: 2007; consider consulting the CS Technical Report No.5/07 for additional methodological details and data handling guidance.