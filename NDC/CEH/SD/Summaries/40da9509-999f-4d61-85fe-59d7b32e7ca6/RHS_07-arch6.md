# River Habitat Survey (RHS) data 2007 [Countryside Survey] Dataset  description

## Overview
- A dataset describing the physical structure of freshwater streams and rivers using River Habitat Survey (RHS) methodology.
- Based on standardized 500 m sample units; surveyors must be accredited to ensure consistent recording.
- Data collected in 2007; entries captured on field tablets and uploaded to a central CEH database with extensive quality checks.
- Aimed at enabling analysis of river and habitat characteristics across a 1 km square sampling framework.

## Data collection and scope
- Method: RHS assesses physical features of rivers/streams without requiring specialist geomorphological or botanical training; accreditation ensures recording consistency.
- Sampling: 1 km square sites, with multiple survey details stored per site (A–Q sections in main data table).
- Data entry: Field tablets used; data audited after upload to CEH central database.
- Supporting materials: Includes technical guidance and reports (Freshwater Manual, Headwater Streams Report) and RHS official website.

## Data structure and tables
- STREAM_RHS_SURVEY_main_07.csv
  - Core site-level dataset with sections A, B, C, D, J, K, L, M, N, O, P, Q.
  - Key identifiers and descriptors:
    - SQUARE (1 km square site code)
    - SITE_ID (site identifier)
    - CS_SURVEY (year code, e.g., “CS2007”)
    - COUNTRY, COUNTY07
    - EZ_DESC_07 (Environmental zone)
    - Numerous geomorphological and hydrological variables (e.g., STREAM_OR_DRAIN, ALTITUDE, SLOPE, FLOW_CATEGORY, CATCHMENT_AREA, STRAHLER_ORDER)
    - Bed/geomorph and hydraulic measurements (e.g., BANKFULL_LEFT/RIGHT, WATER_WIDTH, WATER_DEPTH, BED_MATERIAL, MEASURE_LOCATION)
    - Channel and habitat features (riffles, runs, pools, cascades, vegetation, deflectors, weirs, sluices, bridges, embankments, etc.)
    - Habitat quality and modification indicators (HQA_SCORE, HMS_CLASS)
- STREAM_RHS_SURVEY_spotcheck_07.csv
  - Spot-check data for sections E, F, G; includes a yearly field (YEAR), site identifiers (SQUARE, CS-related fields), and spot-check-specific descriptors (LB_MAT, LB_MD1/2, CH_SUB, CH_FLW, VARIOUS features in bank and channel context).
- STREAM_RHS_SURVEY_bank_07.csv
  - Bank-focused data for sections H and I; contains bank-specific attributes for left and right banks, land use within banktop, vegetation types, banktop/face structure, embankments, and associated descriptors.
  - Numerous fields capture land use, bank morphology, vegetation, and channel features on both banks.
- All data tables include extensive metadata descriptors for each field (data type, description, section mapping).

## Key variables and data types (highlights)
- Site and geography: SQUARE (text), SITE_ID (number), CS_SURVEY (year), COUNTRY/COUNTY07, EZ_DESC_07.
- Physical environment: ALTITUDE, SLOPE, FLOW_CATEGORY, CATCHMENT_AREA, STRAHLER_ORDER, HYDRO_UNIT, HEIGHT_SOURCE, SURVEY_DATE.
- River morphology: STREAM_OR_DRAIN, PART_OF_RIV_OR_ART, BANKFULL_LEFT/RIGHT, BKTOP_HT_LEFT/RIGHT, BKFULL_WIDTH, WATER_WIDTH, WATER_DEPTH, BED_MATERIAL, BED_MATERIAL_DESC, MEASURE_LOCATION, MEASURE_OTHER.
- Channel features and structure: RIFFLES, RUNS, POOLS, WAT_IMP_DAM, DEFLECT_MAJ/INT/MIN, WEIR/SLUICE counts, BRIDGEMAJ/BRIDGEINT/BRIDGEMIN, FLOOD and embankment indicators, CH_REALIGN, CH_OVER_DEEP, WETLAND/OPEN_WATER/BEDROCK related features.
- Vegetation and habitat indicators: TREES_L/TREES_R, CV_B_* (bank vegetation types and descriptions), HQA_SCORE (Habitat Quality Score), HMS_CLASS (Habitat Modification Scores Class).
- Spot-check specifics: SPOT (spot-check number), LB_MAT/LB_MD1/2, CH_SUB/CH_FLW, C_SUB1/2/3, and related descriptive fields.
- Bank attributes: BANK (left/right), L_BTOP/L_BFAC/R_BFAC/R_BTOP (banktop/face structures), USE5_L/R, CV_* vegetation categories, MAJ_IMP and L_MANAGE indicators.

## Data quality, usage, and licensing
- Data quality: Post-collection audit and verification conducted; data entry conducted with field tablets and centralized quality checks.
- Usage guidance: All use of Countryside Survey data must be acknowledged using the official acknowledgement text.
- Acknowledgement and rights: 
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
  - RHS data should be used in line with supporting documents and citations (Murphy & Weatherby 2008; Dunbar et al. 2010; RHS website).

## Practical notes for data users
- The dataset provides rich, multi-table RHS data for 2007, suitable for analyses of river habitat structure, morphology, bank characteristics, and associated vegetation and habitat quality indicators.
- Due to extensive field definitions and coding, refer to the field descriptions within each table to interpret variables correctly.
- Versioning: This description corresponds to RHS data 2007 dataset version 1 (dated 19/10/2016) with accompanying manuals and reports for detailed methodologies.