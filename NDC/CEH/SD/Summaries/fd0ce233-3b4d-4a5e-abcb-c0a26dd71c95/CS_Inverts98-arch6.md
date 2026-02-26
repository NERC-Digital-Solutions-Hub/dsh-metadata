# Headwater stream invertebrate data 1998 [Countryside Survey] Data Table Descriptions

## Overview
- Documents two data tables from Countryside Survey 1998: STREAM_INV_SITE_98.csv (freshwater stream site data) and STREAM_INV_SP_98.csv (freshwater stream invertebrate species data).
- Part of the broader Countryside Survey efforts documenting headwater streams and their macroinvertebrates; data underpin later analyses such as RIVPACS and habitat classifications.
- Includes data collection methods, data entry processes, taxonomy harmonisation, and standardisation for cross-year comparability.
- All use requires acknowledgement to NERC - Centre for Ecology & Hydrology.

## Data collection methods
- Macroinvertebrates sampled using standard Countryside Survey protocols.
- Sampling area: 5–15 meters of stream length with 3 minutes of active sampling plus 1 minute of hand search.
- Sampling tools: standard 1 mm mesh pond net; samples sent to CEH for sorting and identification.
- Supplemental measurements recorded to enable running RIVPACS: width, depth, substrate composition.
- Taxonomy and abundance recording evolved over time:
  - 1990: presence/absence data only.
  - 1998: presence/absence at species level; abundance classes for families.
  - 2007: actual abundances recorded for species.
- To ensure cross-year comparability, taxa were harmonised to a common modern taxonomy; a standardisation exercise produced a mutually exclusive list of taxa for species richness calculations.
- Data entry workflow: field sheets and lab identifications entered into a database; cross-checked against original lab sheets to correct data-entry errors.

## Data tables and key fields

- STREAM_INV_SITE_98.csv (Freshwater Stream - invertebrate sampling site data)
  - YEAR: Year of survey
  - SQUARE: 1 km square sampling site code
  - SITE_ID: Site identifier within the square
  - SAMPLE_DATE: Date of sampling
  - WATER_WIDTH: Width of water (m)
  - DEPTH1, DEPTH2, DEPTH3: Depth measurements at various stream widths (cm)
  - SURF_VEL_CAT: Surface velocity category
  - SAMPLING_TIME: Sampling time (minutes)
  - ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY: Percent cover of substrate types
  - DOM_PART_SIZE: Sediment phi score
  - MACROPHYTE_COVER: Macrophyte cover (%)
  - LC07, LC07_NUM: Land Class 2007 (text and numeric code)
  - EZ_DESC_07: Environmental zone
  - COUNTRY, COUNTY07: Country and administrative area (England/Wales/Scotland)

- STREAM_INV_SP_98.csv (Freshwater Stream - invertebrate species data)
  - YEAR, SQUARE, SITE_ID, SAMPLE_DATE: Correlate with site-level data
  - SPECIES_CODE: Species code
  - NAME: Scientific species name
  - LC07, LC07_NUM: Land Class 2007 (text and numeric code)
  - EZ_DESC_07: Environmental zone
  - COUNTRY, COUNTY07: Country and administrative area
  - Notes indicate category encoding to reflect 2007 classifications and regional distinctions

## Data quality, harmonisation, and standards
- Taxonomic harmonisation across surveys to align with modern taxonomy, enabling comparability over time.
- Standardisation creates mutually exclusive taxa lists for robust species richness calculations.
- Data entry quality assurance includes cross-checking field data with laboratory records to correct errors.
- Documentation clarifies data type differences across years (presence/absence vs abundance) and how these were reconciled for analysis.

## Usage, access, and attribution
- All use of Countryside Survey data must include the acknowledgement:
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- References to accompanying technical reports and field handbooks provide methodological context (e.g., module handbooks and headwater streams reports).

## Practical notes for data support practitioners
- When integrating these tables with other CS datasets, account for taxonomy changes and standardisation decisions to maintain comparability.
- Preserve provenance by maintaining survey year, square, site ID, and sample date linkage between site- and species-level data.
- Use the habitat and substrate variables to contextualise macroinvertebrate assemblages and enable RIVPACS-driven or habitat-based analyses.

## References and further information
- Related field manuals and technical reports for Countryside Survey freshwater studies (e.g., Module 2 field handbook, Headwater Streams Report from 2007, and other CS data center materials) provide detailed methodologies and classifications referenced in these tables.