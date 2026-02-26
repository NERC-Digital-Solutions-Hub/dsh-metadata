# Headwater stream invertebrate data 1990 [Countryside Survey] Data Table Descriptions

## Overview
- Describes the 1990 headwater stream macroinvertebrate data tables from Countryside Survey (CS).
- Points to accompanying manuals and reports for methods and context (e.g., Murphy & Weatherby 2008; 2010 Headwater Streams Report).
- Emphasises data standardisation, quality assurance, and readiness for integration with other CS data.

## Data collection methods
- Macroinvertebrates sampled with standard CS protocols used in 1990 and in later years.
- Sampling area: a single stream-bed area with major habitats sampled within ~3 minutes of active sampling plus 1 minute hand search; typical surveyed length 5–15 m.
- Equipment: standard 1 mm mesh pond net; samples sent to CEH for sorting and identification.
- Supplemental measurements: width, depth, substrate to support RIVPACS (River Invertebrate Prediction and Classification System).
- Taxonomic changes over time; field counts and identification methods evolved (presence/absence in 1990; presence/absence and abundance classes in 1998; estimated actual abundances for species in 2007).

## Taxonomy, standardisation, and harmonisation
- Taxonomy and abundance data updated to a common modern taxonomy to enable cross-year comparisons.
- Standardisation process to derive a mutually exclusive list of taxa for accurate species richness calculations.
- Harmonised datasets enable consistent analyses despite methodological changes over the survey years.

## Data entry and quality assurance
- Laboratory identification of macroinvertebrates followed by data entry from paper sheets into a database; cross-checked against original lab sheets; errors corrected post-entry.

## Data tables and field definitions
- STREAM_INV_SITE_90.csv (Freshwater Stream - invertebrate sampling site data, 1990)
  - Key fields: YEAR, SQUARE, SITE_ID, SAMPLE_DATE, WATER_WIDTH, DEPTH1/DEPTH2/DEPTH3, SURF_VEL_CAT, CLARITY, SAMPLING_TIME, METHOD, ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY, DOM_PART_SIZE, MACROPHYTE_COVER, LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07.
  - Descriptions include sampling year, location code, sampling date, physical habitat metrics, substrate composition, macrophyte cover, land classification, environmental zone, and geographic identifiers.
- STREAM_INV_SP_90.csv (Freshwater Stream invertebrate species data, 1990)
  - Key fields: YEAR, SQUARE, SITE_ID, SAMPLE_DATE, SPECIES_CODE, NAME (scientific name), LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07.
  - Includes species-level data linked to site information, with taxonomic and environmental context.

## Usage, storage, and access
- Data are intended for standardised analysis and integration with other CS outputs (e.g., RIVPACS-based assessments, biodiversity indicators).
- Data entry and quality procedures support traceability from field to dataset.
- Encourages storage and uploading of created datasets to appropriate portals; supports broader data sharing in line with CS objectives.

## Acknowledgement and rights
- All CS data must be acknowledged in use.
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## Related resources
- Murphy, John; Weatherby, Anita. 2008. Countryside Survey. Freshwater Manual. NERC/CEH.
- Dunbar, M. et al. 2010. Countryside Survey: Headwater Streams Report from 2007. NERC/CEH.