# Freshwater pond quality data 2007 [Countryside Survey] Data Table Descriptions

- A Countryside Survey data description document (data tables) for pond-related observations collected in 2007, produced by NERC – Centre for Ecology & Hydrology (CEH). Provides structure, fields, and coding for three main tables used to describe pond sites, macrophytes, and water quality.

## Tables and their key contents

- POND_SITE_INFO.csv
  - General pond site information by survey square and year.
  - Key fields: SQUARE, YEAR, AREA (m2), SURVEY_DATE, TOTAL_SUB_SP, TOTAL_FL_SP, TOTAL_EM_SP, TOTAL_WET_SP, RARE_SP, GT30_PLANT_SP, PSYM_GT75, PSYM_ASSESSMENT, BAPPH_07, WATER, OPEN_PA, VIEW_PROW, LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.
  - Describes site-level context and indicators of pond condition and floristic richness.

- POND_MACROPHYTES.csv
  - Macrophyte species recorded in ponds.
  - Key fields: SQUARE, YEAR, SPECIES, PLANT_TYPE (Submerged, Floating, Emergent, Trees& Shrubs, Algae, Other), COVER (percent cover categories like COVER_FLOATING, COVER_SUBMERGED, COVER_EMERGENT, COVER_TREE_SHADE), LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.
  - Provides species-level composition and canopy/coverage information.

- POND_WATER_QUALITY.csv
  - Environmental and chemical water-quality data for surveyed ponds.
  - Key fields: SQUARE, YEAR, POND_AREA, DRAWDOWN_HEIGHT (cm), PROPORTION_WATER_LEFT_IN_POND, DRIED_OUT, PH, CONDUCTIVITY, ALKALINITY, TURBIDITY, PO4_P, TON, LC07, LC07_NUM, ENV_ZONE_2007, COUNTRY.
  - Includes physical and chemical water parameters alongside pond context.

## Classifications and coding

- Land Class 2007 (LC07 and LC07_NUM): Uses the ITE Land Classification of Great Britain 2007 (Bunce et al.) for land-cover context within pond areas.
- Environmental Zones (ENV_ZONE_2007): Coded descriptions with a key mapping zone codes to zone descriptions (e.g., Easterly/Westerly lowlands, uplands, lowlands, etc.).
- COUNTRY: England, Scotland, or Wales.
- Additional codes appear across tables for data quality and categorisation (e.g., RARE_SP, PSYM assessments, BAPPH_07).

## Data quality, standards, and outputs

- Data are collected and intended to be quality assured, cleaned, and transformed for standardised outputs.
- Outputs include clear formats such as reports, maps, and charts, with datasets stored and uploaded to appropriate portals.
- Acknowledgement requirements: CS data must be acknowledged as owned by NERC-CEH; copyright and database rights apply.

## Temporal and geographic scope

- Year of survey: 2007.
- Spatial framework: Countryside Survey squares (SQUARE codes) across England, Scotland, and Wales.

## Documentation and references

- Related documentation: Murphy, John; Weatherby, Anita. 2008 Countryside Survey. Freshwater Manual. CS Technical Report No.5/07.
- Data references and DOIs provided for LC07 classification and environmental zone keys.

## Opportunities and considerations for Analysts Monitoring the Environment

- Use standardized pond data to assess environmental health and policy performance in freshwater ecosystems.
- Combine pond-level data with other freshwater datasets to enhance analytical value and support broader ecological indicators.
- Facilitate access to underlying data while maintaining clear provenance and standardised classifications (LC07, ENV_ZONE_2007, COUNTRY).
- Leverage PSYM assessments and habitat/potential indicators (BAPPH_07, RARE_SP) to identify priority monitoring areas and conservation needs.