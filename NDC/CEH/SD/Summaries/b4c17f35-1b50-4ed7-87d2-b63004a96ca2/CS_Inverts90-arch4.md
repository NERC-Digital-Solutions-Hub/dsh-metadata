# Headwater stream invertebrate data 1990 [Countryside Survey] Data Table Descriptions

## Overview
- Describes 1990 macroinvertebrate data from Countryside Survey, collected using standard protocols and later harmonised for comparability with 1998 and 2007 surveys.
- Includes both site-level sampling data and species-level data for headwater streams.
- Data support River Invertebrate Prediction and Classification System (RIVPACS) and analyses of biodiversity; subject to specific acknowledgement and copyright.

## Data collection and scope
- Sampling method: single stream-bed area sampled within a 3-minute active period plus 1 minute hand search; typically 5–15 m of river length.
- Equipment: standard 1 mm mesh pond net; samples sent to CEH for sorting/identification.
- Supplemental measurements: width, depth, and substrate required for running RIVPACS.
- Taxonomic and counting methods evolved:
  - 1990: presence/absence recorded.
  - 1998: presence/absence at species level; abundance classes for families.
  - 2007: estimated actual abundances at species level.
- Harmonisation: taxa data standardized to a common modern taxonomy to enable cross-year comparability; standardisation performed to derive a mutually exclusive list of taxa for species richness calculation.
- Data entry workflow: laboratory identification followed by paper-based field sheets; data entered into a database and cross-checked against original lab sheets to correct errors.

## Data processing and quality
- Quality control included cross-checking entries against Lab Sheets; alignment to modern taxonomy on harmonisation/standardisation.
- Data products consist of site-level observations and species observations, enabling species richness and community analyses.
- All data are bound to the Countryside Survey data ownership and copyright framework.

## Data structure

### STREAM_INV_SITE_90.csv
- YEAR: Year of survey (Number)
- SQUARE: 1 km square sampling site code (Text)
- SITE_ID: Site identifier within the square (Number)
- SAMPLE_DATE: Date sample taken (Date)
- WATER_WIDTH: Width of water in stream (m) (Number)
- DEPTH1: Depth at 1/4 width (cm) (Number)
- DEPTH2: Depth at 1/2 width (cm) (Number)
- DEPTH3: Depth at 3/4 width (cm) (Number)
- SURF_VEL_CAT: Surface velocity category (Number)
- CLARITY: Water clarity (see handbook) (Number)
- SAMPLING_TIME: Sampling time (minutes) (Number)
- METHOD: Sampling method (1 = Kick, Kick/sweep) (Number)
- ROCK_PAVEMT: % cover of rock pavement (Number)
- BOULDER_COBBLE: % cover of boulders & cobbles (Number)
- PEBBLE_GRAVEL: % cover of pebbles and gravel (Number)
- SAND: % cover of sand (Number)
- SILT_CLAY: % cover of silt and clay (Number)
- DOM_PART_SIZE: Sediment phi score (see handbook) (Number)
- MACROPHYTE_COVER: % cover of macrophytes (Number)
- LC07: Land class 2007 descriptor (Text)
- LC07_NUM: Land class 2007 code (Number)
- EZ_DESC_07: Environmental zone (Text)
- COUNTRY: England, Scotland or Wales (Text)
- COUNTY07: County (Text)

### STREAM_INV_SP_90.csv
- YEAR: Year of Survey (Number)
- SQUARE: 1 km square sampling site code (Text)
- SITE_ID: Site identifier within the square (Number)
- SAMPLE_DATE: Date sample taken (Date)
- SPECIES_CODE: Species code (Text)
- NAME: Scientific species name (Text)
- LC07: Land class 2007 descriptor (Text)
- LC07_NUM: Land class 2007 code (Number)
- EZ_DESC_07: Environmental zone (Text)
- COUNTRY: England, Scotland or Wales (Text)
- COUNTY07: County (Text)

## Data governance and usage
- Acknowledgement required for all CS data use:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Supporting information and related reports:
  - Murphy, J.; Weatherby, A. 2008 Countryside Survey. Freshwater Manual.
  - Dunbar, M. et al. 2010 Countryside Survey: Headwater Streams Report from 2007.
- Data are intended to support analysis of headwater stream biodiversity and comparability across survey years; references and supplementary documents available through CEH/NERC channels.

## Implications for Data Leaders
- System-wide perspective: demonstrates end-to-end data lifecycle from field collection to harmonised, cross-year datasets suitable for long-term biodiversity analysis.
- Data discoverability and metadata: clear field definitions and data provenance (sampling methods, measurement variables, taxonomy changes) improve discoverability and reuse.
- Data quality and governance: explicit standardisation/harmonisation processes and documented data-entry validation enhance reliability; licensing and acknowledgement terms ensure responsible use.
- Addressing common challenges: dataset highlights issues such as taxonomy evolution, cross-year comparability, metadata completeness, and accessibility constraints—relevant when planning data strategies and cross-institution collaborations.
- Opportunities for cross-sector collaboration: standardized, well-documented data products can support broader communities of practice and data sharing across related ecological and water resource networks.