# Freshwater pond quality data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Describes three CSV data tables from the Countryside Survey 2007 focused on freshwater ponds: POND_SITE_INFO_V_0_1.csv, POND_MACROPHYTES.csv, and POND_WATER_QUALITY.csv.
- Provides variable-level definitions, data types, and descriptive codes to support data discovery, integration, and reuse.
- Data originate from the Countryside Survey and are intended to be used with the accompanying Freshwater Manual (Murphy & Weatherby, 2008).
- Tables include site-level information, macrophyte composition, and water quality metrics for surveyed ponds across Great Britain (England, Scotland, Wales).

## Data Tables and Key Variables

- POND_SITE_INFO_V_0_1.csv (General pond site information)
  - SQUARE: Countryside Survey square code
  - YEAR: Year of survey
  - AREA: Approximate pond area (m2)
  - SURVEY_DATE: Date pond was surveyed
  - TOTAL_SUB_SP, TOTAL_FL_SP, TOTAL_EM_SP, TOTAL_WET_SP: Counts of submerged, floating-leaved, emergent, and total wetland species
  - RARE_SP: Indicates presence of rare species (1/0)
  - GT30_PLANT_SP: Greater than 30 species recorded? (1/0)
  - PSYM_GT75: PSYM score greater than 75%? (1/0)
  - PSYM_ASSESSMENT: PSYM assessment text
  - BAPPH_07: Designated as BAP Priority Habitat? (1/0)
  - WATER: Contains water? (Y/N; for surveyed ponds)
  - COND_SURVEY: Condition survey undertaken? (Y/N)
  - OPEN_PA: Pond in area of open public access? (1/0)
  - VIEW_PROW: Visibility from a public right of way? (1/0)
  - LC07, LC07_NUM: Land class 2007 (text and numeric code)
  - ENV_ZONE_2007: Environmental zone (see key)
  - COUNTRY: England (Eng), Scotland (Sco) or Wales (Wal)

- POND_MACROPHYTES.csv (Macrophyte data for ponds)
  - SQUARE, YEAR: As above
  - SPECIES: Plant species name
  - PLANT_TYPE: Type of plant (SUBMERGED, FLOATING, Emergent, Trees& Shrubs, Algae, Other)
  - COVER_FLOATING, COVER_SUBMERGED, COVER_EMERGENT, COVER_TREE_SHADE: Cover percentages by type
  - COVER: Total cover percentage for totals where PLANT_TYPE indicates cover
  - LC07, LC07_NUM: Land class 2007 (text and numeric code)
  - ENV_ZONE_2007: Environmental zone
  - COUNTRY: England, Scotland or Wales

- POND_WATER_QUALITY.csv (Environmental and chemical pond data)
  - SQUARE, YEAR: As above
  - POND_AREA: Pond area (m2)
  - DRAWDOWN_HEIGHT: Drawdown height (cm)
  - PROPORTION_WATER_LEFT_IN_POND: Proportion of water left in the pond (%)
  - DRIED_OUT: Indicator of pond drying out
  - PH: pH
  - CONDUCTIVITY: Conductivity (mS/l)
  - ALKALINITY: Alkalinity (mg/l)
  - TURBIDITY: Turbidity (ranked scale; 1 = turbid, 4 = clear)
  - PO4_P: Phosphate (mg/l)
  - TON: TON (mg/l)
  - LC07, LC07_NUM: Land class 2007
  - ENV_ZONE_2007: Environmental zone
  - COUNTRY: England, Scotland or Wales

## Environmental Zone and Coding
- ENV_ZONE_2007 provides environmental zone classifications with a key linking zone codes to descriptions (e.g., Easterly lowlands, Westerly lowlands, uplands, etc.).
- LC07 and LC07_NUM provide standardized GB land class information for cross-table comparison.

## Data Quality, Formats, and Metadata
- Data types are specified per field (e.g., Text, Number, Date [SURVEY_DATE], VARCHAR2 for YEAR in some tables).
- Turbidity uses a ranked scale (1 = turbid, 4 = clear); Drawdown height is in centimeters.
- Year of survey is 2007 for all pond data; field definitions include descriptions to aid interpretation.
- Metadata supports join operations across tables via SQUARE, YEAR, LC07/LC07_NUM, ENV_ZONE_2007, and COUNTRY.

## Usage, Access, and Attribution
- All Countryside Survey data must be acknowledged:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology
- Data are associated with Murphy, John; Weatherby, Anita. 2008 Countryside Survey. Freshwater Manual.
- Data can be cited in publications and presentations with the provided attribution.

## Relevance for Data Leaders
- End-to-end data asset: three interconnected tables provide site, biodiversity, and water quality information for pond ecosystems, enabling holistic data strategy and system thinking.
- Facilitates user-centered data products: clear fields and codes support discovery, interpretation, and reuse by policy colleagues or external partners.
- Metadata richness supports data quality and interoperability: standardized keys (SQUARE, YEAR, LC07, ENV_ZONE_2007, COUNTRY) enable data integration, comparison across sites, and tracking of data provenance.
- Highlights practical data governance considerations: explicit zone and country classifications, clear data types, and an accompanying manual improve discoverability and reduce ambiguity.
- Potential constraints to consider: year is fixed to 2007; access and licensing terms require formal acknowledgment; some fields (e.g., PSYM_ASSESSMENT, rare species indicators) may require domain expertise to interpret.