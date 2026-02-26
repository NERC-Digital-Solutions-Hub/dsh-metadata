# Headwater stream invertebrate data 2007 [Countryside Survey] Data Table Descriptions

- This document describes the data structure and collection methods for headwater stream macroinvertebrate data from the 2007 Countryside Survey.
- Data support aims: enable others to explore data and obtain insights by detailing data collection, harmonisation, and data product possibilities.

## Data collection and QA

- Sampling protocol: single stream-bed reach (5–15 m) with about 3 minutes of active sampling plus 1 minute of hand search; use a standard 1 mm mesh pond net; supplemental measurements collected (width, depth, substrate) for RIVPACS.
- Laboratory processing: samples processed by APEM Laboratories for QA; some samples initially processed/audited by CEH; internal audits performed on identifications.
- Taxonomy and abundance harmonisation: taxonomic names revised over time; abundance recording evolved (1990: presence/absence; 1998: presence/absence for species and abundance classes for families; 2007: estimated actual abundances for species). Species data harmonised to a common modern taxonomy; a secondary standardisation ensures mutually exclusive taxa for species richness calculations.
- Data entry flow: tablet data uploaded to CEH central database; lab-identified macroinvertebrate data recorded on paper, entered into a database, and cross-checked against lab sheets to correct errors.

## Data structure: STREAM_INV_SITE_07.csv (Freshwater stream - invertebrate sampling site data)

- YEAR: Year of survey
- SQUARE: 1 km square sampling site code
- SITE_ID: Site identifier (within 1 km square)
- SAMPLE_DATE: Date of sampling
- WATER_WIDTH: Stream width (m)
- DEPTH1 / DEPTH2 / DEPTH3: Depths at 1/4, 1/2, and 3/4 width (cm)
- SURF_VEL_CAT: Surface velocity category (1–5; 1 ≤10, 2 >10–25, 3 >25–50, 4 >50–100, 5 >100)
- SAMPLING_TIME: Sampling time (minutes)
- METHOD: Sampling method (1 = Kick, Kick/sweep; 16 = Search)
- ROCK_PAVEMT / BOULDER_COBBLE / PEBBLE_GRAVEL / SAND / SILT_CLAY: % cover of substrate types
- LC07 / LC07_NUM: Land classification 2007 (text and numeric code)
- EZ_DESC_07: Environmental zone (text)
- COUNTRY: England, Scotland or Wales
- COUNTY07: County or Council area corresponding to the 1 km square

## Data structure: STREAM_INV_SP_07.csv (Freshwater Stream - invertebrate species data)

- YEAR: Year of survey
- SQUARE: 1 km square sampling site code
- SITE_ID: Site identifier (within 1 km square)
- SAMPLE_DATE: Date of sampling
- SPECIES_CODE: Species code
- NAME: Species name
- ABUNDANCE: Abundance (only in 2007 data)
- LC07 / LC07_NUM: Land classification 2007 (text and numeric code)
- COUNTRY / COUNTY07: Geographic descriptors as above

## Taxonomy harmonisation and standardisation

- To enable cross-survey comparability, species names were harmonised to modern accepted taxonomy.
- A separate standardisation process produced a mutually exclusive taxon list for calculating species richness.

## Using the data: potential analyses and products

- Possible outputs: site-level and species-level summaries, diversity metrics, and self-serve data exploration dashboards or pivot-like tables.
- Analytic opportunities: relationships between macroinvertebrate communities and environmental variables (width, depth, substrate, velocity), temporal comparisons across years or sites, and species richness calculations using standardised taxa.
- Data products: ready-to-use site and species tables; documentation of data fields to facilitate interpretation and re-use.

## Access, usage, and acknowledgements

- All use of Countryside Survey data must acknowledge:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC-Centre for Ecology & Hydrology. All rights reserved.
- References and further information for context and methodology are provided in linked manuals and reports (Murphy & Weatherby 2008; Dunbar et al. 2010).