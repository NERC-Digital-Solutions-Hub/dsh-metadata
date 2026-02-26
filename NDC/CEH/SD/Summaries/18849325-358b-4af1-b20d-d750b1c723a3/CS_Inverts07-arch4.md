# Headwater stream invertebrate data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Document describes data tables for headwater stream invertebrate data from the 2007 Countryside Survey.
- Data are owned by NERC - Centre for Ecology & Hydrology (CEH); linked manuals and reports provide methodological context.
- Emphasises data collection, processing, harmonisation, standardisation, and usage guidance.

## Data collection methods
- Macroinvertebrates sampled in a single stream-bed area with three minutes of active sampling plus a one-minute hand search, over 5–15 m of stream length.
- Samples collected with a standard 1 mm mesh pond net and processed at CEH; supplementary measurements (width, depth, substrate) recorded for RIVPACS.
- QA process in 2007 included processing 29 samples at APEM Laboratories and audits of selected main samples; some identifications were performed by CEH.
- Taxonomic identification and counting methods have changed over time; harmonisation to a common modern taxonomy was applied to species data.

## Data processing and quality assurance
- Data from tablet computers uploaded to a central CEH database; extensive audit performed.
- Laboratory-identified macroinvertebrate data entered from paper sheets and cross-checked against original lab sheets to correct data-entry errors.
- Two key quality activities:
  - Harmonisation: aligns species data to a common modern taxonomy across surveys for comparability.
  - Standardisation: derives a mutually exclusive list of taxa for calculating species richness.
- Documentation notes changes in abundance recording across years (presence/absence → abundance classes → actual abundances).

## Data structure: Streams data tables
- STREAM_INV_SITE_07.csv: site-level freshwater stream invertebrate sampling data
  - Key fields include: YEAR, SQUARE (1 km square code), SITE_ID, SAMPLE_DATE, WATER_WIDTH, DEPTH1/2/3, SURF_VEL_CAT (surface velocity category), SAMPLING_TIME, METHOD, various substrate cover percentages (ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY), land class and environmental zone indicators, COUNTRY, COUNTY07.
  - Data types and descriptions accompany each field (e.g., numeric measurements, text codes, date).
- STREAM_INV_SP_07.csv: freshwater stream invertebrate species data
  - Key fields include: YEAR, SQUARE, SITE_ID, SAMPLE_DATE, SPECIES_CODE, NAME, ABUNDANCE (2007 only), LC07 (land classification), LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07.
  - Includes taxonomic and abundance information for each species observed, with related land class/environmental zone descriptors.

## Taxonomy harmonisation and standardisation
- Taxonomic names updated to a single, modern taxonomy to ensure consistency across survey years.
- Standardisation process produces a mutually exclusive taxa list for calculating species richness, enabling reliable cross-year comparisons.

## Data entry and QA workflow
- Tablet-based field data uploaded to CEH central database; comprehensive audit performed.
- Lab-identified macroinvertebrate data entered from paper sheets and cross-checked against lab records to correct errors.
- QA steps include external lab audits (APEM Laboratories) and internal checks on subset samples.

## Data governance, access, and licensing
- All use of Countryside Survey data must be acknowledged with the designated statement:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Data are provided under specific copyright and licensing terms; users must follow acknowledgment requirements in publications, presentations, and reports.

## Key implications and actions for Data Leaders
- Ensure clear provenance and documentation for dataset lineage (collection methods, QA/audit steps, harmonisation, standardisation).
- Prioritise metadata quality and update taxonomic standards to maintain cross-survey comparability.
- Implement robust data-entry controls and cross-checks between field records and laboratory identifications.
- Maintain explicit data governance practices, including licensing, acknowledgments, and usage rights.
- Recognise the importance of combining site-level and species-level data to support analytical workflows (e.g., RIVPACS integration, ecological assessments).
- Address data accessibility and discoverability by providing clear data tables, field definitions, and metadata references to support reuse across networks and partners.