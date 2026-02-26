# Headwater stream invertebrate data 2007 [Countryside Survey] Data Table Descriptions

## Overview
- Documents data tables and collection methodology for headwater stream invertebrates collected during the 2007 Countryside Survey.
- Context: supports freshwater monitoring and environmental health assessments; connected to the Countryside Survey Freshwater Manual and related reports.
- Dataset supports linkage to RIVPACS (River Invertebrate Prediction and Classification System) via accompanying physical measurements.

## Data collection and methods
- Sampling protocol: a single stream-bed sampling area (5–15 m reach) with up to three minutes of active sampling plus one minute of hand search.
- Equipment: standard 1 mm mesh pond net; samples returned to CEH for sorting and identification.
- Supplemental measurements: width, depth, substrate composition recorded to run RIVPACS.
- QA and audit: for 2007, 29 samples processed by APEM Laboratories; 10 main samples audited (initial processing/identification by CEH); APEM conducted internal audits of three QA samples.
- Taxonomic and abundance changes over time: data harmonised to a common modern taxonomy; abundances adjusted to enable comparability across surveys (1990: presence/absence; 1998: presence/absence for species and abundance classes for families; 2007: estimated actual abundances for species).

## Data structure and contents
- Data entry and storage: tablet-based data uploaded to CEH central database; laboratory-identified macroinvertebrate data entered from paper sheets and cross-checked against original lab sheets.
- STREAM_INV_SITE_07.csv
  - Year, square code (1 km grid), site identifier, sample date.
  - Physical and sampling variables: water width, depth at multiple points, surface velocity category, sampling time, method, substrate cover (rock pavement, boulders/cobbles, pebbles/gravel, sand, silt/clay).
  - Land classification and environmental context: LC07, LC07_NUM, EZ_DESC_07 (environmental zone), COUNTRY, COUNTY07.
- STREAM_INV_SP_07.csv
  - Year, square code, site identifier, sample date.
  - Species data: SPECIES_CODE, NAME, ABUNDANCE (2007 only), LC07, LC07_NUM.
  - Environmental context: EZ_DESC_07, COUNTRY, COUNTY07.

## Data quality, standardisation and harmonisation
- Taxonomy: harmonisation to a consistent modern taxonomy to enable cross-survey comparability.
- Abundance: standardisation to derive mutually exclusive taxa lists for species richness calculations.
- Metadata and provenance: explicit linkage to data collection methods, QA steps, and harmonisation decisions to support traceability.

## Data entry, validation and governance
- Data entry workflow: field data via tablets uploaded to CEH; lab identifications transcribed from paper sheets to database; data cross-checked against original lab sheets to correct errors.
- Data governance: data ownership and copyright attributed to NERC-Centre for Ecology & Hydrology; explicit acknowledgement requirements for data use.
- Licensing and acknowledgement: use of Countryside Survey data requires acknowledgment: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”

## Relevance for monitoring frameworks
- Illustrates the end-to-end process for environmental health monitoring data—from field collection and QA to harmonisation and publication-ready datasets.
- Highlights common challenges for monitoring authors:
  - Data gaps and access: reliance on metadata quality and availability for reuse.
  - Silos and data governance: need for integrated central databases and standardized metadata to facilitate cross-program comparisons.
  - Public data sharing: balancing openness with governance and attribution requirements.
- Demonstrates practical solutions: standardized sampling protocols, robust QA, harmonisation across time, and clear data documentation to support transparent, comparable environmental health metrics.