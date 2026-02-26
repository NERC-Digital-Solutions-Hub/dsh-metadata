# River Habitat Survey (RHS) data 1998 [Countryside Survey] Dataset description

## Overview
- RHS assesses the physical structure of freshwater streams and rivers using a standard 500m sampling unit.
- Data are collected by accredited surveyors following standard protocols; no specialist geomorphology or botany required.
- Data entry workflow: field sheets collected on paper, entered into a database, and cross-checked against original sheets.
- Data are part of Countryside Survey outputs with formal acknowledgement and copyright by NERC - Centre for Ecology & Hydrology (CEH).

## Data collection scope and purpose
- Geographic coverage: England, Scotland, and Wales.
- Spatial framework: 1km square sampling units (SQUARE) with multiple survey components within each square.
- Survey focus: detailed site-level and channel morphology, hydrology, and adjacent land use to support GIS-based map visualisations and spatial analyses.
- Data released across multiple tables/CSV files describing field survey details, spot-checks, and bank attributes.

## Data structure and main datasets
- STREAM_RHS_SURVEY_main_98.csv
  - Core site details and field survey sections A, B, C, D, J, K, L, M, N, O, P, Q.
  - Key fields include:
    - SQUARE (1km square code), SITE_ID (site identifier), CS_SURVEY (survey year), COUNTRY, COUNTY07, SURVEY_DATE, ALTITUDE, SLOPE, FLOW_CATEGORY, HYDRO_UNIT, HEIGHT_SOURCE, CATCHMENT_AREA, STRAHLER_ORDER, SOLID_GEOLOGY, DRIFT_GEOLOGY.
    - Numerous morpho-physico descriptors (VALLEY_FORM, VALLEY_TERR, NO_RIFFLES, NO_POOLS, bed/bank features, channel dimensions, vegetation and debris indicators, etc.).
    - Habitat and geomorphology classifications and descriptive codes (e.g., CH_REALIGN, WAT_IMP_DAM, TREES_L/R, VEGETATION attributes, etc.).
- STREAM_RHS_SURVEY_spotcheck_98.csv
  - Spot-check data for RHS sections E, F, G.
  - Fields include YEAR, SQUARE, LC07, COUNTRY, COUNTY07, SPOT, LB_MAT, LB_MAT_DESC, LB_MD1/LB_MD2, CH_SUB/CH_FLW/CH_MD1/CH_MD2, RB_MAT/RB_MD1/RB_MD2, and habitat/land-use descriptors around banktop.
  - Additional columns capture bank-side features, channel substrates, and related descriptions.
- STREAM_RHS_SURVEY_bank_98.csv
  - Bank-focused data for RHS sections H and I.
  - Includes bank-specific attributes (BANK side, land-use within 50m of banktop for various categories, and a wide set of bank-related materials, modifications, vegetation, and bank profiles).
  - Notable fields cover land-use categories (BROAD, CONIF, SCRUB, ORCHARD, WETLAND, OPEN_WATER, URBAN, IRRIG, PARK, etc.), bank morphology (BANKFULL_LEFT/RIGHT, BKTOP, BKFULL_WIDTH, WATER_WIDTH/DEPTH), and channel vegetation types and descriptions.
  - Contains detailed descriptions for bank features, modifications, and surrounding land-use indicators within 5–50 m of banks.
- STREAM_RHS_SURVEY_main_98.csv, STREAM_RHS_SURVEY_spotcheck_98.csv, STREAM_RHS_SURVEY_bank_98.csv collectively comprise the RHS 1998 dataset components (main survey, spot-checks, and bank attributes).

## Data quality, standards and processing
- Data collection designed to ensure consistency across surveyors through accreditation and protocols.
- Data entry includes cross-checking against original field sheets to correct entry errors.
- Uses standardized field codes and descriptive descriptors for geomorphology, hydrology, and land use to facilitate GIS integration and interoperability.

## Usage and attribution
- All Countryside Survey data must be acknowledged in outputs.
- Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © CEH. All rights reserved.
- Data are suitable for map-based products and spatial analyses typical of GIS workflows and policy/public-facing GIS visualisations.

## References and related information
- Field handbook and technical reports associated with Countryside Survey (1998/2000) and subsequent headwater streams reports.
  - Module 2: Survey of freshwater habitats (Field handbook v.2.0, CEH)
  - Countryside Survey: Headwater Streams Report from 2007
  - CEH/CS technical reports and related datasets
- River Habitat Survey official website for additional context and methodology.