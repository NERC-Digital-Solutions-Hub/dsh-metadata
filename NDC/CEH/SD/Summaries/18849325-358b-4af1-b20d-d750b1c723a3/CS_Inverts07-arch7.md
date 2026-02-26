# Headwater stream invertebrate data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Dataset from Countryside Survey 2007 focusing on headwater stream macroinvertebrates.
- Aimed at enabling GIS-based analysis and map-based visualisations of stream invertebrate communities and related environmental context.
- Taxonomic data harmonised to a modern taxonomy; a standardisation process derives a mutually exclusive taxa list for species richness calculations.

## Data collection and processing
- Macroinvertebrates sampled using standard protocols: a single stream-bed area sampled within ~3 minutes of active sampling plus ~1 minute hand search; typical surveyed length 5–15 m.
- Samples collected with a 1 mm mesh pond net and later identified in a lab; supplementary measurements recorded (width, depth, substrate) for running RIVPACS-type analyses.
- QA involved: 29 samples processed by APEM Laboratories Ltd, with additional audits on selected samples; cross-checking of lab data against tablet/central database entries.
- Taxonomic identification and abundance recording have evolved over time; 1990–1998 data used presence/absence and abundance classes, while 2007 used estimated actual abundances for species. To ensure comparability, data were harmonised to a common modern taxonomy.
- Data entry workflow: field data entered from tablet exports to CEH central database; extensive audit and error corrections performed.

## Data structure (Tables)
- STREAM_INV_SITE_07.csv
  - Purpose: Freshwater stream invertebrate sampling site data.
  - Key fields: YEAR; SQUARE (1 km square code); SITE_ID; SAMPLE_DATE; WATER_WIDTH (m); DEPTH1/2/3 (cm); SURF_VEL_CAT (surface velocity category 1–5); SAMPLING_TIME (minutes); METHOD (sampling method); ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY (substrate composition percentages); LC07 and LC07_NUM (land classification 2007); EZ_DESC_07 (environmental zone); COUNTRY; COUNTY07; and related descriptive notes.
- STREAM_INV_SP_07.csv
  - Purpose: Freshwater stream invertebrate species data.
  - Key fields: YEAR; SQUARE; SITE_ID; SAMPLE_DATE; SPECIES_CODE; NAME; ABUNDANCE (2007 only; actual abundance); LC07; LC07_NUM; EZ_DESC_07; COUNTRY; COUNTY07.
  - Taxon-related fields align with the same land classification and environmental zone descriptors as SITE data.

## Data harmonisation and standardisation
- Taxonomic harmonisation across surveys to align to a current, consistent taxonomy.
- Standardisation creates a mutually exclusive taxa list to support robust species richness calculations and cross-year comparisons.

## Data entry and quality assurance
- Data entered from tablet workflow to central CEH database; lab-identified macroinvertebrate data cross-checked against original lab sheets.
- QA process included external auditing (APEM) and internal data checks to correct entry errors.

## Rights, attribution, and usage
- All use of Countryside Survey data must include acknowledgement.
- Acknowledgement wording: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Countryside Survey © and copyright restrictions apply; data usage requires proper attribution.

## GIS considerations and best use
- Spatial linkage via 1 km square codes (SQUARE) and site identifiers (SITE_ID) enables mapping of sampling locations and spatial patterns in invertebrate communities.
- Environmental context included via land classification (LC07/LC07_NUM) and environmental zone (EZ_DESC_07) to support thematic mapping of habitat associations.
- Substrate composition and physical measurements (width, depth) support habitat suitability analyses and integration with predictive models (e.g., RIVPACS).
- Useful for creating map-based data products showing species presence/abundance patterns, community richness, and environmental drivers across headwater streams for policy, clients, or public communication.