# Headwater stream invertebrate data 1990 [Countryside Survey] Data Table Descriptions

## Overview
- Data from the Countryside Survey (NERC – Centre for Ecology & Hydrology) on headwater stream macroinvertebrates collected in 1990.
- Sampling followed standard protocols; aims to support analysis of stream invertebrates and compatibility with RIVPACS.
- Taxonomic identification and abundance data have evolved over time; data were harmonised to a common modern taxonomy and standardised for mutually exclusive taxa to enable species richness calculations.

## Data collection methods
- Sampling area: a single stream-bed area (5–15 m length) with major habitat types sampled within about three minutes of active sampling plus one minute of hand search.
- Equipment and protocol: standard 1 mm mesh pond net; samples brought to CEH for sorting and identification.
- Supplemental measurements: width, depth (at 1/4, 1/2, and 3/4 stream width), surface velocity category, water clarity, sampling time, and sampling method (1 = Kick, Kick/sweep).
- Habitat and substrate data: percent cover of rock pavement, boulders/cobble, pebbles/gravel, sand, silt/clay; sediment particle size (DOM_PART_SIZE); macrophyte cover.
- Land classification and environment: LC07 (land class 2007 codes), LC07_NUM, environmental zone (EZ_DESC_07), country, and county information.
- Data context: to support calculations such as those used by RIVPACS; all physical measurements collected to accompany biological data.

## Data harmonisation and standardisation
- Taxonomic changes over time: identification level and underlying taxonomy revised, requiring harmonisation across years.
- Abundance data: 1990 originally recorded as presence/absence; later years used species-level data and abundance classes for some taxa; harmonisation standardised data to enable cross-year comparability.
- Standardisation also produced a mutually exclusive list of taxa for accurate species richness calculations.

## Data entry and quality control
- Field data sheets and lab identifications recorded on paper, then entered into a database.
- Cross-checking performed against original lab sheets with corrections of any data-entry errors.

## Tables described
- STREAM_INV_SITE_90.csv
  - Freshwater Stream – invertebrate sampling site data, 1990
  - Key fields: YEAR, SQUARE (1 km square code), SITE_ID, SAMPLE_DATE, WATER_WIDTH, DEPTH1/DEPTH2/DEPTH3, SURF_VEL_CAT, CLARITY, SAMPLING_TIME, METHOD, ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY, DOM_PART_SIZE, MACROPHYTE_COVER, LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07, etc.
- STREAM_INV_SP_90.csv
  - Freshwater Stream invertebrate species data, 1990
  - Key fields: YEAR, SQUARE, SITE_ID, SAMPLE_DATE, SPECIES_CODE, NAME, LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07, etc.

## Usage, acknowledgements, and rights
- All Countryside Survey data must be acknowledged in outputs.
- Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey ©; all rights reserved.