# Headwater stream invertebrate data 1990 [Countryside Survey] Data Table Descriptions

## Overview
- Documentation for Countryside Survey headwater stream macroinvertebrate data from 1990.
- Supports integration with later surveys and RIVPACS-based analyses.
- Data are owned by NERC - Centre for Ecology & Hydrology; require acknowledgement in all uses.

## Data Collection Methods
- Macroinvertebrates sampled using standard 1990 protocols (consistent with later years).
- Sampling area: a single stream-bed area capturing major habitats within about three minutes of active sampling plus one minute hand search.
- Typical reach length: 5–15 meters.
- Methods: standard 1 mm mesh pond net; samples returned to CEH for sorting/identification.
- Supplemental measurements: width, depth, substrate required for RIVPACS.
- Taxonomy and counting methods have evolved; data cross-checked against lab records and harmonised to a common modern taxonomy.
- Abundance data were progressively refined across years (presence/absence to species-level abundance estimates); standardisation derives mutually exclusive taxa for species richness.

## Data Structure (Tables)
- STREAM_INV_SITE_90.csv (Freshwater Stream - invertebrate sampling site data, 1990)
  - Key fields: YEAR, SQUARE (1km square code), SITE_ID, SAMPLE_DATE, WATER_WIDTH (m), DEPTH1/DEPTH2/DEPTH3 (cm), SURF_VEL_CAT (surface velocity category), CLARITY, SAMPLING_TIME (minutes), METHOD (sampling method), ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY, DOM_PART_SIZE (sediment phi), MACROPHYTE_COVER, LC07 / LC07_NUM (land classification 2007), EZ_DESC_07 (environmental zone), COUNTRY, COUNTY07.
- STREAM_INV_SP_90.csv (Freshwater Stream invertebrate species data, 1990)
  - Key fields: YEAR, SQUARE, SITE_ID, SAMPLE_DATE, SPECIES_CODE, NAME (scientific name), LC07 / LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07.

## Data Harmonisation, Quality, and Provenance
- Data entry: field sheets and lab data entered into a database; cross-checked against original lab sheets; errors corrected.
- Taxonomy: harmonised to a common modern taxonomy to enable cross-year comparability.
- Standardisation: derived mutually exclusive taxa lists for consistent species richness calculations.

## Usage, Metadata, and Licensing
- All CS data require acknowledgement:
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- Data can be used for GIS analyses, including mapping site-level variables, species distributions, habitat associations, and integration with land classification and environmental zones.

## GIS Relevance and Practical Applications
- Enables map-based visualization of headwater stream invertebrates across GB at 1km square resolution.
- Combine site-level measurements (width, depth, substrate, macrophyte cover) with land classification (LC07) and environmental zones for habitat suitability and association analyses.
- Species and richness data support distribution maps, hotspot analyses, and cross-year trend assessments when used with harmonised taxonomy.
- Potential integration with RIVPACS outputs for predictive mapping of invertebrate communities.

## Practical Considerations and Limitations
- Taxonomic and methodological changes over time require careful harmonisation and standardisation when combining with other years.
- Data reflect 1990 survey methods; spatial resolution is tied to 1km squares and site-level sampling within those squares.
- Availability and resolution of certain environmental variables may constrain some analyses.