# Headwater stream invertebrate data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Document for Countryside Survey data on headwater stream macroinvertebrates (2007), © NERC - Centre for Ecology & Hydrology, Version 1 dated 19/10/2016.
- Describes data collection methods, datasets, and data tables used to store site-level and species-level invertebrate data.
- Data support RIVPACS analyses and related environmental measurements; data are stored and curated by CEH.
- Acknowledgement and copyright requirements must be applied to all copies and presentations.

## Data collection and processing
- Macroinvertebrates collected using standard Countryside Survey protocols:
  - Sample area: a single stream-bed area sampled within three minutes of active effort, plus one minute of hand searching.
  - Length of stream surveyed: typically 5–15 meters.
  - Equipment: standard 1 mm mesh pond net; samples returned to CEH for sorting/identification.
  - Supplemental measurements: width, depth, and substrate composition recorded for running RIVPACS.
- QA and audit details for 2007:
  - 29 QA samples processed by APEM Laboratories Ltd.
  - Ten main samples selected for audit; initial processing/identification by CEH.
  - APEM also internally audited identifications of three QA samples.

## Taxonomy, data harmonisation, and standardisation
- Taxonomic level and underlying taxonomy have evolved; data harmonised across surveys to a common modern taxonomy.
- Abundance recording evolved over time:
  - 1990: presence/absence
  - 1998: presence/absence for species; abundance classes for families
  - 2007: actual abundances recorded for species
- A standardisation exercise derives a mutually exclusive list of taxa for calculating species richness.

## Data tables and schema
- STREAM_INV_SITE_07.csv
  - Brief: Freshwater stream - invertebrate sampling site data
  - Key fields: YEAR, SQUARE, SITE_ID, SAMPLE_DATE, WATER_WIDTH, DEPTH1/DEPTH2/DEPTH3, SURF_VEL_CAT, SAMPLING_TIME, METHOD, ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY, LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07
- STREAM_INV_SP_07.csv
  - Brief: Freshwater Stream - invertebrate species data
  - Key fields: YEAR, SQUARE, SITE_ID, SAMPLE_DATE, SPECIES_CODE, NAME, ABUNDANCE (2007 only), LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07

## Data quality assurance and auditing
- Central data entry pipeline:
  - Tablet-collected data uploaded to CEH central database.
  - Macroinvertebrate identifications conducted in the laboratory.
  - Data entered from lab sheets and cross-checked against original records; corrections made for any data-entry errors.
- QA outcomes contributed to harmonised taxonomic and abundance data across years.

## Data standards, metadata, and reuse
- Land classification and environmental descriptors incorporated:
  - LC07 and LC07_NUM (Land Classification 2007)
  - EZ_DESC_07 (Environmental zone)
  - COUNTRY and COUNTY07 (geographic attribution)
- Documentation and supporting materials reference standard works (e.g., Murphy & Weatherby 2008; Bunce et al. 2007) and provide links to classification resources for interpretation.
- All use of Countryside Survey data must be acknowledged with the provided attribution statement:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## Usage, sharing, and governance
- Data are prepared for discovery and reuse by others within appropriate governance boundaries.
- Systems and processes are in place to ensure data availability, accuracy, and timely updates, while respecting sharing limitations and licensing.