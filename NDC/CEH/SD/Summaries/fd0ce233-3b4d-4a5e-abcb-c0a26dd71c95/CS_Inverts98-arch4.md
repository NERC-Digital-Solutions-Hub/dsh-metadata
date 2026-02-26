# Headwater stream invertebrate data 1998 [Countryside Survey] Data Table Descriptions

## Overview
- Describes headwater stream invertebrate data from the Countryside Survey (CS) 1998.
- Data tables provided: STREAM_INV_SITE_98.csv (site-level data) and STREAM_INV_SP_98.csv (species-level data).
- Includes data collection methods, data entry workflow, taxonomic changes and standardisation, and guidance on data use and acknowledgement.

## Data Collection Methods
- Macroinvertebrates sampled in a single stream-bed area within a 3-minute active sampling plus an additional 1-minute hand search, over typically 5–15 m of river.
- Specimens collected with a standard 1 mm mesh pond net and later sorted/identified in the CEH laboratory.
- Supplemental physical measurements collected for RIVPACS use: width, depth (three positions across the stream), and substrate information.
- Taxonomy and abundance recording changed over time (1990: presence/absence; 1998: presence/absence for species and abundance classes for families; 2007: estimated actual abundances for species); harmonisation to a modern common taxonomy and standardisation to mutually exclusive taxa lists were performed.

## Data Tables and Key Fields

- STREAM_INV_SITE_98.csv (Site-level data)
  - YEAR, SQUARE, SITE_ID, SAMPLE_DATE
  - WATER_WIDTH (m), DEPTH1/DEPTH2/DEPTH3 (cm)
  - SURF_VEL_CAT (surface velocity category), SAMPLING_TIME (minutes)
  - ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY (substrate cover %)
  - DOM_PART_SIZE (sediment phi score), MACROPHYTE_COVER (%)
  - LC07, LC07_NUM (2007 land classification)
  - EZ_DESC_07 (Environmental zone), COUNTRY, COUNTY07
  - Additional geographic identifiers: 1 km square code, etc.

- STREAM_INV_SP_98.csv (Species-level data)
  - YEAR, SQUARE, SITE_ID, SAMPLE_DATE
  - SPECIES_CODE (text), NAME (scientific name)
  - LC07, LC07_NUM, EZ_DESC_07
  - COUNTRY, COUNTY07
  - Taxonomic and coding fields align with land classification and environmental zones as above

## Taxonomy, Standardisation, and Data Harmonisation
- Across CS surveys, identification level and taxonomy have evolved; data harmonised to a common modern taxonomy.
- A standardisation process yields a mutually exclusive list of taxa for consistent species richness calculations.
- Abundance data evolved from presence/absence to more detailed abundance categories, and later to actual abundances in 2007.

## Data Entry, Quality Control, and Provenance
- Macroinvertebrate identifications were performed in a laboratory, with data entered from paper field sheets into a database.
- Records were cross-checked against original lab sheets; any data-entry errors were corrected.
- Data collection and processing are documented in associated CS reports and field handbooks (referenced in the document).

## Access, Usage, and Acknowledgement
- All Countryside Survey data require acknowledgement.
- Acknowledgement text:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Data references and supporting information are provided for further details and methodological context.