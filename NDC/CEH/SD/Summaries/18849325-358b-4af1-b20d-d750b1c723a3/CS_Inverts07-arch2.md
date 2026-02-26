# Headwater stream invertebrate data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Documentation for the 2007 Countryside Survey headwater stream invertebrate data tables, including collection methods, data processing, standardisation, and table schemas.
- Supports monitoring of freshwater biodiversity and environmental health using harmonised, time-consistent data.

## Data Collection Methods
- Macroinvertebrate sampling followed standard protocols: a single stream-bed area sampled within three minutes of active searching, plus one minute of hand searching.
- Surveyed stream length typically 5–15 meters.
- Sampling employed a standard 1 mm mesh pond net; collected samples returned to CEH for sorting/identification.
- Supplemental measurements collected for RIVPACS use (width, depth, substrate composition).
- QA specifics: 29 samples from the QA exercise processed by APEM Laboratories; ten main samples audited with initial processing/identification by CEH; APEM also audited three QA samples.
- Taxonomic level and abundance counting changed over time; harmonisation to a common modern taxonomy implemented; standardisation produced a mutually exclusive taxa list for species richness calculation.
- Data entry: tablet-based data uploaded to CEH central database; lab-identified macroinvertebrate data cross-checked against original lab sheets to correct data-entry errors.

## Data Tables and Key Fields
- STREAM_INV_SITE_07.csv (Freshwater stream – invertebrate sampling site data)
  - YEAR, SQUARE, SITE_ID, SAMPLE_DATE
  - WATER_WIDTH, DEPTH1, DEPTH2, DEPTH3
  - SURF_VEL_CAT (surface velocity category 1–5)
  - SAMPLING_TIME, METHOD
  - ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY
  - LC07, LC07_NUM (Land Classification 2007)
  - EZ_DESC_07 (Environmental zone), COUNTRY, COUNTY07
- STREAM_INV_SP_07.csv (Freshwater Stream – invertebrate species data)
  - YEAR, SQUARE, SITE_ID, SAMPLE_DATE
  - SPECIES_CODE, NAME, ABUNDANCE (2007 only)
  - LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07
- Notes: LC07/Land Classification 2007 references and environmental zone descriptions provided; fields include taxonomic and environmental metadata to support cross-analysis and standardisation.

## Data Quality, Standardisation, and Taxonomy
- Taxonomic harmonisation to a common modern taxonomy to enable comparability across survey iterations.
- Standardisation to produce mutually exclusive taxa lists for robust species richness calculations.
- Acknowledges changes in taxonomic level of identification and abundance counting over time; standardisation mitigates these differences.

## Data Access, Usage, and Attribution
- All Countryside Survey data must be acknowledged in outputs.
- Acknowledgement example: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Data are subject to copyright; data use requires proper citation and acknowledgement.

## Relevance for Environmental Monitoring and Analysis
- Enables consistent, time-series assessment of environmental health via standardized invertebrate data and RIVPACS-compatible measurements.
- Supports mapping and reporting through standardized site and species data, with rich environmental context (width, depth, substrates, land classes, environmental zones).
- Provides a defensible dataset for policy performance evaluation and environmental health indicators, with QA and data provenance clearly documented.