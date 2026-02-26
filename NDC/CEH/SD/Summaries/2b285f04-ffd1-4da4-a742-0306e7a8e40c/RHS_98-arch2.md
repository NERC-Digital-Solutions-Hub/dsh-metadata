# River Habitat Survey (RHS) data 1998 [Countryside Survey] Dataset description

- Purpose: Document RHS data collected in 1998 as part of Countryside Survey; provides standardized, auditable data on the physical structure of freshwater streams and rivers to support environmental health monitoring and policy evaluation over time.

## Overview and scope

- RHS assesses physical river/channel structure using standardized 500m length sampling units.
- Designed to be accessible to surveyors without specialist geomorphology or botany expertise, but requires accreditation and adherence to standard protocols.
- Data cover field survey details, site characteristics, and a wide range of habitat features to enable monitoring of environmental health.

## Data collection and provenance

- Data collection referenced to: RHS field methods and Handbooks (Module 2: Freshwater Studies) from Countryside Survey 2000 and related technical reports.
- Data collected in the 1998 RHS survey window; Countryside Survey and CEH are the data custodians.
- Data collection process: field sheets completed on paper, then entered into a database and cross-checked against original sheets to correct data-entry errors.

## Dataset structure and contents

- Main dataset: STREAM_RHS_SURVEY_main_98.csv
  - Key fields include: SQUARE (1km grid code), SITE_ID (site identifier), CS_SURVEY (year label, e.g., CS2000=1998), COUNTRY, COUNTY07, EZ_DESC_07 (environmental zone), STREAM_OR_DRAIN, ALTITUDE, SLOPE, FLOW_CATEGORY, CATCHMENT_AREA, STRAHLER_ORDER, HYDRO_UNIT, SURVEY_DATE, ADV_COND, BED_VIS, SURVFROM, SPOTCHECK, and a broad suite of physical habitat descriptors.
  - Habitat and geomorph features captured: valley form, valley terrace, number of riffles/pools, weirs/sluices/culverts/bridges, banktop and bankfull measurements, embankments, bed/material description, channel dimensions, water depth/width, debris and woody features, channel vegetation, deposition features (unvegetated/vegetated bars, riparian features), and various "other" feature descriptors.
  - Feature codes and descriptions use structured categories (e.g., NO_RIFFLES, NO_POOLS, TREES_L/TREES_R, SH_CHANNEL, OVERHANG, EX_B_ROOTS, etc.) with detailed definitions.
  - Data types include text, numbers, and coded values; missing values use specific codes (e.g., -9, 999).
  - Summarising scores included: HQA_SCORE (Habitat Quality Score) and HMS_CLASS (Habitat Modification Scores Class).

- Spot-check dataset: STREAM_RHS_SURVEY_spotcheck_98.csv
  - Contains data for RHS E, F, and G sections; includes Year, SQUARE, LAND CLASS codes (LC07 and LC07_NUM), COUNTRY, COUNTY07, and SPOT (spot-check number).
  - Spot-check fields extend to spot-specific observations and contextual site details to complement main data.

- Bank data: STREAM_RHS_SURVEY_bank_98.csv
  - Covers RHS sections H and I (sweep-up); includes bank-specific assessments of land use within 50m of banktop (e.g., OPEN_WATER, R_PASTURE, IMP_GRASS, URBAN, etc.), and extensive bank-related descriptors (BANK, BANKTOP, BANKFULL, EMBANK, EMBANK_WIDTH, WATER_WIDTH, WATER_DEPTH, etc.).
  - Includes multiple bank-side features and land-use categories, with numerous descriptive fields for channel morphology and adjacent land use.

## Data quality, entry, and documentation

- Data entry pipeline: paper field sheets -> database -> cross-check against original sheets; corrections applied for any data-entry errors.
- Documentation provides explicit field definitions, data types, and coding schemes, enabling consistent interpretation and reuse.
- All RHS data usage requires acknowledgement to NERC - CEH; formal acknowledgement text provided for publications and presentations.

## Outputs and usage in environmental monitoring

- RHS data can support outputs such as site reports, maps, and charts illustrating habitat structure and health.
- Standardized metrics like Habitat Quality Score (HQA) and Habitat Modification Scores (HMS) enable comparison across sites and time, informing policy performance and environmental condition assessments.

## Access, challenges, and governance

- Challenges noted in the archetype context include increasing the value of RHS datasets by combining them with other relevant data and enabling access to the underlying data used to produce outputs.
- Data ownership and licensing: Countryside Survey data are owned by NERC - CEH; access and use must follow the provided acknowledgement and copyright statements.
- Acknowledgement requirement: Include the stated Countryside Survey attribution in all copies, publications, or presentations.

## Version and sources

- Version: 1
- Date: 19/10/2016
- Source: Countryside Survey data © NERC - Centre for Ecology and Hydrology; references to Field Handbook v2.0 (1998) and associated Technical Reports. River Habitat Survey official website referenced for additional context.