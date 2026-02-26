# Headwater stream invertebrate data 1998 [Countryside Survey] Data Table Descriptions

## Overview
- Describes the data tables and methods for headwater stream macroinvertebrate data collected in 1998 as part of Countryside Survey.
- Aims to support environmental monitoring and policy evaluation through standardized, verifiable datasets.
- Data intended for use with River Invertebrate Prediction and Classification System (RIVPACS) and related environmental assessments.
- Includes guidance on data provenance, harmonisation across surveys, and standardisation for species richness calculations.

## Data collection and sampling methods
- Macroinvertebrates sampled using standard Countryside Survey protocols.
- Sampling area: a single stream-bed area whose major habitat types can be sampled within three minutes of active sampling, plus a one-minute hand search.
- Survey length: typically 5 to 15 meters of stream.
- Equipment: standard 1 mm mesh pond net; samples sent to CEH for sorting and identification.
- Supplemental measurements recorded for RIVPACS: width, depth at multiple points, substrate composition, and other physical habitat data.
- Taxonomic identification and counting methods have changed across survey periods; historical data were harmonised to a common modern taxonomy and abundances were standardised to enable comparable analyses.

## Taxonomy, standardisation, and data harmonisation
- Data from different survey years were harmonised to a uniform, modern taxonomy to ensure comparability.
- A standardisation process derived a mutually exclusive list of taxa for calculating species richness.
- Abundance data evolved from presence/absence (1990) to species-level presence/absence (1998) and then estimated actual abundances for species (2007), necessitating harmonisation for cross-year consistency.

## Data entry and quality assurance
- Field data and laboratory identifications were initially recorded on paper, entered into a database, and cross-checked against original lab sheets.
- Data-entry errors were corrected to ensure integrity of the final datasets.

## Data tables and key fields
- STREAM_INV_SITE_98.csv (Freshwater Stream - invertebrate sampling site data)
  - Key fields include: YEAR, SQUARE (1 km square code), SITE_ID, SAMPLE_DATE, WATER_WIDTH, DEPTH1/DEPTH2/DEPTH3, SURF_VEL_CAT (surface velocity category), SAMPLING_TIME, % cover of substrate types (ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY), DOM_PART_SIZE, MACROPHYTE_COVER, LC07/LC07_NUM (land classification 2007), EZ_DESC_07 (environmental zone), COUNTRY, COUNTY07.
- STREAM_INV_SP_98.csv (Freshwater Stream - invertebrate species data)
  - Key fields include: YEAR, SQUARE, SITE_ID, SAMPLE_DATE, SPECIES_CODE, NAME (scientific name), LC07/LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07.
- Both tables are designed to align site-level habitat context with species-level observations and to support standardized analyses across years.

## Use, attribution, and access
- All Countryside Survey data must be acknowledged in use: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Data are © NERC-Centre for Ecology & Hydrology; all rights reserved.
- Acknowledgement and copyright notices should accompany copies of data, publications, presentations, or reports.  

## Outputs, applications, and forward-look
- Data support monitoring of environmental health and policy performance over time, with standardized formats suitable for monitoring frameworks like RIVPACS.
- Facilitates cross-year analyses through harmonised taxonomy and standardised taxon lists, enabling broader data integration.
- Highlights ongoing opportunities to increase data value by linking these datasets with additional environmental or socio-ecological data and by improving access to underlying data.