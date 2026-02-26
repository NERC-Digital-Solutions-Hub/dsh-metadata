# River Habitat Survey (RHS) data 1998 [Countryside Survey] Dataset description

- The RHS is an assessment of the physical structure of freshwater streams and rivers using a standardized 500 m sampling unit.
- Survey protocol requires accredited surveyors and consistent recording across a 1 km square framework; data are collected under the Countryside Survey program.
- Data were recorded on paper, then entered into a database and cross-checked against original sheets to correct data-entry errors.

## Data collection and scope

- Version: RHS data from 1998, part of the Countryside Survey 2000 pipeline (Module 2: Freshwater Studies; field handbook reference provided).
- Sampling framework: 1 km square sampling sites; the core RHS dataset described here comprises field-survey details across multiple sections (A, B, C, D, J, K, L, M, N, O, P, Q) and related spot-checks.
- Data entry workflow: paper field sheets → database entries → quality checks against original sheets.
- Additional references and supporting information are cited for methods and classifications (e.g., land classification, habitat descriptions).

## Tables and key variables

- STREAM_RHS_SURVEY_main_98.csv
  - Core site details and field survey sections (A, B, C, D, J, K, L, M, N, O, P, Q).
  - Key fields include: SQUARE (1 km² code), SITE_ID, CS_SURVEY (survey year code), COUNTRY, COUNTY07, EZ_DESC_07 (environmental zone), SURVEY_DATE, ALTITUDE, SLOPE, FLOW_CATEGORY, CATCHMENT_AREA, STRAHLER_ORDER, HYDRO_UNIT, HEIGHT_SOURCE, SURVEY_DATE, ADV_COND, BED_VIS, VALLEY_FORM, VALLEY_TERR, NO_RIFFLES, NO_POOLS, and extensive channel/bank morphology and vegetation descriptors.
  - Habitat quality and modification indicators: HQA_SCORE, HMS_CLASS, L_MANAGE, ANIMALS, ALDERS, DIS_ALDERS.
  - Numerous detailed bed, bank, vegetation, and channel morphology fields (e.g., TREES_L/R, SH_CHANNEL, OVERHANG, EX_B_ROOTS, UW_T_ROOTS, FALLEN_TREES, WATER_DEPTH, BANKFULL_LEFT/RIGHT, BKTOP_HT_LEFT/RIGHT, WATER_WIDTH, etc.).
  - Includes land-use/geomorphology and habitat attributes linked to 2007 land classification codes.

- STREAM_RHS_SURVEY_spotcheck_98.csv
  - Spot-check data for RHS sections E, F, G.
  - Key fields include YEAR, SQUARE, LC07/LC07_NUM, COUNTRY/COUNTY07, EZ_DESC_07, SPOT, LB_MAT/LB_MAT_DESC, LB_MD1/LB_MD1_DESC, CH_SUB/CH_SUB_DESC, RB_MAT/RB_MAT_DESC, CH_FLW/CH_FLW_DESC, and related bank/channel features.
  - Captures left and right bank materials, channel modifications, marginal features, substrate descriptions, and spot-check-specific channel attributes.

- STREAM_RHS_SURVEY_bank_98.csv
  - Bank-related RHS data (sections H and I: Land use near banks, bank morphology, and vegetation types).
  - Includes YEAR, SQUARE, LC07/LC07_NUM, COUNTRY/COUNTY07, EZ_DESC_07, BANK (left/right), and extensive land-use fields within 50 m of banktop (e.g., OPEN_WATER, WETLAND, R_PASTURE, IMP_GRASS, URBAN, PARK, IRRIG, etc.).
  - Vegetation and bank features categories: BROAD, CONIF, SCRUB, HEATH, WETLAND, HERBS, various CV_* channel vegetation types; bank profile descriptors (L_BTOP/L_BTOP_DESC, L_BFAC/L_BFAC_DESC, USE5_L/USE5_L_DESC, etc.).
  - Includes habitat modification scores (HMS/HQA related fields) and bank profiles.

- Additional notes
  - The data use and interpretation rely on established RHS field handbooks and related Countryside Survey reports.
  - Table schemas and description notes include coding conventions, potential values, and boundaries (e.g., 999 = no value, -9 = missing value, P/N/Y/other codes for presence/absence/degree).

## Data quality, access, and licensing

- Data collection and entry include cross-checking against original paper sheets to correct entry errors.
- All use of Countryside Survey data must acknowledge CEH/NERC and include the specified acknowledgement text.
- Data are owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © database rights retained.

## Practical notes for analysts

- Scale considerations: RHS operates at 500 m field survey units within 1 km squares; suitable for analyzing habitat structure along streams and for integrating with land-use and hydrological data.
- Key derived metrics available: Habitat Quality Score (HQA), Habitat Modification Scores (HMS), and land-use near banks, which enable correlations between physical habitat structure, anthropogenic modification, and surrounding land use.
- When combining datasets, be mindful of coding schemes, missing values, and the need to harmonize land-class codes (e.g., LC07/LC07_NUM, 2007 land classification) across tables.
- Potential uses include habitat assessment, correlative studies between physical habitat features and ecological outcomes, and baseline layering for predictive habitat models.

## References and acknowledgement

- Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © database rights.
- Primary methodological references include: Furse et al. 1998 and 2002-2010 Countryside Survey technical reports; River Habitat Survey official website for methodology and updates.