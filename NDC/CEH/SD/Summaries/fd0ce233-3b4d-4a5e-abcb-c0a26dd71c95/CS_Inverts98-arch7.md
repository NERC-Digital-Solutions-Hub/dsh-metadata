# Headwater stream invertebrate data 1998 [Countryside Survey] Data Table Descriptions

## Purpose and scope
- Describes two data tables from the Countryside Survey headwater stream invertebrate dataset (1998): STREAM_INV_SITE_98.csv (site-level data) and STREAM_INV_SP_98.csv (species-level data).
- Supports ecological analysis and integration with GIS, including harmonisation across surveys and preparation for use with RIVPACS (River Invertebrate Prediction and Classification System).
- Data originate from field surveys of freshwater habitats; macroscope includes physical measurements, habitat descriptors, and invertebrate identifications.
- Emphasises the need for data acknowledgement and proper data standards when using CS data.

## Data collection and methods
- Macroinvertebrates sampled using standard protocols: 3 minutes of active sampling plus 1 minute of hand searching.
- Sampling area per site typically 5–15 meters of stream length; collected with a standard 1 mm mesh pond net and returned to CEH for sorting and identification.
- Supplemental physical measurements recorded to enable analyses and RIVPACS inputs: width, depth at multiple points, and substrate characteristics.
- Taxonomy and abundance recording have changed over time; harmonisation to a common modern taxonomy implemented to ensure comparability.
- Standardisation procedures also derive a mutually exclusive taxa list for calculating species richness.

## Data structure and tables
- STREAM_INV_SITE_98.csv (Freshwater Stream - invertebrate sampling site data)
  - Key fields: YEAR, SQUARE (1 km square code), SITE_ID, SAMPLE_DATE, WATER_WIDTH, DEPTH1/2/3, SURF_VEL_CAT (surface velocity category), SAMPLING_TIME, substrate cover categories (ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY), DOM_PART_SIZE (sediment phi score), MACROPHYTE_COVER, LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07.
- STREAM_INV_SP_98.csv (Freshwater Stream - invertebrate species data)
  - Key fields: YEAR, SQUARE, SITE_ID, SAMPLE_DATE, SPECIES_CODE, NAME (scientific name), LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07.
- Both tables use 1 km square site coding and include taxonomic and environmental descriptors to support spatial analyses and habitat modelling.

## Data quality, harmonisation, and standardisation
- Taxonomic identifications and abundance reporting have varied across surveys; harmonisation aligns data to a common modern taxonomy.
- Standardisation ensures mutually exclusive taxa lists for robust species richness calculations.
- Data entry workflow: field sheets -> database entry -> cross-check against original lab sheets; errors corrected as part of quality control.

## Data usage and attribution
- All Countryside Survey data require acknowledgement in outputs.
- Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey ©; All rights reserved.
- Data are suitable for GIS analyses involving stream habitat, landscape classification (LC07), environmental zones, and cross-referencing site-level and species-level information for spatial decision-making.

## Relevance for GIS specialists
- Provides structured, geolocated site and species data suitable for map-based visualization and spatial analysis.
- Enables integration with land classification (LC07) and environmental zone descriptors for habitat suitability and biodiversity modelling.
- The dual-table design supports both habitat characterization (site-level) and species distributions (species-level) across 1 km squares, aiding scalable mapping and trend analysis.