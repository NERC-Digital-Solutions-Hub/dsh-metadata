# River Habitat Survey (RHS) data 1998 [Countryside Survey] Dataset  description

## Overview

- Provides River Habitat Survey (RHS) data collected in 1998 as part of the Countryside Survey, with copyright held by NERC - Centre for Ecology & Hydrology (CEH).
- Related supporting information includes field handbooks and technical reports from subsequent years (e.g., 2000 module 2 freshwater studies; 2007 headwater streams report), and a broader RHS official website.
- Data are organized as CSV tables corresponding to field survey sections and spot-checks, intended for use in assessing freshwater habitat structure and associated features.

## Data collection method and provenance

- RHS is a standardized assessment of the physical structure of freshwater streams and rivers using a 500 m sampling unit.
- Recording relies on consistent recognition of defined features; surveyors must be accredited to ensure consistency.
- Data collection relies on established protocols from referenced field handbooks and CEH/Environment Agency technical reports.
- Data were entered from paper field sheets into a database and cross-checked against the original sheets; data-entry errors were corrected.

## Data structure and content

- Main dataset: STREAM_RHS_SURVEY_main_98.csv
  - Contains site details and sections A, B, C, D, J, K, L, M, N, O, P, and Q.
  - Key fields include:
    - SQUARE: 1 km square sampling site code (text)
    - SITE_ID: site identifier within the square (numeric)
    - CS_SURVEY: year code (e.g., CS2000 for 1998 survey)
    - COUNTRY, COUNTY07, LC07 and LC07_NUM (land classification 2007)
    - SITE survey details (SURVEY_DATE, SURVFROM, ADV_COND, BED_VIS, etc.)
    - Physical and geomorphic attributes (ALTITUDE, SLOPE, FLOW_CATEGORY, CATCHMENT_AREA, STRAHLER_ORDER, HYDRO_UNIT)
    - Geology (SOLID_GEOLOGY, DRIFT_GEOLOGY), habitat and channel features (VALLEY_FORM, VALLEY_TERR, NO_RIFFLES, NO_POOLS, etc.)
    - Vegetation and bank/channel features (TREES_L, TREES_R, SH_CHANNEL, OVERHANG, EX_B_ROOTS, UW_T_ROOTS, FALLEN_TREES, C_WOODY_DEB, etc.)
    - Channel morphology descriptors (BED_MATERIAL, MEASURE_LOCATI ON, BRIDGEMAJ, BRIDGEINT, BRIDGEMIN, OUTFALLS, FORDS, DEFLECTOR, REVETMAJ, REVETINT, REVETMIN, OTHERMAJ, OTHERINT, OTHERMIN)
    - Habitat assessments and indicators (HQA_SCORE, HMS_CLASS)
- Spot-check data: STREAM_RHS_SURVEY_spotcheck_98.csv
  - Contains sections E, F, and G of RHS, including yearly spot-check records (YEAR), location (SQUARE, COUNTRY, COUNTY07), and spot-check specific attributes (LB_MAT, LB_MAT_DESC, LB_MD1/2, LB_FE1/2, CH_SUB, CH_FLW_DESC, RB_MAT/RB_MD1/2, RB_FE1/2, USE5_L/R, CV_* and other vegetation/channel features).
- Bank data: STREAM_RHS_SURVEY_bank_98.csv
  - Covers sections H and I (sweep-up) with bank-side attributes, land use within 50 m of banktop, and numerous habitat and modification indicators (BROAD, CONIF, SCRUB, OPEN_WATER, URBAN, IRRIG, PARK, NOTVIS, etc.), as well as bank profile details (L_BTOP/L_BFAC/L_BTOP_DESC, R_BTOP/R_BFAC/R_BTOP_DESC) and vegetation classifications (CV_B_L, CV_HER, CV_REE, CV_SBT, CV_FOL, etc.).
- Data usage notes
  - 999 = no value; -9 = missing value indicators within fields.
  - Units and measurement conventions follow the RHS field handbook and CEH documentation.
  - The dataset includes references to land classification and habitat descriptors with standardized coding schemes.

## Data standards, metadata and documentation

- Data align with the Countryside Survey and RHS documentation, including field protocol and data dictionaries.
- Cross-references to official RHS documents and the RHS website are provided for deeper metadata and method details.
- Acknowledgement and copyright notice must be used when reproducing data: Countryside Survey data owned by NERC - CEH; Countryside Survey © Database Right/Copyright NERC-CEH. All rights reserved.

## Access, usage, and licensing

- The data are provided as CSV tables with explicit field definitions and coding.
- All use of Countryside Survey data must be acknowledged, per the copyright notice.
- The dataset is associated with authoritative RHS resources, including the official website and CEH project reports, which provide additional context and methodological detail.

## Related resources and references

- Countryside Survey 2000 Module 2: Freshwater Studies (Field handbook v.2.0) – CEH report and unpublished material.
- Countryside Survey: Headwater Streams Report from 2007 (CS Technical Report No. 8/07) – CEH project number C03259.
- Countryside Survey 2000 – Environment Agency R&D Technical Report E1-038/TR1 (2002).
- River Habitat Survey official website: http://www.riverhabitatsurvey.org/

## Practical implications for data leadership

- Provides a comprehensive, standardized dataset for assessing river and stream habitat structure, enabling cross-site comparability and long-term monitoring when combined with other RHS datasets.
- Highlights the importance of accreditation, consistent protocols, and rigorous data-entry QC to ensure data reliability across networks.
- Demonstrates a multi-table data architecture (main RHS, spot-check, and bank data) that supports modular data governance, discoverability, and granular analysis of habitat features, land use, and bank modifications.
- Underlines the necessity of clear metadata, coding standards (e.g., missing value indicators), and explicit acknowledgement in all published outputs to protect data provenance and licensing.