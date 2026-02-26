# Headwater stream invertebrate data 1998 [Countryside Survey] Data Table Descriptions

- This document describes two data tables from Countryside Survey headwater stream invertebrate sampling (1998): STREAM_INV_SITE_98.csv (site-level data) and STREAM_INV_SP_98.csv (species-level data).
- Data support macroinvertebrate-based assessments and are used alongside other Countryside Survey materials (e.g., field handbook, RIVPACS) for environmental health monitoring and policy evaluation.

## Purpose and context

- Provides structured metadata and field/lab data required to analyse headwater stream invertebrates within the Countryside Survey.
- Supports environmental health indicators through standardized data collection, taxonomic harmonisation, and compatibility with RIVPACS.

## Data collection methods

- Macroinvertebrate sampling followed standard Countryside Survey protocols:
  - A single stream-bed sampling area per site, targeted during a three-minute active sampling period plus a one-minute hand search.
  - Surveyed river length typically 5–15 meters.
  - Use of a standard 1 mm mesh pond net; samples returned to CEH for sorting/identification.
  - Supplemental measurements collected: width, depth at multiple points, substrate composition, to run RIVPACS.
- Taxonomic practices evolved during the survey period; data harmonisation aligned species data to a common modern taxonomy for comparability.
- Abundance recording evolved:
  - 1990: presence/absence.
  - 1998: presence/absence for species, abundance classes for families.
  - 2007: actual abundances for species.
- A standardisation process derives a mutually exclusive list of taxa for calculating species richness.

## Data entry and quality control

- Field data collected on paper sheets, then entered into a database and cross-checked against original lab sheets.
- Data-entry errors corrected through verification against source documents.
- Data governance and quality assurance practices implied through lab-validated entry and harmonisation processes.

## Table descriptions and key variables

- STREAM_INV_SITE_98.csv (freshwater stream - invertebrate sampling site data)
  - Temporal and spatial identifiers: YEAR, SQUARE (1 km square code), SITE_ID (site identifier), SAMPLE_DATE.
  - Physical/habitat measurements: WATER_WIDTH, DEPTH1/DEPTH2/DEPTH3, SURF_VEL_CAT (surface velocity category), SAMPLING_TIME.
  - Substrate and habitat composition: ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY, DOM_PART_SIZE, MACROPHYTE_COVER.
  - Land classification and environmental context: LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07.
  - Additional classifications: LC07 and related numeric codes (for crosswalks to Land Classification 2007).
- STREAM_INV_SP_98.csv (freshwater stream - invertebrate species data)
  - Identifiers: YEAR, SQUARE, SITE_ID, SAMPLE_DATE.
  - Taxonomic data: SPECIES_CODE, NAME (scientific name), LC07, LC07_NUM, EZ_DESC_07.
  - Geographic context: COUNTRY, COUNTY07.
  - This table links species observations to site-level data, enabling calculation of metrics like species richness and diversity in conjunction with site variables.

## Data harmonisation, standardisation, and taxonomy

- To ensure comparability across survey years, species identifications were harmonised to a modern taxonomy, and standardised taxon lists were created for species richness calculations.
- The documentation notes changes in identification level and underlying taxonomy over time, highlighting the need for ongoing standardisation when aggregating across years.

## Usage notes and acknowledgment

- All Countryside Survey data must be acknowledged with:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- The data are intended for use in environmental monitoring, policy scrutiny, and decision-making, with careful attention to provenance and data-quality considerations described in the table descriptions.