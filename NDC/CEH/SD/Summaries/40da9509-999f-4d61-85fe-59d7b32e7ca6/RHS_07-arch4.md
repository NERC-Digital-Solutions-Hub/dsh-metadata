# River Habitat Survey (RHS) data 2007 [Countryside Survey] Dataset  description

- Overview
  - RHS assesses the physical structure of freshwater streams and rivers using standard 500m sampling units.
  - Surveyors must be accredited; consistent recording follows published protocols to ensure comparability.
  - Data were collected in 2007 and entered via field tablets, then uploaded to a central CEH database with extensive auditing.

- Data collection and entry
  - Field data captured on tablet computers (2007) and uploaded to CEH’s central database.
  - Post-entry audit and quality checks performed to ensure data integrity.

- Data structure and main data files
  - STREAM_RHS_SURVEY_main_07.csv (main survey data)
    - Site-level details organized by 1km square sampling site (SQUARE) and SITE_ID.
    - Includes: year of survey (CS_SURVEY), location (COUNTRY, COUNTY07), land classification (LC07, LC07_NUM), environmental zone (EZ_DESC_07), and survey specifics (STREAM_OR_DRAIN, DISTANCE_F_SOURCE, ALTITUDE, SLOPE, FLOW_CATEGORY, CATCHMENT_AREA, STRAHLER_ORDER).
    - Geology and hydrology: SOLID_GEOLOGY, DRIFT_GEOLOGY, HYDRO_UNIT, HEIGHT_SOURCE, SURVEY_DATE.
    - Channel and habitat measures: PART_OF_RIV_OR_ART, ADV_COND, bed visibility (BED_VIS), survey origin (SURVFROM), spot-check indicator (SPOTCHECK), and numerous channel features counts (WEIRSMAJOR, WEIRSINT, WEIRSMINOR, SLUICES, BRIDGEMAJ/BRIDGEINT/BRIDGEMIN, OUTINT_MAJ/INT/MIN, FORDS_*, DEFLECT_*, REVET_*, OTHERMAJ/INT/MIN, etc.).
    - Bank and bed characteristics: CH_REALIGN, CH_OVER_DEEP, WAT_IMP_DAM, TREES_L/TREES_R, SH_CHANNEL, OVERHANG, EX_B_ROOTS, UW_T_ROOTS, FALLEN_TREES, C_WOODY_DEB, and multiple bed material/measurement fields (BED_MATERIAL, BED_MATERIAL_DESC, MEASURE_LOCATION, MEASURE_OTHER, etc.).
    - Habitat and structural indices: HQA_SCORE (Habitat Quality Score) and HMS_CLASS (Habitat Modification Scores Class).
    - Vegetation and land-use context: extensive banktop and bank vegetation fields (e.g., BANKFULL_LEFT/RIGHT, EMBANKED_HT_LEFT/RIGHT, BKFULL_WIDTH, WATER_WIDTH/DEPTH, etc.).
  - STREAM_RHS_SURVEY_spotcheck_07.csv (spot-check data)
    - Contains sections E, F, G for spot-check sampling (YEAR, SQUARE, LC07/LC07_NUM, COUNTRY, COUNTY07, BANK, and numerous spot-check descriptors).
    - Includes left-bank and right-bank material and modifications, channel substrates, flow types, and spot-check descriptors for channel features.
  - STREAM_RHS_SURVEY_bank_07.csv (bank/top sections data)
    - Covers sections F–I with banktop land-use, vegetation, and channel vegetation types.
    - Includes detailed right/left bank materials, banktop and bankface structure, banktop land-use within 5m, and an extensive set of channel vegetation type indicators (CV_*, CV_DESC, etc.).
    - Banktop and bank vegetation are linked to RHS spot-checks and provide context for habitat condition near banks.
  - All use of RHS data is accompanied by explicit acknowledgement requirements.

- Data quality, governance and usage notes
  - Data entered and curated through a central CEH database with formal auditing; standardized protocols ensure cross-site comparability.
  - Land classification codes follow ITE Great Britain 2007 (LC07/LC07_NUM) and country/county descriptors align with national UK schemes.
  - Habitat quality and modification scores (HQA_SCORE, HMS_CLASS) provide integrated indicators of ecological condition.
  - Documentation emphasizes that all Countryside Survey (CS) data usage must be acknowledged with the provided text.

- Access, rights and acknowledgement
  - Countryside Survey data are owned by NERC - Centre for Ecology & Hydrology; all rights reserved.
  - Acknowledgement to be used on all copies, publications, and presentations:
    - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
    - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
  - Data are provided to support data-driven decisions and cross-sector collaboration; emphasises a system-wide approach to data management and reuse.